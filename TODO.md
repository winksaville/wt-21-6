# Todo list

## Continuation notes

_None._

## In Progress

### Create f1 using multi-step

#### Problem

Test the multi-step cycle's ladder markers, `(done)` and `(current)`, as `vc-x1 cycle` rewrites
them into each commit.

#### Solution

Run a three-rung ladder with `vc-x1`, the plain build: the opening, one work rung that creates
`f1.txt`, and the closing as a trapezoid onto `main`. After each commit, check the ladder in
`zTOC.md` and `vc-x1 cycle --status`.

#### Acceptance check

- `f1.txt` exists in the closed tree.
- After each commit, `zTOC.md`'s ladder marks every committed rung `(done)` and the next one
  `(current)`, and `vc-x1 cycle --status` agrees with it.
- After the closing, every marker is final and the closing is a trapezoid onto `main`.

#### Deliberation

- Validation waiver: `.vc-config.md` has no `[validate]` table, so `vc-x1 validate` refuses. Wink
  waived validation for this cycle's rungs on 2026-11-16. The waiver covers the reviews and the
  commits and does not cover the Land, whose push still takes its own approval.
- Version: `Cargo.toml` is the version-of-record, `0.2.0-0` at the opening, `-1` at the work rung,
  and `0.2.0` at the closing. `version.toml` is left as found.

#### Rungs

The rung subsections, in the ladder's order. The ladder itself is in `zTOC.md > ## Ladder`.

##### Create f1 using multi-step opening

The cycle's first commit, carrying its plan: the bookmark, the last cycle's record deleted, and the
Todo entry moved into this block.

##### feat: create f1.txt

Create `f1.txt` at the workspace root, holding one line.

##### Create f1 using multi-step closing

Closing out the cycle.

## Waiting

## Todo

## Ideas

## Closed

# References
