# Words
If you want to share a solution to a puzzle, it would be nice if there is a
succinct way to describe it. In this chapter we are going to learn one way of
doing that.

We will be studying _words_, i.e. sequences of _letters_ over an _alphabet_. We
start out with an introductory example. Lets take the alphabet of `{N, E, S, W}`
without paying much attention to what the letters represent. Now we can create
words over that alphabet by stringing letters together. For example, `NENENENE`
is a perfectly fine word, just as `NEWSNEWSNEWS` is.

Let's imagine for a moment that the letters stand for compass directions and
that the words are instructions for some weary traveler that wants to find the
nearest inn. Even though the journey is often more valuable than reaching the
destination, try telling that to our traveler, who just wants to sleep. I we
would give the traveler the following instruction `NEWS`, they would know that
we are pulling their leg. Can you see why?

Our weary traveler, if they have their wits about them, can sanitize our
directions by removing all occurrences of `NS`, `SN`, `EW` or `WE`. This will
leave directions to the same destination without any detours.

## Free group
We our going to do the same for our instructions to solve permutation puzzles.
Every permutation puzzle has generators. E.g. Turn a face on the Rubiks cube,
shift these counters to the right, twist this section.

We will associate a letter with every generator. For every letter we also take
an inverse letter. So if the letter is `x` we will also have `x`^-1^. This will
be our alphabet.

We can form words over that alphabet by stringing letters together. We can
strike any occurrence of a letter with its inverse to normalize the word. It
could be the case that this will leave the empty word, i.e. the word with no
letters.

We can define an multiplication on words by juxtaposition. I.e. if we have two words
`u` and `v`, we can multiply them by listing all the letters of `u` first,
followed by the letters of `v`, make sure to normalize the word by striking out
occurrences of a letter with their inverse.

We can also define a inverse for a word. If you think hard what an inverse
should be, you would discover that it amounts to reversing the order of the
letters and inverting each letter. Once you strike out all occurrences of
letters and their inverse, you will be left with the empty word, which serves as
the identity element for words.

## Shortcut
We can take some a shortcut that saves space when discussing words. Instead of
listing the word `NNNNNNNN` literally we could also write `N`^8^, i.e. list the
letter and how often it occurs.

This works out nicely with inverse, because it is the same as the algebraic
manipulations of unknowns that you maybe encounter in school.

## Exercises
1. There is a well known riddle involving the compass directions. It goes like
   this
   
> You start your journey by traveling one kilometer due south. Then you make a
> turn and head east for one kilometer. Next, you make an other turn and follow
> a trail north for another kilometer. You end up where you started and are
> faced by a bear. What color is the bear?

  Can you solve this riddle?

2. Normalize the word `NNEWSSEEWWN`
3. Invert `NENENENE`
4. Multiply `abba` with `(ab)^-1`

## Implementation
Implement words over an alphabet and the operations that are defined on them.
