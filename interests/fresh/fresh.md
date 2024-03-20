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
