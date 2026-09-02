# UBC Rocket — 2025/2026

Hands-on rocketry work from my first year in engineering at UBC: mechanical design and
CAD, composite manufacturing, avionics integration, and energetic (separation charge)
testing.

Two projects live here.

| | [**The Big Mach**](big-mach/) | [**Star Raptor**](star-raptor/) |
|---|---|---|
| **What** | UBC Rocket test vehicle — a supersonic airframe built to fly a new reefing parachute system and in-house avionics | My own certification rocket, designed and built solo |
| **Team** | Three-person test-rocket sub-team, drawing on the avionics, embedded software, recovery and composites sub-teams | Just me |
| **My role** | Full-vehicle CAD and assembly, 3D printing, composite layup, avionics bay integration, separation-charge design and testing | Everything |
| **Scale** | 146 cm, 10.7 cm diameter, 7.7 kg wet, L935 motor, simulated Mach 1.03 / 3.06 km apogee | ~1 m, motor-ejection recovery, no electronics |
| **Timeline** | Sub-team project across the year | Five-day sprint |

---

## What I actually did

I joined UBC Rocket as a first-year student and was put on the test-rocket sub-team.
The job of that team is to fly other people's new hardware — a reefing parachute
system and a custom avionics stack — on a vehicle we design and build ourselves. That
meant most of my time went into being the person who takes a requirement from another
sub-team and turns it into geometry, a printed part, a laid-up tube, or a wired-up bay.

Concretely, across the two projects:

- **CAD** — I owned and assembled the full `FullAssembly` SolidWorks model of the Big
  Mach (nose cone sections, body tubes, couplers, bulkheads, centering rings, fin
  pattern), and modelled Star Raptor's printed parts from scratch. The avionics bay
  component (`EDR_AVBAY_DESIGN`) came from the avionics sub-team; the rest of the
  assembly and all the mating is mine.
- **Simulation** — OpenRocket models for stability and trajectory, used to size the
  airframe and check the margin before committing to a layup.
- **Manufacturing** — 3D printing (including a PA6GF glass-filled-nylon nose cone),
  fiberglass wet layups, and composite fin work.
- **Avionics integration** — physically fitting the flight computer stack, battery and
  charge wiring into the bay.
- **Energetics and testing** — designing and ground-testing the black powder separation
  charges that deploy the recovery system, fired over a remote link.

Where the evidence in this repository supports a claim, I've linked it. Where it
doesn't, I've said so rather than dressing it up — see the evidence tables in each
project README.

---

## Repository layout

```text
big-mach/
  README.md
  media/
    design/     OpenRocket + SolidWorks screenshots
    build/      composite layup, printed parts, avionics bay, finished airframe
    testing/    separation charge ground test (video)
    launch/     launch site
star-raptor/
  README.md
  media/        printed fin can, recovery packing, assembled vehicle
```

## A note on what is not here

The full SolidWorks assembly is a ~177 MB archive and is deliberately not committed —
it is too large to be useful in a Git repository and needs SolidWorks to open anyway.
The screenshots in `big-mach/media/design/` are taken from it. I'm happy to share the
archive directly.

---

*Jeremy Aidan Yu · UBC Engineering*
