# Organisation profile page

Date: 2026-11-16

## Problem / Motivation

Pactolus Microelectronics is the new home of the work that began as the Open Memory Initiative. The organisation was created on 2026-11-16 and had no profile page, so a visitor saw two repositories and no statement of what the project is, what exists and what does not.

The old organisation's page also made two claims that no longer hold: it called the DDR4 schematic "complete", and it listed `spdr` as upcoming. The new page had to state the real status from the start.

## What Changed

| File | Change |
|---|---|
| `profile/README.md` | New. The public profile page GitHub shows on the organisation. |
| `docs/implementations/2026-11-16-organisation-profile.md` | New. This record. |

## Implementation Approach

The page follows the pattern of the maintainer's other organisations: a name, one line under it, a short opening that ties the name's story to the work, a table of programs, and a list of working rules.

Every status claim in the programs table links to the artifact that backs it:

- The DDR4 schematic's rule-check result links to `exports/erc.json` in `ddr4-udimm`.
- The `spdr` release links to crates.io, and its validation claim links to `docs/validated-against.md` in `spdr`.
- The Silicon program is stated as not started, with no design, because none exists.

## Design Decisions

- **A new organisation, not a rename.** The old organisation stays as an archive so that existing links to it keep showing the work. The page therefore says it continues the Open Memory Initiative and links to the archive.
- **Status wording is "schematic only", not "schematic complete".** The schematic passes its rule check, but decoupling, termination and the SPD device are open items, and there is no layout or board.
- **Aims are written as aims.** The first planned silicon contribution is named, and the same row says no design exists yet.
- **No banner.** There is no Pactolus mark yet. The old banner belongs to the archive and is not reused.

## Verification

1. Open https://github.com/Pactolus-Microelectronics and confirm the page renders under the organisation name.
2. Follow each link in the programs table and confirm it resolves:
   - `ddr4-udimm` and its `exports/erc.json`, which reports 0 violations
   - `spdr`, its crates.io page, and `docs/validated-against.md`, which names one module
3. Confirm the page makes no claim of a layout, a board, or any fabricated chip.

## Related Docs

- `ddr4-udimm`: https://github.com/Pactolus-Microelectronics/ddr4-udimm
- `spdr`: https://github.com/Pactolus-Microelectronics/spdr
- The archive: https://github.com/The-Open-Memory-Initiative-OMI
