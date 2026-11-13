# DodoDentist plugin for Claude

Dental-practice scheduling inside Claude. This plugin connects to the hosted
DodoDentist MCP and teaches Claude how to check availability, providers,
treatment prices, calendar blocks, daily appointment counts and stock, find a
patient you name and their appointments, and, with your confirmation, book,
move and cancel appointments, add patients and update their contact details,
and correct stock counts.

## Requirements

A DodoDentist account with access to the intended organization. The plugin
connects to `https://mcp.dododentist.com/mcp` over OAuth. There is no API key
to copy and nothing to self-host.

## What you can ask

- “List my clinics and show the administrative overview for the first one.”
- “Show aggregate schedule counts for my first clinic for the next seven
  days.”
- “Show bookable availability and provider display names.”
- “List the procedure catalog with prices.”
- “Book Sample Patient 03 for a cleaning next Monday at 10:00.”
- “Move Sample Patient 01's appointment to Thursday afternoon.”
- “Add a new patient called Robin Example.”

## Privacy and safety

The connector finds a patient only by the name you give and never lists
patients. It never returns contact details, notes, the procedures booked,
diagnoses, treatment information, anamnesis, tooth charts, images or other
clinical data. Every write asks for your confirmation first; nothing is
deleted. It does not make diagnoses, treatment recommendations, urgency
decisions or other medical decisions.

The DodoDentist account you authorize determines which organization Claude can
access. See the
[privacy policy](https://www.dododentist.com/en/privacy-policy/) and
[connector documentation](https://www.dododentist.com/developers/#mcp).

## Install

The source repository and directory listing are separate publication steps.
Once the plugin is accepted into Claude's community directory, install it using
the directory instructions shown by Claude. Do not treat this source artifact
as proof that the public listing is live.

## Contents

- `clinic-administration` — the single skill covering all seventeen
  connector tools, the booking workflow, identifier and version rules, the
  patient and clinical boundary and unsupported requests.
- `.mcp.json` — the hosted DodoDentist OAuth connector.

## Support

`info@dododentist.com` ·
[www.dododentist.com](https://www.dododentist.com/)

## License

Apache-2.0. See [LICENSE](./LICENSE).

## Cross-host package

The repository root is an [Agent Plugins](https://agent-plugins.org/) package: `plugin.json`, `mcp.json`, and `skills/clinic-administration/SKILL.md` install the hosted connector and its workflow together. Claude uses `.claude-plugin/plugin.json` and `.mcp.json`; Gemini CLI uses `gemini-extension.json`; Antigravity uses `com.google.antigravity/`. All adapters use https://mcp.dododentist.com/mcp and the product OAuth flow. No credential is bundled.

Clinic administration only. Do not request patient identities, individual appointments, clinical records, or medical decisions.
