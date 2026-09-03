# UBC Rocket, 2025/2026

Hands-on rocketry from my first year in engineering at UBC: mechanical design and CAD,
composite manufacturing, avionics integration, and energetic (separation charge) testing.

Two projects live here. One I built with a sub-team, one I built alone in five days.

---

<table>
<tr>
<td width="50%"><a href="big-mach/"><img src="big-mach/media/build/finished-airframe-painted.jpg" alt="The Big Mach, finished and painted"></a></td>
<td width="50%"><a href="star-raptor/"><img src="star-raptor/media/shoulder-carry-scale.jpg" alt="Star Raptor, shoulder carried for scale"></a></td>
</tr>
<tr>
<td><h3><a href="big-mach/">The Big Mach</a></h3>
A UBC Rocket test vehicle, built so the team could fly a new reefing parachute system and an in-house avionics stack on hardware it controlled end to end.
<br><br>
<b>My role:</b> full-vehicle CAD and assembly, 3D printing, composite layup, avionics bay integration, separation charge design and ground testing.
<br><br>
<b>Scale:</b> 146 cm long, 10.7 cm diameter, 7.7 kg with motors, L935 motor, simulated Mach 1.03 and 3.06 km apogee.
</td>
<td><h3><a href="star-raptor/">Star Raptor</a></h3>
My own certification rocket, designed and built solo to earn a Canadian Association of Rocketry certification.
<br><br>
<b>My role:</b> everything. Design, CAD, printing, assembly, recovery packing, flight.
<br><br>
<b>Scale:</b> roughly 1 m, printed nose cone and five-fin can, motor-ejection recovery, no onboard electronics.
</td>
</tr>
</table>

---

## What I actually did

I joined UBC Rocket as a first-year student and was put on the test-rocket sub-team.
The job of that team is to fly other people's new hardware (a reefing parachute system
and a custom avionics stack) on a vehicle we design and build ourselves. So most of my
time went into being the person who takes a requirement from another sub-team and turns
it into geometry, a printed part, a laid-up tube, or a wired-up bay.

Concretely, across the two projects:

| Area | What that meant here |
|---|---|
| **CAD** | Owned and assembled the full `FullAssembly` SolidWorks model of the Big Mach: nose cone sections, body tubes, couplers, bulkheads, centering rings, fin pattern. Modelled Star Raptor's printed parts from scratch. |
| **Simulation** | OpenRocket models for stability and trajectory, used to size the airframe and check margin before committing to a layup. |
| **Manufacturing** | 3D printing (including a PA6GF glass-filled-nylon nose cone), fiberglass wet layups, composite fin work, paint and finishing. |
| **Avionics integration** | Physically fitting the flight computer stack, battery and charge wiring into the bay, and keeping it serviceable by the sub-team that owned it. |
| **Energetics and testing** | Sizing and massing black powder separation charges, wiring e-matches, and firing them over a remote link. |

The avionics bay component (`EDR_AVBAY_DESIGN`) came from the avionics sub-team. The
rest of the assembly and all the mating is mine. Where a claim rests on memory rather than
on something in this repository, I have said so in place rather than dressing it up.

---

## The one that shows the most

The separation charge ground test. Recovery depends on a black powder charge splitting
the airframe at the right moment, and the charge mass is not something you calculate
once and trust. You mass it out, fire it, and watch.

![Separation charge ground test](big-mach/media/testing/separation-charge-test.gif)

*Ground test of the recovery separation charge, fired remotely. Full detail in the
[Big Mach testing section](big-mach/README.md#separation-charge-testing).*

---

## Navigation

| | |
|---|---|
| **[The Big Mach](big-mach/README.md)** | Full engineering case study: design, manufacturing, avionics, testing, launch |
| **[Star Raptor](star-raptor/README.md)** | Solo five-day build, and the scoping decisions that made it possible |
| **[Design media](big-mach/media/design/)** | OpenRocket and SolidWorks screenshots |
| **[Build media](big-mach/media/build/)** | Composite layup, printed parts, avionics bay, finished airframe |
| **[Testing media](big-mach/media/testing/)** | Separation charge ground test, charge mass measurement |
| **[Full CAD assembly](https://github.com/BentoOre0/2025-2026-UBC-ROCKET-work/releases/tag/cad-v1)** | The complete SolidWorks assembly, 169 MB, hosted as a release asset |

```text
big-mach/
  README.md
  media/
    design/     OpenRocket + SolidWorks screenshots
    build/      composite layup, printed parts, avionics bay, finished airframe
    testing/    separation charge ground test, charge mass measurement
    launch/     launch site photos and video
star-raptor/
  README.md
  media/        printed fin can, recovery packing, assembled vehicle
```

## The full CAD assembly

The complete SolidWorks assembly is 169 MB, which is too large to sit usefully in a Git
tree, so it is published as a
**[release asset](https://github.com/BentoOre0/2025-2026-UBC-ROCKET-work/releases/tag/cad-v1)**
instead. Start at `FullAssembly.SLDASM`. It needs SolidWorks to open, and the
screenshots in `big-mach/media/design/` are taken from it if you just want to look.

---

*Jeremy Aidan Yu, UBC Engineering*
