---
title: LabVIEW
resourceType: Software
categories: [programming]
site: https://www.ni.com/en/support/downloads/software-products/download.labview.html
isFoss: false
layout: fave
OSes: [apple, linux, windows]
---

You'll either love LabVIEW or absolutely despise it. I changed camps once I tried (and failed) to recreate a fairly simple LabVIEW-based project in a traditional programming language, and realized how much easier it was to set up the user interface in LabVIEW. If you need a flexible way to control hardware from a single interface, you'll have a hard time finding a better tool.

If you're just playing around (i.e., not using it for commercial or academic projects), you can use the Community edition for free; the full commercial version is *very* expensive, but the academic versions I've used have been pretty reasonable (though you'll need to arrange it through their sales department).

Mac support for hardware can be iffy, though running it in Parallels seems to be just as stable as the native Windows version.

Certain Arduino and Raspberry Pi models can be controlled directly from LabVIEW using their LINX toolkit. With a little bit of poking around, you can probably get it working with other Arduino-compatibile boards as well; my [LINXx](../projects/lynxx.html) project should give you some idea of how the existing toolkit is set up and where you might start your own extensions.