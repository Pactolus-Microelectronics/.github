# Pactolus Microelectronics

*Open hardware, tested before it is trusted.*

In the myth, King Midas washed his golden touch into the river Pactolus, and from then on the gold lay in sand that anyone could pan. The Lydians who gathered it trusted none of it until it had been tested on a touchstone. Chips are made of sand. We design memory, tools and chips in the open, and we publish what is needed to test every claim we make.

This is the continuation of the [Open Memory Initiative](https://github.com/The-Open-Memory-Initiative-OMI), whose organisation remains as the archive of the work up to 2026. It is the work of a single maintainer, [Mert Efe Şensoy](https://github.com/mertefesensoy), not a consortium.

## Programs

| Program | In the story | What it is | Where it stands today |
|---|---|---|---|
| **Memory** · [`ddr4-udimm`](https://github.com/Pactolus-Microelectronics/ddr4-udimm) | The Treasury | A reference design for an 8 GB DDR4 UDIMM, built from public sources only, with the reasoning written down. | **Schematic only.** It passes the electrical rule check with [0 violations](https://github.com/Pactolus-Microelectronics/ddr4-udimm/blob/main/exports/erc.json) and has a generated netlist, parts list and PDF. Decoupling, termination and the SPD device are open items. There is no board layout and no board. |
| **Tooling** · [`spdr`](https://github.com/Pactolus-Microelectronics/spdr) | The Touchstone | A read-only decoder and linter for DDR5 SPD data, written in Rust. It checks a module's timing and structure, not just its checksum. | **Released:** version 0.1.2 on [crates.io](https://crates.io/crates/spdr). It covers unbuffered modules and has been [confirmed against one real module](https://github.com/Pactolus-Microelectronics/spdr/blob/main/docs/validated-against.md) so far. |
| **Silicon** | The River | Chips designed in the open and fabricated on shared runs that anyone can buy into. | **Not started.** The first planned contribution is a dense memory test array, with its retention time measured. No design exists yet. |

## How we work

- **The open alternative comes first.** When something is behind an NDA or priced out of reach, we map the wall and build what can be built in the open.
- **Pass criteria are written down before the work is run.**
- **Every number we publish has a recorded source.**
- **Aims are stated as aims.** Until something is built and measured, we say what we are building, not what it achieves.
- **Results that did not work are published with the same care as those that did.**
- **No NDA, leaked or proprietary material, ever.**

## Contributing

Open an issue or a pull request on the relevant repository. The most useful help right now:

- **Design review of the DDR4 schematic.** Errors and gaps in the schematic, the 288-pin pin map and the documents.
- **SPD dumps from real DDR5 modules,** so `spdr` can be checked against more than one.

An honest "I can do this part but not that one" is worth more than a general offer.

## Licences

Hardware is under CERN-OHL-S-2.0, code under Apache-2.0 and documents under CC-BY-SA-4.0, as stated in each repository.

> If it can't be inspected, it can't be trusted.
