# Contributing

Thanks for helping improve these agents and skills.

1. **One piece, one place.** Check that an agent/skill doesn't already cover your
   idea; prefer extending it over adding a near-duplicate.
2. **Keep agents thin.** Judgment and procedure go in the agent; long reference
   material goes in `knowledge/`.
3. **Stay generic.** No client names, personal paths, secrets or private data.
4. **Verifiable output.** Every agent/skill should end with concrete, checkable
   output (tables, file:line, numbers).
5. **Frontmatter.** Agents need `name` and `description` (and optionally `tools`);
   skills need `name` and `description` in `SKILL.md`.
6. **Index it.** Add a one-line row to the README table.

Open a pull request with a short description of the problem the piece solves and
an example prompt you tested it with.
