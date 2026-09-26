# PiRogue Tool Suite: workshop curriculum

A reusable, facilitator-ready training package for the PiRogue Tool Suite, built for human rights organizations and digital security trainers. Four modules follow one investigation, case **LAB-001**, from a lure SMS to a shared report. Delivers in person or online.

## Modules

| # | Title | Deck |
|---|---|---|
| 1 | PTS setup and configuration | `day1-setup-and-configuration.pdf` |
| 2 | Network interception, capture and analysis | `day2-network-interception-capture-analysis.pdf` |
| 3 | PTS ecosystem, Colander, integrations | `day3-ecosystem-colander-integrations.pdf` |
| 4 | Dynamic analysis of Android apps with Octopus | `day4-dynamic-analysis-octopus.pdf` |

Each module is 3 hours with a break. The decks cover PiRogue (capture, fleet), Colander (cases, evidence, sharing), and Octopus (dynamic Android app analysis).

## What's in the package

```
day1..day4 .md / .pdf      the four decks (Marp Markdown + rendered PDF)
CHANGELOG.md               provenance, technical notes, what was tested
ATTRIBUTION.md             credits and license guidance
remote-delivery.md         running the workshop online

facilitator/
  facilitator-guide.md     how to run the workshop, per-module notes
  lab-setup.md             bill of materials, setup order, rehearsal checklist
  malware-handling.md      safe handling of the real training sample
  train-the-trainer.md     adapting and delivering it onward
  (the case solution and the exercise answer key are distributed to
   facilitators separately, not in this public repository)

handouts/                  give to trainees
  cheatsheet-module1..4.md one page per module
  exercises.md             exercise sheets for modules 2 and 4

lab-kit/
  make-lab-kit.py          generates a consistent LAB-001 case for your domain
  README.md                what it produces and how to deploy it
  example-output/          a generated example (domain training.example.org)

assets/                    the two diagrams used in the decks
```

## Quick start for a facilitator

1. Read `facilitator/facilitator-guide.md` and `facilitator/lab-setup.md`.
2. Stand up the infrastructure (Colander, a VPN PiRogue, the lab server).
3. `cd lab-kit && python3 make-lab-kit.py --domain <your domain>`, then deploy the pieces it generates.
4. Rehearse against the checklist in `lab-setup.md`.
5. Render the decks with speaker notes for yourself:
   ```bash
   npx @marp-team/marp-cli day4-dynamic-analysis-octopus.md --pdf --pdf-notes -o day4-notes.pdf
   ```
6. Deliver. Hand trainees the cheat sheets and exercises, keep the facilitator materials.

> The case solution and exercise answer key are not in this public repository. Facilitators receive them separately so the exercises stay useful.

## Re-render the decks

```bash
npx @marp-team/marp-cli day1-setup-and-configuration.md --pdf --allow-local-files
# ...same for day2, day3, day4
```

## The case, and the sample

LAB-001 uses a **real** malicious Android sample (a trojanised Wire, from the PTS training samples). The lure SMS and the network beaconing are simulated by the lab kit so the case is reproducible; the sample is real so evidence handling is real. Read `facilitator/malware-handling.md` before you start.

## Credits

Built on the PiRogue Tool Suite by Defensive Lab Agency (`pts-project.org`), and its documentation at `docs.pts-project.org`. The training sample and the guides it draws on are published by the PTS project.
