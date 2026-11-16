# Todo list

## Continuation notes

- The cycle "Create f1 using multi-step" closed as a trapezoid onto `main`. Check whether it has
  landed, `main` at its closing and the `create-f1-using-multi-step` bookmark gone, locally and on
  the remote.
- `.vc-config.md` still has no `[validate]` table, so `vc-x1 validate` refuses. The template's
  "Configure this workspace" Todo was dropped before this cycle; ask Wink whether to restore it.

## In Progress

_No cycle currently in progress._

## Waiting

## Todo

### Retest the ladder markers once vc-x1 carries m-13

`vc-x1` 0.85.23 marks the next rung `(current)` in each commit's `zTOC.md`, as the cycle "Create
f1 using multi-step" showed. vc-x1 accepted `m-13`'s fix, a commit marking its own rung `(done)`
and nothing `(current)`. Once an installed build carries it, run a multi-step cycle again and check
that no committed tree names a `(current)` rung.

### Report that cycle --open duplicates a Todo entry's subsections

When the `## Todo` entry it moves already has `####` subsections, `vc-x1 cycle --open` nests them
inside its own scaffold, so `#### Problem`, `#### Solution`, and `#### Rungs` appear twice. Seen at
the opening of "Create f1 using multi-step". Report it to vc-x1 by a vc-x1-messages thread, on
Wink's go.

## Ideas

## Closed

### Create f1 using multi-step

#### Problem

Test the multi-step cycle's ladder markers, `(done)` and `(current)`, as `vc-x1 cycle` rewrites
them into each commit.

#### Solution

A three-rung ladder ran under `vc-x1` 0.85.23, the plain build: the opening, `feat: create
f1.txt`, and the closing as a trapezoid onto `main`. After each commit, the committed `zTOC.md`
and `vc-x1 cycle --status` were compared. They agreed, and each commit's tree named the next rung
`(current)`. Wink expected that and judges it wrong, the same finding as `m-13` in
vc-x1-messages, which vc-x1 accepted at `m-13-1` and which this build does not yet carry.

#### Acceptance check

- `f1.txt` exists in the closed tree.
- After each commit, `zTOC.md`'s ladder marks every committed rung `(done)` and the next one
  `(current)`, and `vc-x1 cycle --status` agrees with it.
- After the closing, every marker is final and the closing is a trapezoid onto `main`.

Result, at the closing's start: pass as written. `f1.txt` is in the tree, and after the opening
and after `feat: create f1.txt` the ladder and `cycle --status` agreed, the committed rungs
`(done)` and the next `(current)`. The markers after the closing and the trapezoid shape are
checked on the closed tree. The `(current)` marker the check accepts is itself the finding, `m-13`.

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

Creates `f1.txt` at the workspace root, holding the one line `f1`.

Finding, from the opening: the opening commit's `zTOC.md` already marks this rung `1 (current)`,
written by `cycle --commit` before any of this rung's work exists. Wink expected this and judges
it wrong: a commit's tree should not name as current a rung that nothing has started. AGENTS.md's
per-rung flow, step 7, states it as intended, "the rung `(done)` and the next `(current)`", so a
fix changes that rule as well as `vc-x1`. It is `m-13`, accepted by vc-x1 at `m-13-1`. The rung's
commit repeated it, marking the closing `2 (current)`.

##### Create f1 using multi-step closing

Records the acceptance check's result and the `(current)` finding, bumps the version to the
cycle's bare version, and files the two `vc-x1` findings as Todos. The closing is a trapezoid onto
`main`.

# References
