# Maintaining architecture-brainstorming

This repository distributes an architecture-brainstorming skill. Runtime instructions belong in
`SKILL.md`; this file guides agents maintaining the repository itself.

- Preserve independence from any project, technology, or lifecycle stage.
- Keep brainstorming as the working method: explore ideas, then converge when evidence is sufficient.
  Do not require an interview or a complete protocol for every request.
- Separate ideas, hypotheses, recommendations, proposals, approved decisions, and open questions.
- Preserve the freedom to recommend and draft useful documentation within authorized work.
- Keep shared instructions in the entrypoint and conditional details in `references/`.
- Do not incorporate project memories, private conversations, personal data, machine paths, or
  pilot-specific rules. Examples must remain generic rather than creating universal restrictions.
- Treat templates as adaptable syntheses. Do not copy full standards or manuals, or claim compliance
  without appropriate evidence. Preserve sources and distinctions among standards, guidance, and practices.
- Before completing a change, validate frontmatter, metadata, and local links. When behavior changes,
  test a realistic situation outside the editing examples, with independent review when available.
- Test installation only in a temporary directory. Do not install skills into a requester's project
  without an explicit request, and do not commit installation artifacts.
- Use the existing `skills` CLI. Do not add an npm package, custom installer, or runtime dependency
  without demonstrated need.
- Use `main` as the default branch and tags for versions. Do not force-push or replace remote history
  to work around content or authorization conflicts.

The MIT license covers this repository's original content. External sources retain their own terms.
