# UBC Rocket Portfolio Repository Redesign

You are working on my GitHub repository:

`https://github.com/BentoOre0/2025-2026-UBC-ROCKET-work.git`

Your job is to comprehensively improve the repository as a **public engineering portfolio**, with the goal of making someone who discovers the repository interested enough to explore the projects and understand what I actually built and contributed.

This is not simply a README cleanup. Treat this as a **portfolio presentation and documentation redesign**.

## 1. First: inspect before modifying

Start by thoroughly inspecting the existing repository.

Understand:

* The current directory structure
* `big-mach/`
* `star-raptor/`
* Existing READMEs
* Existing images/media
* CAD files, screenshots, videos, models, documentation, and other artifacts
* Git history where useful
* Any information already documented about my contributions

Do not immediately rewrite everything.

First form an understanding of:

1. What each project is
2. What I personally contributed
3. What evidence exists for those contributions
4. What media is available
5. What information is missing
6. What would make the repository visually compelling to someone browsing my engineering portfolio

If something is unclear, flag it rather than inventing information.

---

## 2. Overall goal

Redesign the repository so that it feels like a **serious engineering portfolio**, rather than a generic project dump.

The repository should quickly communicate:

> I designed, built, integrated, tested, and worked on real rocket hardware.

A visitor should be able to understand the projects within roughly 30 seconds, then progressively dive deeper if they are interested.

Prioritize:

* Visual presentation
* Engineering substance
* Clear storytelling
* Evidence of hands-on work
* My personal contributions
* Easy navigation
* Concise but interesting documentation

Do not make the documentation artificially corporate or overly verbose.

Keep my voice reasonably natural and personal.

---

## 3. Remove em dashes

This is an explicit formatting requirement.

**Do not use em dashes (`—`) anywhere in the rewritten documentation.**

Use commas, parentheses, colons, semicolons, or separate sentences instead.

Search the final documentation for `—` and remove every occurrence.

---

## 4. Redesign the root README

Completely rethink the root `README.md`.

The root README should function as the **landing page for my rocketry portfolio**.

It should contain:

### Hero / introduction

A strong opening section that immediately establishes:

* UBC Rocket
* 2025/2026
* What these projects are
* My role as an engineering student
* The fact that these are real physical rocket projects

Make this visually appealing using Markdown-supported formatting.

### Project showcase

Create a visually interesting section introducing:

#### The Big Mach

Give it:

* A representative image
* One-sentence description
* My role
* Key technical characteristics
* Link to the dedicated project README

#### Star Raptor

Give it:

* A representative image
* One-sentence description
* My role
* Key technical characteristics
* Link to the dedicated project README

Prefer images that immediately communicate what the project looks like.

### Engineering skills / areas

Include a concise section showing the types of engineering work represented in the repository, such as:

* CAD
* SolidWorks
* OpenRocket
* Composite manufacturing
* 3D printing
* Avionics integration
* Embedded systems
* Recovery systems
* Mechanical design
* Testing
* Systems integration

Only include skills supported by the repository or by information I have provided.

### Navigation

Make it extremely easy to reach:

* The Big Mach README
* Star Raptor README
* CAD/design documentation
* Build documentation
* Testing documentation
* Relevant media

The root README should not contain every technical detail. It should make the visitor want to click deeper.

---

## 5. Separate project READMEs

Each project should have its own polished README.

At minimum:

`big-mach/README.md`

`star-raptor/README.md`

These should feel like **individual engineering case studies**.

Do not simply duplicate the root README.

Each project README should tell a story.

Suggested structure:

### Overview

What is the project?

What problem or purpose did it serve?

### My Role

Be very explicit about what I personally did.

Distinguish between:

* Work I owned
* Work I contributed to
* Hardware/design supplied by another subteam
* Team-level accomplishments

Do not accidentally imply that I personally designed something if the repository indicates otherwise.

### Design

Explain the relevant mechanical/system design.

Use images heavily here.

For example:

* CAD screenshots
* Full assembly
* Exploded views
* Component closeups
* OpenRocket screenshots
* Technical diagrams

### Manufacturing

Show physical evidence of:

* 3D printing
* Composite work
* Assembly
* Mechanical components
* Finishing
* Integration

### Avionics / Integration

Where applicable, document:

* Avionics bay
* Electronics
* Wiring
* Batteries
* Sensors
* Integration with the airframe

Again, distinguish my work from work originating from other subteams.

### Testing

Show evidence of testing.

Include:

* Ground testing
* Separation testing
* Recovery testing
* Relevant videos
* Results
* What was learned

### Final Vehicle

Show the finished rocket prominently.

### Engineering Takeaways

Include a short section discussing what I learned or what engineering decisions were important.

This should sound like an engineering student reflecting on real work, not a generic AI-generated "lessons learned" section.

---

## 6. Images are a major priority

The repository currently has useful media. Make much better use of it.

Do not bury all images at the bottom of the README.

Images should appear **next to the content they explain**.

For example:

* Hero image near project introduction
* CAD screenshot in Design
* Manufacturing photo in Manufacturing
* Avionics photo in Avionics
* Test image/video in Testing
* Finished rocket near the conclusion

Use Markdown image embeds appropriately.

Prefer existing repository images rather than inventing images.

If multiple images exist, choose the strongest ones.

Avoid unnecessarily huge images that make the README slow to load.

Where appropriate, create simple image galleries using Markdown tables or other GitHub-compatible formatting.

---

## 7. Improve image organization

Review the existing media structure.

If the current structure is confusing, reorganize it into something intuitive.

For example:

```text
big-mach/
├── README.md
├── media/
│   ├── hero/
│   ├── design/
│   ├── manufacturing/
│   ├── avionics/
│   ├── testing/
│   └── launch/
```

Do not blindly follow this structure if the existing media suggests something better.

The goal is for a future visitor to understand where media belongs without having to guess.

Rename files where useful so that filenames are descriptive.

Avoid filenames such as:

`IMG_1234.jpg`

Prefer:

`big-mach-avionics-bay.jpg`

Do not rename files if doing so would break important references without fixing those references.

---

## 8. Full assembly ZIP

I have a full assembly archive for the project, including the SolidWorks assembly and potentially associated CAD files.

I want to potentially upload the full assembly as a ZIP so that people can access the complete CAD work.

**Do not immediately commit the ZIP.**

First:

1. Locate the archive if it is available locally.
2. Inspect its contents.
3. Determine its approximate size.
4. Determine whether it contains:

   * SolidWorks assemblies
   * Parts
   * Drawings
   * Configurations
   * References
   * Exported geometry
   * Other files
5. Determine whether the assembly is self-contained or has broken/external references.
6. Determine whether GitHub is an appropriate place to host it.
7. Consider repository size and GitHub file-size limitations.
8. Consider whether Git LFS, GitHub Releases, an external download, or another approach would be better.

Then **stop and discuss the findings with me before making a decision**.

I specifically want a running discussion about the contents of the assembly.

For each significant file/folder, explain:

* What it appears to be
* Whether it is useful to a portfolio visitor
* Whether it should be included
* Whether it should be documented
* Whether it should be excluded

Do not delete or alter CAD source files simply to make the archive smaller.

The purpose is to preserve the engineering work while making the public repository approachable.

If the full assembly should not live directly in Git, design a clean way for the README to say something like:

> Full CAD assembly available here.

with an appropriate download location.

Do not invent a download URL.

---

## 9. Portfolio storytelling

Think about the repository from the perspective of someone reviewing my portfolio for:

* Software engineering
* Mechanical engineering
* Systems engineering
* Embedded systems
* Aerospace engineering

The documentation should demonstrate that I can work across disciplines.

Highlight the connection between:

**requirements → design → manufacturing → integration → testing**

where the evidence supports it.

Do not turn this into a buzzword-heavy skills list.

Show the engineering through the project.

---

## 10. Preserve technical accuracy

This is extremely important.

Never fabricate:

* Dimensions
* Masses
* Performance
* Materials
* Test results
* Flight results
* Responsibilities
* Team responsibilities
* Components
* Design decisions

If a fact is not supported by the repository or by information I have explicitly provided, either:

* leave it out, or
* mark it as something that needs clarification from me.

When describing my contributions, err on the side of accuracy rather than making my role sound larger than it was.

---

## 11. Evidence-driven documentation

Where possible, connect claims to actual evidence.

For example:

**Claim:**

> Designed the full airframe assembly.

**Evidence:**

> Link/image showing the SolidWorks assembly.

Do this naturally rather than creating an academic citation system.

The goal is for a recruiter or engineer to be able to look at the repository and see evidence that the work actually happened.

---

## 12. GitHub presentation

Optimize specifically for GitHub's rendering.

Check:

* Relative image paths
* Internal README links
* Headings
* Tables
* Image sizes
* Broken links
* Code formatting
* Mobile readability
* Directory naming
* Navigation

Avoid fancy Markdown that GitHub does not render reliably.

Do not introduce unnecessary JavaScript or web-app dependencies.

---

## 13. Do not over-document

The repository should be impressive, not exhausting.

Use:

* Short paragraphs
* Strong images
* Technical bullet points
* Tables where useful
* Expandable sections only when genuinely helpful

The detailed project READMEs can contain deeper information, while the root README should remain relatively concise.

Think:

**Root README = portfolio landing page**

**Project README = engineering case study**

**Files/media = evidence**

---

## 14. Work iteratively

Do not make one giant blind rewrite.

Work in stages:

### Stage 1: Audit

Inspect the repository and summarize:

* Current structure
* Existing documentation
* Available media
* Missing media
* Problems
* Proposed new structure

### Stage 2: Discuss

Before making major structural changes, tell me what you found and what you recommend.

In particular, I want to discuss the full assembly archive and what it contains.

### Stage 3: Implement

After we agree on the direction:

* Rewrite the root README
* Rewrite project READMEs
* Reorganize media
* Add image embeds
* Improve navigation
* Add appropriate CAD/archive references
* Fix broken links

### Stage 4: Review

Perform a final portfolio-quality review.

Ask yourself:

> If I were a recruiter or engineering student seeing this GitHub repository for the first time, would I immediately understand what Jeremy built and want to see more?

Fix anything that prevents that.

---

## 15. Important: keep me involved

This is intended to be a **running collaboration**, not a one-shot autonomous rewrite.

When you encounter:

* Ambiguous files
* Unknown CAD components
* Unclear ownership
* Potentially important photos
* Large archives
* Missing information
* Questions about how something was built
* Questions about whether something should be public

**Ask me.**

Do not fill gaps with assumptions.

I want to be able to explain the engineering decisions and then have you incorporate that information into the documentation.

---

## 16. Final quality check

Before considering the task complete:

* No em dashes anywhere
* No fabricated technical claims
* No broken image links
* No broken README links
* Images are prominent and useful
* Root README works as a portfolio landing page
* Each project has its own README
* Project READMEs are substantially different from the root README
* My individual contributions are clearly identified
* Team contributions are not incorrectly attributed to me
* Full CAD assembly handling has been discussed before committing it
* Repository structure is intuitive
* Documentation feels human-written
* The repository is visually compelling
* A visitor can understand the projects quickly
* A technically interested visitor can dive much deeper

**Start with Stage 1 only. Inspect the repository and report your findings and proposed improvements before making major changes.**
