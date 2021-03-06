# Solving Permutation Puzzles
A book about solving permutation puzzles with the aid of computers

This book is distributed via [Leanpub][leanpub:solving-permutation-puzzles].

## Workshop
A workshop that will present this material will be held at [Joy of Coding][joy-of-coding].

## For the impatient
For the impatient, below is a short transcript on how to solve a geometric
puzzle with [GAP][gap].

### Puzzle
We will look at the symmetries of the pentagon, and how to reach a certain
configuration by rotating and flipping over.

### Finding generators
Number the vertices of the pentagon 1 through 5. If we rotate, notice that it
produces the permutation

```plain
[
  1, 2, 3, 4, 5
  2, 3, 4, 5, 1
]
```

or `(1 2 3 4 5)` for short. Flipping the pentagon over corresponds with the
permutation

```plain
[
  1, 2, 3, 4, 5
  1, 5, 4, 3, 2
]
```

or `(2 5)(3 4)`

### Creating group
Start `gap` and enter the following command to create the pentagon group.

```plain
pentagon := Group((1,2,3,4,5), (2,5)(3,4));
```

### Membership
We can use the group to check if a permutation is a member of the group. E.g. to
see that `(1 2)` is not a member of the group.

```plain
(1, 2) in pentagon;
```

Check that `(1, 5)(2, 4)` is a member.

### Solving
To solve the puzzle we want to find a word in the generators that is the
permutation.

We can do that by creating the free group, find a homomorphism and inspecting a
preimage.

```plain
f := FreeGroup("r", "s");
hom := GroupHomomorphismByImages(f, pentagon, GeneratorsOfGroup(f),
GeneratorsOfGroup(pentagon));
PreImagesRepresentative(hom, (1, 5)(2, 4));
```

[leanpub:solving-permutation-puzzles]: https://leanpub.com/solving-permutation-puzzles
[joy-of-coding]: http://joyofcoding.org/
[gap]: http://www.gap-system.org/ 
