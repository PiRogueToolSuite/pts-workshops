<div align="center">
<img width="60px" src="https://pts-project.org/android-chrome-512x512.png">
<h1>PiRogue Tool Suite training curriculum</h1>
<p>
A four-module workshop that teaches PiRogue, Colander and Octopus through one investigation, for human rights organizations and digital security trainers.
</p>
<p>
<a href="https://pts-project.org">Website</a> | 
<a href="https://pts-project.org/docs/">Documentation</a> | 
<a href="https://discord.gg/qGX73GYNdp">Support</a>
</p>
</div>

## Modules

The four modules follow one investigation, case **LAB-001**, from a lure SMS to a shared report. Each is 3 hours with a break.

| # | Title | Slides |
|---|---|---|
| 1 | PTS setup and configuration | [`slides/day1-setup-and-configuration.pdf`](slides/day1-setup-and-configuration.pdf) |
| 2 | Network interception, capture and analysis | [`slides/day2-network-interception-capture-analysis.pdf`](slides/day2-network-interception-capture-analysis.pdf) |
| 3 | PTS ecosystem, Colander, integrations | [`slides/day3-ecosystem-colander-integrations.pdf`](slides/day3-ecosystem-colander-integrations.pdf) |
| 4 | Dynamic analysis of Android apps with Octopus | [`slides/day4-dynamic-analysis-octopus.pdf`](slides/day4-dynamic-analysis-octopus.pdf) |

The decks cover PiRogue (capture, fleet), Colander (cases, evidence, sharing) and Octopus (dynamic Android app analysis).

## What's in this repository

```
day1..day4 .md      the four decks, Marp Markdown (source)
slides/             the four decks rendered to PDF
assets/             the two diagrams used in the decks
LICENSE
```

## Render the decks

The PDFs in `slides/` are built from the Markdown with [Marp](https://marp.app):

```bash
npx @marp-team/marp-cli day1-setup-and-configuration.md --pdf --allow-local-files -o slides/day1-setup-and-configuration.pdf
# ...same for day2, day3, day4
```

Add `--pdf-notes` to include the presenter notes (demo scripts and expected answers) as PDF annotations.

## The case, and the sample

LAB-001 is built around a **real** malicious Android sample (a trojanised Wire, from the PTS training samples). The lure SMS and the network beaconing described in the decks are simulated so the case is reproducible; the sample is real so evidence handling is real. Treat the sample as live malware: run it only on a wiped, dedicated device on an isolated network, never on a personal or work machine.

## Credits

Built on the [PiRogue Tool Suite](https://pts-project.org) by Defensive Lab Agency, and its [documentation](https://pts-project.org/docs/). The training sample and the guides these slides draw on are published by the PTS project.

## Community

[GitHub](https://github.com/PiRogueToolSuite) | 
[Mastodon](https://infosec.exchange/@pts) | 
[X](https://x.com/PiRogueTools) | 
[Discord](https://discord.gg/qGX73GYNdp) | 
[Open Collective](https://opencollective.com/pts)
