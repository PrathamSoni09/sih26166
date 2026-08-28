### Three people, three fully separate boxes. Nobody waits on anybody.
----
## Person 1 — Preprocessing [pick one]
Takes one raw image → outputs one cleaned image (scaled + illumination-fixed).
Tests alone by making their own fake "before/after" pair (just resize + darken any image themselves).
## Person 2 — Matching & Geometry [Pratham Soni]
Takes two clean images → outputs matched points + transform matrix.
Tests alone by taking one image, applying a known rotation/scale to a copy of it, and checking if their code recovers that known transform.
## Person 3 — API + UI + Scoring/Overlay [pick one]
Builds the dashboard, confidence score formula, and overlay visual — all using fake made-up numbers/JSON that look like what Person 2 will eventually produce.
Tests alone with zero real matching happening — just hardcoded sample output.
----
We need to create a json structure to pass the data through the 3 systems, independent and can be work parallelly.