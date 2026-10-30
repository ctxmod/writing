# One Topic per Page

A documentation page serves one reader task, and its scope is the
task, not the component: "Rotate the signing key" is a page;
"Key management" is a category. Related-but-different tasks get
their own page with their own title, and the connections between
pages are named in prose, not implied by adjacency.

## Rationale

Page scope is the unit of findability: a reader arrives from search
with one question, and a page that answers three tasks makes them
read past two irrelevant answers to find theirs — or, worse, follow
the steps for the neighboring task. The task test catches the common
failure: a page titled "Advanced configuration" mixes several tasks
under one adjective, while "Rotate credentials without downtime" and
"Set up a secondary region" each name one thing a reader wants to
do. Splitting is cheap and linking is free; the mixed page is the
only expensive shape. The limit case is genuine reference material —
a full option table — which serves the task "look up a setting" and
is one page by that test, not by length.
