# Changelog

## 1.0.0

Initial ChatGPT release with canonical DodoDentist icons, an administrative clinic sidebar and read-only connector metadata.

All notable changes to the DodoDentist Claude plugin are documented here. The
project follows Semantic Versioning. Every published content change needs a
manifest version bump because Claude uses that version as its update cache key.

## 1.3.0

- `clinic-administration` 1.3.0, for the connector's website tools: it reads
  and changes the practice's website settings (colours, social links,
  WhatsApp number, external website, online booking window), which show on
  the public site at once, and reads and edits the files of a website builder
  draft as checkpoints it can go back to. A draft is not the public site,
  and cannot be published yet.

## 1.2.0

- `clinic-administration` 1.2.0: an appointment still to schedule
  (`TO_SCHEDULE`) is a visit the dentist planned without a date. A patient's
  `list_appointments` lists these first, with no times, and
  `reschedule_appointment` books one at the length the dentist planned, after
  the user confirms the day and time.

## 1.1.0

- `clinic-administration` 1.1.0, for connector 0.2.0: it books, moves and
  cancels appointments, adds patients and changes their name, phone, email or
  language, and sets stock counts, each after the user confirms. A patient is
  found only by the name the user gives (`find_patient`, at most five
  matches) and appointments are listed for one patient or one day.
- The skill confirms every write, tells a read-only connection to reconnect,
  and keeps patient lists, contact details, the procedures booked and every
  clinical record out of reach.

## 0.2.1

- `clinic-administration` 1.0.1: the tool table now says when to use each
  tool in the words dental teams ask with, matching the connector's rewritten
  tool descriptions. Schedule counts are documented as including canceled
  appointments, and availability as the practice's own online-booking window.
- Same eight read-only tools and the same administrative-only boundary.

## 0.2.0

- Add portable Agent Plugins 1.0 manifests, Gemini CLI and Antigravity adapters, and repository agent instructions.
- Keep every adapter on the existing read-only OAuth MCP endpoint and canonical product skill.

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
