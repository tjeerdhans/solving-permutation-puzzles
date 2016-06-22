# Cycle Notation

Up till now we represented permutations as a table. This takes up a lot of
space. We could save some space by listing only the second row, because the
first row is always the same. I.e it is the numbers `0` through `n-1`. But if
the permutation permutes a lot of things, this is still taking up a lot of
space. Furthermore, it is hard to see what is going on in a glance.

We are going to look into a different representation, that could save some space
and shed more light on what is going on. It is called the *cycle notation*.

We will explain what the cycle notation is with an example. Lets look into the
following permutation

```plain
[
    0 1 2 3 4 5
    1 2 0 4 3 5
]
```

In order to construct the cycle notation we are going to start with a number
that is permuted by the permutation, e.g. `0`. We list `0` and see where it is
permuted to. In this case `1`, so we list it besides `0`. Next, we find out where
`1` is permuted, listing that besides `1`, i.e. `2`. Now to is permuted to `0`
and one cycle is closed. We continue with listing these numbers that are
permuted in this fashion until all numbers are inspected. It is customary to
leave out numbers that are not permuted. In our example we end up with the
following cycle notation.

```plain
(0 1 2)(3 4)
```

## Exercises

1. Find the cycle notation for the following permutation.

```plain
[
    0 1 2 3 4 5 6 7 8
    8 7 5 6 4 3 1 2 0
]
```

2. How does the cycle notation of two permutations relate to the cycle notation
   of their product? E.g `(0 1 2)` and `(3 4)`, or `(0 1 2)` and `(2 3)`.
3. Implement an algorithm to create the cycle notation given a permutation.

## Implementation
Implement the cycle notation for permutations.
