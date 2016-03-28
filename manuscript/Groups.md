# Groups
Some collection of permutation elements group together nicely. For example, if
you look at the following four permutations

```
[
    0 1 2 3
    0 1 2 3
]

[
    0 1 2 3
    1 0 2 3
]

[
    0 1 2 3
    0 1 3 2
]

[
    0 1 2 3
    1 0 3 2
]
```

Let's call them `a`, `b`, `c`, and `d`, in that order. These permutations form a
nice group in the sense that this collection is *closed*. I.e. it does not
matter which two permutations you multiply you always get a permutation in the
group. 

Below there is a multiplication table for these elements. This shows that
closed-ness property of the collection of permutations. 

|     | `a` | `b` | `c` | `d` |
| `a` | `a` | `b` | `c` | `d` |
| `b` | `b` | `a` | `d` | `c` |
| `c` | `c` | `d` | `a` | `b` |
| `d` | `d` | `c` | `b` | `a` |

The closed-ness property comes with other nice properties.

1. There is an **identity** element, i.e. an element that when multiplied with
   an other permutation `p` results in that permutation `p`.
2. For each permutation `p` there is an **inverse** element. I.e. an element
   that when multiplied with `p` results in the identity.

There is an interesting property that multiplication of permutation has. The
multiplication is called **associative**. Any collection of elements that
multiplies that satisfies the four properties **closed**, **associative**,
**identity** and **inverse** is called a [group][].

Groups are great tool for studying permutation puzzles. So we will study them in
closer detail.

## Exercises

1. Verify the properties for the group mention in this section?
2. Work out the multiplication table for the following collection of
   permutations `Id`, `(1 2 3 4)`, `(1 3)(2 4)`, `(1 4 3 2)`?
3. What elements should be added to the following permutations to make it a
   group: `(1 2 3)` and `(2 3)`?

[group]: https://en.wikipedia.org/wiki/Group_%28mathematics%29 

