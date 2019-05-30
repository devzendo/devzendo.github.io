---
permalink: /parachute-changelog/
title: "The Parachute Project: Changelog / Release Notes"
excerpt: "What happened when!"
author_profile: false
---

{% include base_path %}

0.0.1 (ongoing work for the first release)
* Versioning and build now controlled by Maven and CMake.
* Successfully runs hello2.asm !
* Renamed emulator binary from t800emul to temulate.
* Started adding the T801 instructions, from "Transputer Instruction Set - Appendix, Guy Harriman".
* Started adding the T801/T805 instructions from "Support for debugging/breakpointing in transputers" (INMOS
  Technical Note 61).
  Added the -j flag to enable 'j 0' breakpoints.
* Described current implementation/missing status in the above section.
* The T810 instructions from "The IMS T810 - A Preliminary Survey" are not implemented.
* Builds using Maven/CMake/CLion on macOS, Windows 10, CentOS 7, Ubuntu LTS, Raspbian Stretch.
* Added Boot-from-ROM, fixed Wdesc bug after boot from link.
* Fixes: xword, call, j & scheduling (with assistance from Michael Brüstle), locations of TPtrLoc1, TPtrLoc0.
  csngl and xdble: correct detection of sign of Areg
* Monitor: db (renamed from da), dw improvements, added w (workspace display), added b/b+b-/b? (breakpoints),
  added s (show all state).
* Adopted the Apache License v2.
* Since the assembler understands offset addressing, the manual building of offset operands has been changed from:
  j 'label - _XX1' \\
  _XX1: \\
  to: \\
  j label \\
