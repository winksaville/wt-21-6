# Todo list

## Continuation notes

## In Progress

_No cycle currently in progress._

## Waiting

## Todo

## Ideas

## Closed

### chore: prepare the repo of vc-x1 cycles

#### Problem

This was a dual-repo but not setup properly for working with vc-x1

#### Solution

- Create bare TODO.md and zTOC
- Run vc-x1-dev cycle --open --title "chore: prepare the repo of vc-x1 cycles"
- Update Problem, Solution, Acceptance check
- vc-x1-dev cycle --scope both --close --single-step --body "..." --land main --push --dry-run
- vc-x1-dev cycle --scope both --close --single-step --body "..." --land main --push


#### Acceptance check

`vc-x1-dev cycle --status` which reads the record

#### Deliberation

_None._

#### Rungs

The rung subsections, in the ladder's order. The ladder itself is in `zTOC.md > ## Ladder`.

##### chore: prepare the repo of vc-x1 cycles opening

The cycle's setup commit: create the bookmark, delete `## Closed`'s contents, move the Todo entry
into this block, and bump the version-of-record.

##### chore: prepare the repo of vc-x1 cycles closing

Closing out the cycle.

# References

