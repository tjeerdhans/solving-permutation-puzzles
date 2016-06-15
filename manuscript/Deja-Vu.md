# Deja Vu
With the Schreier-Sims algorithm we can determine if a certain permutation is
contained in a certain group. This applies to permutation puzzles. We know the
the generators of the puzzle and we know the current state of the puzzle. We
would like to know if that state is reachable from the start by puzzling. Or if
someone disassembled the puzzle and assembled it incorrectly.

Not only do we want to know if a puzzle is solvable, but we would also want to
know how it is solvable. But this is not different from the other strategy that
we employed when we only had generators and did not know of the Schreier-Sims
algorithm. I.e. Do double bookkeeping on words and use that the get a final word
that takes the start puzzle state to the current puzzle state. The inverse word
Solves the puzzle.

## Implementations
Extend the Schreier-Sims algorithm and keep track of the corresponding words in
the generators for each permutation.
