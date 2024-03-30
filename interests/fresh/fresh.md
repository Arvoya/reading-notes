# Fresh

> Notes taken from [Fresh](https://fresh.deno.dev/docs/concepts/routing)

Designed to make it easy to build fast, scalable, and reliable applications.

* Page load times should be reduced to a minimum.
* The work performed on the client should be minimized.
* Errors should have a small blast radius - stuff should gracefully degrade.

## Architecture

[Islands Architecture](./fresh.md)

Fresh applications ship pure HTML to the client by default. Parts of a server-
rendered page can then be independently re-hydrated with interactive widgets
(islands).

Client is only responsible for rendering parts of the page that are interactive
enough to warrant the extra effort.

## Server Components

When you create a route, all of the components used are rendered on the server.
No javascript is sent to the client, unless you specifically include something
form the `/islands/` folder.

## Routing

Fresh routes are based on their URL path. By default routes specify which paths
they are invoked for using the name of the file. Routes can also define a
custom URL pattern for more advanced use cases.

File names are mapped to route patterns as follows:

* File extensions are ignored.
* Literals in the file path are treated as string literals to match.
* File names `<path>/index.<ext>` behave identically to a file named
`<path>.<ext>`.
* Path segments can be made dynamic by surrounding an identifier with
`[` and `]`.
* Paths where the last path segment follows the structure `[...<ident>]` are
treated as having a wildcard suffix.

| File Name                 | Route Pattern        | Matching Paths            |
|---------------------------|----------------------|---------------------------|
| index.ts                  | /                    | /                         |
| about.ts                  | /about               | /about                    |
| blog/index.ts             | /blog                | /blog                     |
| blog/[slug].ts            | /blog/:slug          | /blog/foo, /blog/bar      |
| blog/[slug]/comments.ts   | /blog/:slug/comments | /blog/foo/comments        |
| old/[...path].ts          | /old/:path*          | /old/foo, /old/bar/baz    |
| docs/[[version]]/index.ts | /docs{/:version}?    | /docs, /docs/latest, /docs/canary |

Advanced use-cases can require a more complex pattern be used for matching.

``` ts
import { RouteConfig } from "$fresh/server.ts";

export const config: RouteConfig = {
    routeOverride: "/x/:module@:version/:path*",,
};

// ...
```

### Route Groups

A route group is a folder which has a name that is wrapped in parentheses. This
enables grouping of related routes that may use a different `_layout` file for
each group.

``` bash
└── routes
    ├── (marketing)
    │   ├── _layout.tsx  # only applies to about.tsx and career.tsx
    │   ├── about.tsx
    │   └── career.tsx
    └── (info)
        ├── _layout.tsx  # only applies to archive.tsx and contact.tsx
        ├── archive.tsx
        └── contact.tsx
```

## Routes

There are 2 main parts to routes: `handler` and the `component`

### Handler route

``` ts
import { FreshContext, Handlers } from "$fresh/server.ts";

export const handler: Handlers = {
  GET(_req: Request, _ctx: FreshContext) {
    return new Response("Hello World");
  },
};
```

To define a handler, one needs to export a `handler` function or object from the
route module.

If the handler is an object, each key in the object is the name of the HTTP
method that the handler should be called for.

Example:

`GET` handler above is called for `GET` requests. If the handler were a
function, it is called for all requests regardless of the method. If an HTTP
method does not have a corresponding handler, a 405 HTTP error is returned
instead. If an HTTP method is not defined, a 501 HTTP error is returned.

### Component route

``` ts
import { PageProps } from "$fresh/server.ts";

export default function Page(props: PageProps) {
  return <div>You are on the page '{props.url.href}'</div>;
}
```

The component is the default export of the route module. It is the component
that is rendered when the route is matched. If no handler is defined, a default
handler is used that renders the component. You can override the default
handler to modify how the component is rendered.

### Mixed handler and component route

``` ts
import { HandlerContext, Handlers, PageProps } from "$fresh/server.ts";

export const handler: Handlers = {
    async GET(_req: Request, ctx: HandlerContext) {
        const resp = await ctx.render();
        resp.headers.set("X-Custom-Header", "Hello World");
        return resp;
    },
};
```

A custom handler is used to add a custom header to the response after
rendering the component.

### Async route components

``` ts
interface Data {
  foo: number;
}

export const handler: Handlers<Data> = {
    async GET(req, ctx) {
        const value = await loadFooValue();
        return ctx.render({ foo: value });
    },
};

export default function MyPage(props: PageProps<Data>) {
    return <p>Foo is {props.data.foo}</p>;
}
```

Here we have separate `handler` and `component` exports. The `handler` is
responsible for fetching the data and the `component` is responsible for
rendering the data. The `component` is passed the data as a prop. The `handler`
can also be used to modify the response before it is sent to the client. The
`handler` can also be used to handle errors. If an error is thrown in the
`handler`, the error is caught and the `component` is not rendered.

``` ts
// Async route component
export default async function MyPage(req: Request, ctx: RouteContext) {
  const value = await loadFooValue();
  return <p>foo is: {value}</p>;
}
```

Here we have a single `async` function that is both the `handler` and the
`component`. The `handler` is responsible for fetching the data and rendering
the component. The `handler` can also be used to modify the response before it
is sent to the client. The `handler` can also be used to handle errors. If an
error is thrown in the `handler`, the error is caught and the `component` is not
rendered.

This is useful for simple routes that do not require a separate
shandler` and `component`. Avoiding having to create the `Data` boilerplate.
