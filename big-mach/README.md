# The Big Mach

![The finished airframe, painted and named](media/build/finished-airframe-painted.jpg)

*The Big Mach at the end of the build, in the UBC Rocket workshop. The bare grey
PA6GF nose cone on the right is a spare print of the same part.*

---

## What it is

The Big Mach is a UBC Rocket **test vehicle**. It exists so that two pieces of new
hardware, a reefing parachute recovery system and an in-house avionics stack, could be
flown and characterised on something the team controlled end to end, rather than risking
them on the competition rocket.

That framing drives every design decision on the vehicle. It has to fly high and fast
enough to be a meaningful test, it has to separate reliably to give the recovery system
a chance to work, and the avionics bay has to be accessible enough that another sub-team
can service their own hardware inside it.

From the OpenRocket model (`FINAL_L935_BIG_MACH_with_centering rings.ork`):

| Parameter | Value |
|---|---|
| Length | 146 cm |
| Max diameter | 10.7 cm |
| Mass, no motors | 5176 g |
| Mass, with motors | 7718 g |
| Motor configuration | `3147L935-P` (L-class, 935 N average) |
| Stability margin | 1.5 cal (11%), CG 79.2 cm / CP 95.3 cm |
| Simulated apogee | 3064 m |
| Simulated max velocity | 347 m/s, **Mach 1.028** |
| Simulated max acceleration | 195 m/s² |

The name is not decoration: the simulation puts the vehicle just over Mach 1, which is
what the airframe and fin design had to survive.

<table>
<tr>
<td width="50%"><img src="media/design/openrocket-3d-view.png" alt="OpenRocket 3D view"></td>
<td width="50%"><img src="media/design/openrocket-side-view.png" alt="OpenRocket side view with CG and CP marked"></td>
</tr>
<tr>
<td colspan="2"><em>OpenRocket model. The side view shows the internal stack (nose cone, avionics bay with drogue and main parachutes either side of the avionics stack, coupler, then the motor body tube) and the CG/CP markers used to check the stability margin.</em></td>
</tr>
</table>

---

## My role

I was one of three people on the test-rocket sub-team. The sub-team designed and built
the vehicle; the recovery, avionics, embedded software and composites sub-teams supplied
the payload hardware and the expertise. A lot of the job was translation: taking a
requirement from another sub-team and turning it into something that could actually be
printed, laid up, or bolted in.

**What was mine:**

- **The full-vehicle SolidWorks assembly.** I built and mated `FullAssembly`: nose cone
  sections (`NoseconeTip`/`NoseConeMiddle`/`NoseconeBottom`), avionics bay body tube,
  motor body tube, inner tube, bulkheads, centering rings, the fin pattern
  (`LocalCirPattern1`) and the bottom plate.
- **OpenRocket modelling** for stability and trajectory.
- **3D printing.** The majority of the sub-team's printed prototypes and flight parts
  went through me, including the PA6GF (glass-filled nylon) nose cone.
- **Fiberglass wet layup** for the custom body tubes.
- **Avionics bay integration.** Fitting the flight computer stack, battery and charge
  wiring into the bay.
- **Separation charge design and ground testing.** Sizing and massing black powder
  charges, wiring e-matches, and firing them over a remote link.
- **Painting and finishing.**

**What was not mine:**

- The **avionics bay internal design** (`EDR_AVBAY_DESIGN` in the assembly tree) came
  from the avionics sub-team. I integrated it and built the structure around it. I did
  not design the flight computer or its sled.
- The **reefing parachute system** is the recovery sub-team's design. The Big Mach was
  the vehicle that carried it.
- The **composite layups and fin fabrication were done with the team.** I did the work
  alongside more experienced members, not alone. The photo captions in `media/build/`
  reflect this distinction as I recorded it at the time.

---

## Design

<table>
<tr>
<td width="50%"><img src="media/design/solidworks-full-assembly.png" alt="SolidWorks full assembly"></td>
<td width="50%"><img src="media/design/solidworks-sectioned-view.png" alt="SolidWorks sectioned view showing internal avionics"></td>
</tr>
<tr>
<td colspan="2"><em>Left: the assembled vehicle in SolidWorks, with the component tree showing the parts I mated. Right: the same model sectioned, exposing the avionics stack inside the bay. This is the view that mattered when checking that the avionics sub-team's hardware and the recovery hardware could physically coexist in one bay.</em></td>
</tr>
</table>

![Nose cone and avionics bay detail](media/design/solidworks-nosecone-avbay.png)

*Nose cone and avionics bay, hidden-line view. The avionics bay is the shoulder section
behind the cone; the recovery hardware packs either side of the electronics.*

> **Full assembly available.** The complete SolidWorks assembly (37 files, 205 MB
> uncompressed) is published as a
> [release asset](https://github.com/BentoOre0/2025-2026-UBC-ROCKET-work/releases/tag/cad-v1).
> Start at `FullAssembly.SLDASM`. The avionics bay, backplane, connector and pyro board
> assemblies inside it belong to the avionics sub-team; the airframe and the top-level
> mating are mine.

---

## Manufacturing

<table>
<tr>
<td width="50%"><img src="media/build/pa6gf-nosecone-fiberglass-tube.jpg" alt="PA6GF printed nose cone next to fiberglass body tube"></td>
<td width="50%"><img src="media/build/composite-tube-carbon-fins.jpg" alt="Composite body tube and carbon fibre fin"></td>
</tr>
<tr>
<td colspan="2"><em>Left: the PA6GF nose cone I printed, next to the green fiberglass body tube. PA6GF (glass-filled nylon) was chosen over a standard print material because the cone sees the highest aerodynamic heating and stagnation pressure on the vehicle. Right: the composite airframe and a carbon fibre fin during fin fabrication: fiberglass and phenolic in the tube, carbon in the fins.</em></td>
</tr>
</table>

![Aft end of the airframe, looking down the body tube](media/build/aft-centering-ring-detail.jpg)

*Looking down the airframe at the motor tube, held concentric inside the body tube by a
centering ring, with printed blocks spaced around the annulus.*

### The layup diameter mismatch

The most instructive manufacturing problem on this project was a **diameter mismatch on
the first fiberglass wet layup**. The tube we produced did not come out at a diameter
that mated correctly with the parts it had to meet, so the layup had to be reworked and
re-run rather than salvaged.

The lesson that actually stuck is that on a wet layup the mandrel is not the only thing
setting the finished diameter. Layer count, resin uptake and how hard the tube is
compacted all stack into the final wall thickness, and a coupler fit that is toleranced
tightly on paper has very little room to absorb that. The fix was to treat the layup
schedule as something to be designed against a target *finished* inside diameter and
verified, rather than assumed from the mandrel.

> **Evidence note.** I have no photograph of the mismatched tube itself, and no written
> record of the measured error. This section is from memory. The composite work that is
> documented here is the successful second attempt and the fin fabrication.

---

## Avionics integration

![Avionics bay stack](media/build/avionics-bay-integration.jpg)

*The avionics bay stack out of the airframe: the flight computer boards on their printed
sled, screw-terminal blocks for the charge wiring, power leads and connectors, and the
battery strapped below. My work here was the physical integration: getting this stack,
its battery and its charge wiring to fit, mount and route inside the bay, and remain
serviceable by the avionics sub-team.*

---

## Separation charge testing

Recovery on this vehicle depends on a black powder charge separating the airframe at the
right moment. Too little and the sections do not part; too much and you damage the
airframe or the parachute you are trying to deploy. The charge mass is not something you
can confidently calculate and walk away from. It gets massed out, fired, and watched.

![Separation charge ground test](media/testing/separation-charge-test.gif)

*Ground test, trimmed to the event. The airframe sits horizontally on the pavement, the
charge fires, and the sections separate in a puff of smoke. Fired remotely, triggered
from a phone over a wireless link to the firing board and out to the e-match. Full
resolution clip: [`separation-charge-test.mp4`](media/testing/separation-charge-test.mp4).*

![Charge mass on a precision scale](media/testing/charge-mass-measurement.jpg)

*Massing a charge on a jeweller's scale during test preparation. The reading is 2.494 g.
This is the measurement step the section above is about: the charge mass is set on a
scale, not estimated.*

**What I did:** designed and ground-tested the separation charges, using an **Eggtimer
Quantum** as the firing system and **e-match** ignition, iterating charge mass across
**three separation tests** until the recovery system deployed reliably. I worked with the
team leads to estimate the starting charge requirement, and debugged power and
electronics faults that came up during testing.

> **Evidence note, read this before quoting numbers.** The three-test count, the Eggtimer
> Quantum, the e-match ignition and the charge-mass iteration are from my own recollection
> of the test campaign. The photograph above evidences **one** charge being massed at
> 2.494 g, but this repository holds **no test log and no per-test results**, so I cannot
> say from the repo alone whether 2.494 g was a starting point, an intermediate step, or
> the value that flew. I have deliberately not invented numbers to fill that gap. If you
> want the specifics, ask me and I will tell you what I remember and flag what I am unsure
> of.

---

## Launch

Launching a high-power vehicle out of Vancouver means driving it to a site that will take
it. For this campaign that was Pasco, Washington: 603 km and about six and a quarter
hours from the Hennings Building on campus, across the border.

<table>
<tr>
<td width="50%"><img src="media/launch/launch-site-drive.jpg" alt="Route from UBC to Pasco, Washington"></td>
<td width="50%"><img src="media/launch/launch-site-vehicle-pose.jpg" alt="With the vehicle at the launch site"></td>
</tr>
<tr>
<td><em>The drive. UBC Hennings Building to Pasco, WA: 603 km, 6 hr 14 min, one border crossing.</em></td>
<td><em>With the Big Mach at the launch site.</em></td>
</tr>
</table>

![At the launch site with the sub-team](media/launch/launch-site-team.jpg)

*At the launch site with the sub-team and team lead. It was extremely windy, which is the
kind of thing that decides whether a launch window happens at all. Video from the same
day: [`launch-site-team-video.mp4`](media/launch/launch-site-team-video.mp4).*

---

## Evidence index

Because this is a portfolio repository, here is an honest mapping from each claim to what
actually backs it up.

| Claim | Evidence in this repo | Status |
|---|---|---|
| Vehicle is called "The Big Mach" | Name painted on the airframe; OpenRocket filename | **Verified** |
| Vehicle geometry, mass, stability, trajectory | OpenRocket screenshots (`media/design/`) | **Verified** |
| Dual-deploy recovery (drogue + main) around an avionics stack | OpenRocket component tree, sectioned CAD view | **Verified** |
| I assembled the full SolidWorks model | Assembly tree in `media/design/`; full assembly in the [release](https://github.com/BentoOre0/2025-2026-UBC-ROCKET-work/releases/tag/cad-v1) | **Verified** |
| Avionics bay design came from the avionics sub-team | `EDR_AVBAY_DESIGN` component in the tree; my own build notes | **Verified** |
| PA6GF nose cone, fiberglass tube, carbon fins | Build photos (`media/build/`) | **Verified** |
| Avionics stack physically integrated into the bay | `media/build/avionics-bay-integration.jpg` | **Verified** |
| Remote-fired separation charge testing | `media/testing/separation-charge-test.gif` and `.mp4` | **Verified** |
| Charges were massed on a precision scale | `media/testing/charge-mass-measurement.jpg`, reading 2.494 g | **Verified** |
| Which charge mass flew, and how it changed across tests | No test log in repo | **From memory, not evidenced here** |
| Three separation tests | No test log in repo | **From memory, not evidenced here** |
| Eggtimer Quantum + e-match firing system | Firing behaviour visible in video; hardware not identifiable in frame | **Partly evidenced** |
| Fiberglass layup diameter mismatch and rework | None | **From memory, not evidenced here** |
| Majority of the sub-team's prototypes printed by me | None | **From memory, not evidenced here** |
| Three-person sub-team | Launch site photos | **Consistent, not conclusive** |

---

## What I took away from it

- **Ground testing energetics is not optional.** The charge mass that "should" work and
  the charge mass that reliably separates a specific airframe with a specific shear pin
  and seal arrangement are different numbers, and the only honest way to close that gap
  is to fire it and watch.
- **Composite processes have tolerances that CAD does not.** The diameter mismatch cost a
  rework because the layup was treated as a way to realise a drawing rather than as a
  process with its own variation.
- **Integration is a design constraint, not a final step.** The bay had to be serviceable
  by people who were not me, working on hardware I did not design. Designing for someone
  else's access changed the geometry.
