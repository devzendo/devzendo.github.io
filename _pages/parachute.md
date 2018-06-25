---
permalink: /parachute/
title: "The Parachute Project"
excerpt: "Let's stick with the past, 'cos the future won't last."
author_profile: false
---

{% include base_path %}

This is one of my projects that isn't quite ready to be released yet. 

It's quite a long-term project; something of a historical reconstruction, inspired by one of my
favourite lyrics:

"Let's rebuild the past, 'cos the future won't last." -- "The Hot Revivalist" by The High Llamas.

... and also by the works of genius that were the Inmos Transputer, occam and CSP. I'm also inspired in this project
by the genius of Charles 'Chuck' H. Moore, and the Forth language he invented. Also by Professor Niklaus Wirth's
Project Oberon, and his paper "A Plea for Lean Software".
 
The history of the project leading up to its current point can be found [**here]](){{ base_path }}/parachute-history/)


The current state is that I have the following three sub-projects:

The Transputer MASM-subset Macro Assembler can be found at:
```
https://bitbucket.org/devzendo/transputer-macro-assembler
```

Transputer eForth can be found at:
```
https://bitbucket.org/devzendo/transputer-eforth
```

The Transputer emulator itself can be found at:
```
https://bitbucket.org/devzendo/transputer-emulator
```


# Future
Other things I've always wanted to write: my own OS; my own language.... 

<a href="http://www.projectoberon.com/">Niklaus Wirth's Project Oberon</a> is a huge inspiration - build a complete useful system that one person can understand all of. 

<a href="https://github.com/pervognsen/bitwise">Per Vognsen's Bitwise project</a> is similarly inspiring.

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
There are more emulators now - <a href="http://transterpreter.org">the Transterpreter</a>, 
<a href="https://sites.google.com/site/transputeremulator/Home">Gavin Crate's emulator</a>, 
<a href="http://spirit.lboro.ac.uk/emulator.html">Julian Highfield's emulator</a>.


So the Transputer isn't dead... watch this space...

... to be continued ...

Matt Gumbley, Fri 13 Apr 2018
