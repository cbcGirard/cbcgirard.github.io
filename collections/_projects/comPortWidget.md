---
title: COM port monitor
linkout: https://github.com/cbcGirard/COM-list-Widget
components: [Rainmeter]
layout: project
desc: List the active COM ports, with auto-update.
---

# Motivation
Making sure the Arduino IDE was actually pointed at the right board was a confusing process for a lot of beginners, especially during the 1.x days of the software. You could manually compare the list of ports before and after plugging the board in, but badly-behaved Windows machines sometimes spat out a long list of dummy entries, making the hunt for the correct entry needlessly difficult.

# Implementation
[Rainmeter](../_faves/rainmeter.html) seemed like the easiest way to create an always-on widget for Windows, and potentially install it across the instructional lab's computers.

Though I had (and still have) minimal experience with PowerShell scripting, it didn't take much Googling to find a relevant built-in command. A little tweaking, and I had a one-liner that Rainmeter could call every couple seconds and display the port number + description of each active device.

# Improvements
Now that the Arduino IDE enumerates the available serial ports in real-time, there's not much need for an additional widget to show what the board you just plugged in shows up as. Plus, my little hack is Windows-only, while the IDE seems to be equally convenient on Mac and Linux machines.