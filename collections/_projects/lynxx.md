---
title: LYNXx
linkout: https://github.com/cbcGirard/LINXx
components: [programming, LabVIEW, Arduino, Teensy]
layout: project
desc: Extended firmware for controlling Arduino boards with LabVIEW.
---

As a TA, I found hardware compatibility was frequently an issue for Mac users in my classes. Students often wanted to pair small, battery-powered Arduino hardware with a nicer LabVIEW interface on their laptops. Synchronizing data between the two over serial or WiFi was often a source of confusion; the NI-supported toolkit (LINX) made it easy to program the Arduino entirely from LabVIEW and keep the two in sync, but it only supported a limited number of older Arduino models---not the fancier ones students wanted to use in their projects.

Since the LINX toolkit is open-source, I decided to extend it to support newer Arduino models (and their additional features). In addition to the LINXx code itself, I also set up Doxygen to automatically document the code and [publish it to GitHub Pages](https://cbcgirard.github.io/LINXx/); that way, it should be easier for others to understand how the existing project works and where to start for further adaptations.