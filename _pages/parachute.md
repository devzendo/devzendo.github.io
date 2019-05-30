---
permalink: /parachute/
title: "The Parachute Project"
excerpt: "Let's stick with the past, 'cos the future won't last."
author_profile: false
---

{% include base_path %}

This is a long-term project; something of a historical reconstruction, inspired by 
* the Inmos Transputer, occam and CSP. 
* Professor Niklaus Wirth's Project Oberon, and his paper "A Plea for Lean Software".
* <a href="https://github.com/pervognsen/bitwise">Per Vognsen's Bitwise project</a>.

The goals are: 
 * to build a portable, open source Transputer emulator, inspired by a version I wrote several years ago
 * write a toolchain to support development for it
 * produce a port of eForth that runs on it
 * extend eForth into a distributed OS kernel
 * learn about process calculi
 * investigate modern/concurrent/functional language design
 * investigate building an FPGA Transputer system capable of running the above

To download the current release of Parachute for macOS, Ubuntu, CentOS, Raspberry Pi, or Windows 10, visit the [**Parachute Downloads**]({{ base_path }}/parachute-download/) page.

The history of the project leading up to its current point can be found at the [**Parachute Project History**]({{ base_path }}/parachute-history/) page.

Parachute is released under the [**Apache License 2.0**](http://www.apache.org/licenses/LICENSE-2.0).

The current state is that I have the following three sub-projects - the README.md at the top-level of each of these
repositories will give more detail...

All are IN PROGRESS, NOT YET RELEASED FORMALLY.

WORKING (assembles eForth correctly), STILL NOT FEATURE-COMPLETE - The Transputer MASM-subset Macro Assembler can be found at:
```
https://bitbucket.org/devzendo/transputer-macro-assembler
```

IN PROGRESS (needs I/O code changing to match my I/O server protocol) - Transputer eForth can be found at:
```
https://bitbucket.org/devzendo/transputer-eforth
```

WORKING (needs releasing) - The Transputer emulator itself can be found at:
```
https://bitbucket.org/devzendo/transputer-emulator
```


# Future
Other things I've always wanted to write: my own OS; my own language.... 

Once eForth works, and I can investigate the system, it needs to grow to provide the facilities I want so that
this can be my version of Project Oberon. There will need to be an ELF loader, and a bootloader that can link with an ELF object. Then a
higher level language (one or more) will be needed for later stages... perhaps best achieved by "just" writing a
back end for LLVM that targets the T800...

The emulator itself could be reworked to run a virtual Transputer on each physical core, with links connecting the
cores; it could have 'video memory' added via say the SDL library.

# Modern Hardware Transputers
There's an interesting project called 
<a href="https://web.archive.org/web/20170726121213/http://www.opentransputer.org/">OpenTransputer</a> (that seems to
have dried up), involving making a new Transputer in an FPGA, and with the links replaced with a switch to a Benes
network. They have a version of <a href="https://github.com/TransputerSystems/TSS">occam written in Java</a>;
it'd be good to port that to use my back end toolchain...

Also, <a href="https://tu-dresden.de/ing/informatik/ti/vlsi/ressourcen/dateien/dateien_studium/dateien_lehstuhlseminar/vortraege_lehrstuhlseminar/lehrstuhlseminar_ss17/20170720_T42_Transputer-in-FPGA_DesignStatus_DeptSeminar-Presento_UM.pdf?lang=en">
Uwe Mielke's T42 Transputer in FPGA</a> project.

# Other Emulators
There are more emulators now - 
* <a href="http://transterpreter.org">the Transterpreter</a>, 
* <a href="https://sites.google.com/site/transputeremulator/Home">Gavin Crate's emulator</a>, 
* <a href="http://spirit.lboro.ac.uk/emulator.html">Julian Highfield's emulator</a>.

# Resources
* <a href="{{ base_path }}/static/transputer/tis-acwg.pdf" target="_blank">Transputer Compiler Writer's Guide</a> (PDF) (open in new tab)
* <a href="{{ base_path }}/static/transputer/compiler-writers-guide-errata.txt" target="_blank">Transputer Compiler Writer's Guide Errata sheet</a> (ASCII) (open in new tab)


So the Transputer isn't dead... watch this space...

... to be continued ...

Matt Gumbley, Tue 30 Apr 2019
