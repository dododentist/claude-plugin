# DodoDentist plugin for Claude

Read-only clinic administration inside Claude. This plugin connects to the
hosted DodoDentist MCP and teaches Claude how to review clinic metadata,
bookable availability, provider display names, procedure catalogs,
non-identifying calendar blocks and aggregate schedule counts.

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
- “List this week's non-appointment calendar blocks.”

## Privacy and safety

The public connector does not expose patient records or contact details,
individual appointment records, diagnoses, treatment information, notes,
anamnesis, tooth charts, images or other clinical data. It is read-only and
does not make diagnoses, treatment recommendations, urgency decisions or
other medical decisions.

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

- `clinic-administration` — the single skill covering all eight read-only
  connector tools, identifier/pagination rules, aggregate-count semantics,
  privacy boundary and unsupported clinical/write requests.
- `.mcp.json` — the hosted DodoDentist OAuth connector.

## Support

`info@dododentist.com` ·
[www.dododentist.com](https://www.dododentist.com/)

## License

Apache-2.0. See [LICENSE](./LICENSE).
