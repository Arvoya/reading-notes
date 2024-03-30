# Big 0 Time Complexity

Categorizes your algorithm on time or memory based on input. It is not an exact
measurement, but a general idea of how your algorithm will perform.

Example:

'Oh of N', grows linearly based on input.

## Why is it important?

Often it will help make decisions about which algorithm to use.
Knowing how they perform can help you make better programs.

**As your input grows, how fast does computation or memory grow?**

## Examples

How does this program's execution time grow with respect to input?

``` typescript
funciton sum_char_codes(n: string): number {
    let sum = 0;
    for (let i = 0; i < n.length; i++) {
        sum += n.charCodeAt(i);
    }
    return sum;
    }
```

This program has a time complexity of O(n) because the time it takes to run
grows linearly with the input.

Tip:

* Look for loops

---

``` typescript
function sum_char_codes(n: string) number {
    let sum = 0;
    for (let i = 0; i < n.length; i++) {
        sum += n.charCodeAt(i);
    }
    for (let i = 0; i < n.length; i++) {
        sum += n.charCodeAt(i)
    }
    return sum;
}
```

Constants are ignored, so this program still has a time complexity of O(n). Instead
of O(2n).

---

``` typescript
function sum_char_codes(n: string) number {
    let sum = 0;
    for (let i = 0; i < n.length; i++) {
        const charCode = n.charCodeAt(i);
        // Capital E
        if (charCode === 69) {
            return charCode;
        }
        sum += charCode;
    }

    return sum;
}
```

Often the worst case scenario is used to determine the time complexity. In this
case, the worst case is that the input is a string of 'E's is at the end of the array.
This would be O(n).

---
### O(N^2)

``` typescript
function sum_char_codes(n: string) number {
    let sum = 0;
    for (let i = 0; i < n.length; i++) {
        for (let j = 0; j < n.length; j++) {
            sum += n.charCode;
        }
    }
    return sum;
}
```

---

### O(N^3)

``` typescript
function sum_char_codes(n: string) number {
    let sum = 0;
    for (let i = 0; i < n.length; i++) {
        for (let j = 0; j < n.length; j++) {
            for (let k = 0; k < n.length; k++) {
                sum += n.charCode;
            }
        }
    }

    return sum;
}
```

---

### O(n log n)

* Quick sort

### O(log n)

* Binary search trees

## Important Concepts

1. growth is respect to the input
2. constants are ignored
3. worst case scenario is often used
    1. Depends on the algorithm
