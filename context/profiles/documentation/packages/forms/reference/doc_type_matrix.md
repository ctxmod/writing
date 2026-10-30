# The Document Type Matrix

Documentation fails most often by mixing the four jobs. The matrix:
every page is a tutorial, a how-to guide, a reference, or an
explanation — each answers a different reader need, and a page that
answers two does both worse.

## The four types

| Type | Reader need | Reader's state | Form |
| --- | --- | --- | --- |
| Tutorial | "Teach me the basics safely" | Newcomer, will judge the whole project by this hour | A lesson with guaranteed success: few steps, all working, outcome visible |
| How-to guide | "Get this specific thing done" | Practitioner, mid-task, impatient | Steps for one real goal, assuming the basics, naming prerequisites |
| Reference | "Look up the exact facts" | Practitioner, in flow, verifying | Neutral, complete, correct listings: options, flags, returns, formats |
| Explanation | "Help me understand why" | Reader with time, seeking the model | Background, design reasoning, comparisons, history |

The split is by reader need, not by topic: one subsystem legitimately
produces all four pages. "Build your first index" (tutorial),
"Reindex without downtime" (how-to), "Index options" (reference),
"How the index stack stays rebuildable" (explanation).

## Selection criteria

Ask what the reader is doing when they arrive. Learning the tool →
tutorial. Working on a task → how-to. Checking a fact → reference.
Deciding or diagnosing → explanation. A page whose draft answers two
of these splits into two pages, and the split usually reveals that
the drafts barely shared a sentence.

## The mixing failure modes

Each confusion has a signature: a tutorial that assumes setup it
never taught (how-to leaked in); a reference page that wanders into
why-the-design-is-so (explanation leaked in), bloating every lookup;
a how-to that pauses for a history lesson (explanation leaked in)
while the practitioner waits. The remedy is always the same: move
the foreign material to the page of its own type and point to it —
by name, in prose — from the place it was pulled out of.

## How the types age

The types also age differently, and knowing the type tells the
maintainer what must be checked: tutorials and how-tos break
silently when a step stops working, so they need executed
verification; references break loudly (a documented flag that does
not exist), so they need diffing against the product; explanations
go stale slowest. A page's type is therefore also its review
contract.
