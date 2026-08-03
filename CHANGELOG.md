# Changelog

All notable changes to the DodoDentist Claude plugin are documented here. The
project follows Semantic Versioning. Every published content change needs a
manifest version bump because Claude uses that version as its update cache key.

## 0.1.1

- The `clinic-administration` skill is now a byte-identical copy of the
  canonical skill in `@dododentist/skills`, synced by `pnpm sync:skills` and
  also published at
  [dododentist/skills](https://github.com/dododentist/skills) and served as a
  `skill://` resource by the connector itself.
- Its frontmatter gained the `license`, `compatibility` and `metadata` keys
  the agentskills.io spec expects. The skill body is unchanged.

## 0.1.0

Initial source-ready release.

- One `clinic-administration` skill covering the eight read-only,
  administrative DodoDentist tools.
- Hosted OAuth connector at `https://mcp.dododentist.com/mcp`.
- Explicit exclusion of patients, individual appointments, clinical data,
  writes and medical decisions.
