---
title: Finger of Indication
linkout: https://github.com/cbcGirard/finger-of-indication
components: [Meshlab, Fusion360, 3d printing]
layout: project
desc: Teacher's little helper for troubleshooting code and circuits
---

<iframe src="https://chapman456.autodesk360.com/shares/public/SH30dd5QT870c25f12fcd6831dfc3ad04be8?mode=embed" width="720" height="600" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

# Motivation
I like my classes to be mostly hands-on; it's both a better way to learn than simply trying to absorb a lecture, and *way* more fun for *me* than standing up front and talking. As a result, I spend a lot of time on over-the-shoulder debugging with students.

When a breadboarded circuit goes wrong, it often takes some careful tracing to find *where* the problem is: move a wire a couple millimeters, and you might have a completely different circuit than you intended, though it looks basically identical. 

# Goals
- Since breadboards use a standard 0.1" spacing, the pointer should be at least that narrow to unambiguously point out the relevant location

- Though I wanted a fine pointer to poke through the mess of wires, it had to be nonconductive. That ruled out metal construction, but relying on 3d printed plastic limited how thin and long I could make the pointer without it snapping off immediately.

- I already [carry a pen at all times](../_faves/pen.html) for notetaking, so I could design some kind of cap with a small, extra-pointy protrusion to give enough precision while still being mechanically roubust.

# Implementation
Since I was going to 3d print the part in an eye-catching neon hue, I wanted to have a little fun with the design. A quick search for "pointer finger" yielded [an excellent starting point](https://www.printables.com/model/219826-pointer-extendable), though I was a bit skeptical that the telescoping part would be sufficiently robust and stuck with the idea of a pen cap like [another model used](https://www.printables.com/model/216468-pointer-finger-stick-pen).

[Fusion360](../_faves/fusion360.html) isn't great for sculpting meshes, but it will happily import .stl files and combine them with your geometrically-defined CAD models. Export the resulting union as another .stl, and proceed with your 3d-printing pipeline of choice.

# Improvements
I was pretty pleased with the initial test print, with one minor complaint: the finger was much sausage-ier than I'd like. I didn't want to shrink the dimensions too much and compromise the structural integrity, but it looked like I could get away with shrinking the finger's width but keeping the thickness to compromise between the two goals. Stretching the tip lengthwise also helped enhance the desired pointiness of the finger where stiffness was less important. I'd used [Meshlab](https://www.meshlab.net/) before for these kind of localized tweaks, and the 'per-vertex geometric function' filter made it relatively straightforward to adjust it appropriately.

Since the geometry (other than the finger itself) is pretty straightforward, this would be well suited to a parametric design tool like [OpenSCAD](../_faves/openscad.html) or a Python script with basic mesh manipulation capabilities.