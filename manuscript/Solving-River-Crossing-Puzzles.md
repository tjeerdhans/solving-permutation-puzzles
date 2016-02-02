# Solving River Crossing Puzzles

In the last chapter the *wolf, sheep, and cabbage* puzzle was introduced. If you
try to solve it, you probably end up doodling on a piece of paper. When I
doodled, I came up with a short representation of the _puzzle state_, i.e. a
complete description of the location of the ferryman, the wolf, the cabbage and
the sheep.

I opted for using the symbols `F`, `W`, `S` and `C` for the ferryman, wolf,
sheep and cabbage respectively. I use `|` to designate the river and place the
symbols on either side of it, to tell where the corresponding figure is. E.g.
the string `FWSC|` denotes the all figures are on the left bank of the river.
This could be the starting position. The end position would be described by
`|FWSC`.

**Excercise** How many different states does the wolf, sheep and cabbage puzzle
  has? 

To answer this question realize that there are four actors. The ferryman, the
wolf, the sheep and the cabbage. All of these actors can be found on either the
left bank or the right bank. This amounts to `2 * 2 * 2 * 2 = 16` different
states.

The table below lists all the possible states of the wolf, sheep and cabbage
puzzle.

| #  | State    | Notes     |
|---------------------------|
| 1  | `FWSC\|` | Start     |
| 2  | `FWS\|C` |           |
| 3  | `FWC\|S` |           |
| 4  | `FSC\|W` |           |
| 5  | `WSC\|F` | Forbidden |
| 6  | `FW\|SC` | Forbidden |
| 7  | `FS\|WC` |           |
| 8  | `FC\|WS` | Forbidden |
| 9  | `WS\|FC` | Forbidden |
| 10 | `WC\|FS` |           |
| 11 | `SC\|FW` | Forbidden |
| 12 | `F\|WSC` | Forbidden |
| 13 | `W\|FSC` |           |
| 14 | `S\|FWC` |           |
| 15 | `C\|FWS` |           |
| 16 | `\|FWSC` | Finish    |

We now have a good grasp of all the states that play a role in the sheep, wolf,
cabbage puzzle. But we the possible moves from each state are still unclear. Let
us focus on that for the a moment. From state 1, i.e. where we find everybody on
the left bank, it is possible to move to states 5, 9, 10, and 11, because the
ferryman could travel alone (state 5), or take on of the other actors (state 9,
10, 11 respectively).

**Excercise** Create a table that lists all possible moves for each state.

| State  | Neighbours    |
|------------------------|
| 1  | 5, 9, 10, 11      |
| 2  | 13, 14            |
| 3  | 10, 13, 15        |
| 4  | 14, 15            |
| 5  | 1                 |
| 6  | 16                |
| 7  | 14, 16            |
| 8  | 16                |
| 9  | 1                 |
| 10 | 1, 3              |
| 11 | 1                 |
| 12 | 16                |
| 13 | 2, 3              |
| 14 | 2, 4, 7           |
| 15 | 3, 4              |
| 16 | 6, 7, 8, 12       |

