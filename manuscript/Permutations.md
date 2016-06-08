# Permutations
A permutation is a rearrangement of some objects. The objects that we are going
to arrange are the `n` numbers `0` through `n-1`, for certain values of `n`. We
will represent a permutation by listing the rearrangement explicitly. E.g. below
we are looking at a permutation of the numbers `0` through `2` where `0` and `1`
are swapped and `2` stays in its place.

```plain
[
    0 1 2
    1 0 2
]
```

If we are pressed for space, we could also represent a permutation by only
listing where the objects end up. I.e. `[1, 0, 2]`. 

## Composing Permutations
If we have two permutations, e.g. two permutations on 3 numbers the first
swapping `0` and `1`, the second swapping `1` and `2`, we can compose the two
permutations by doing the rearrangements one after the other. In our example the
composition is the permutation

```plain
[
    0 1 2
    2 0 1
]
```

### Order is Important
When we are composing two permutations we need to take care of the order in
which we compose them. First swapping `0` and `1` followed by swapping `1` and
`2` is a different permutation then first swapping `1` and `2` followed by
swapping `0` and `1`.

## Special Permutation; Identity
There is one special permutation. The permutation that does not rearranges any
of the objects. We call this permutation the *identity*. The identity has the
special property that is when you compose it with a permutation, you get the
permutation you composed the identity with.

## Inverse Permutation
For any permutation there is a special permutation called the *inverse*. If you
compose a permutation with its inverse you end up with the identity.

## Exercises
1. How many permutations on `n` numbers are there?
2. Compose the following two permutations `[1, 0, 2, 3]` and `[0, 1, 3, 2]`.
3. Convince yourself that every permutation has an inverse and that the inverse
   is unique.
4. Determine the inverse of `[1, 2, 3, 4, 0]` and `[1, 0, 3, 2]`. 
