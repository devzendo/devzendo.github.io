---
permalink: /parachute/
title: "The Parachute Project"
excerpt: "Let's stick with the past, 'cos the future won't last."
author_profile: false
---

{% include base_path %}

This is one of my projects that isn't quite ready to be released yet. But hey, it's open source! It's out there!
I'm building it, so.... come!

It's one of those long-term aspirational things; something of a historical reconstruction, inspired by one of my
favourite lyrics:

"Let's rebuild the past, 'cos the future won't last." -- "The Hot Revivalist" by The High Llamas.

... and also by the works of genius that were the Inmos Transputer, occam and CSP. I'm also inspired in this project
by the genius of Charles 'Chuck' H. Moore, and the Forth language he invented. Similarly by Professor Niklaus Wirth's
Project Oberon, and his paper "A Plea for Lean Software".
 

# Origin - Phase 1, The Keele Years

The origin of this project was around December 1995 to March 1996. 

The final year project in my computer science undergraduate degree was to write an emulator for the Inmos T800
Transputer. This was at Keele University, under Dr. Barry Cook. 

The first version was written in occam (converted from occam to C via the SPOC system) - and was very slow. I rewrote
it around March 1996, in C (a language with which I was more familiar at a low level).

This version 2 was much faster.

I had this idea about having a Transputer virtual machine running on every desktop, running distributed computation
jobs - like the BOINC network does.... "just" connect the links to network ports, and with a bit of hand waving, you've
got a compute grid... "just like that".... ah, youth..

# Origin - Phase 2, The Lost Version

A couple years after I graduated, I started afresh with a third version in C++, with Microsoft Visual Studio and MFC;
a graphical version with an indended debugger/disassembler user interface inspired by Microsoft CodeView. It would run
binary T800 programs compiled by SPOC etc... sadly I never got it to a fully working point, and the code was lost.

# Origin - Phase 3, Trains and Parallel Processing

In 2005, I was bored during my commute to work, and having some time to kill on the train, and an old laptop running
Linux, set about starting a new version of the Transputer emulator. This time, the links were connected to network
ports. Link 0 can also communicate with a server process. I defined a small protocol for this server
(later work will make use of existing Transputer server protocols; I needed something to get started).

I found on the Internet Parallel Computing Archive a project called ttools, which was an assembler/linker/disassembler,
custom object format, and boot loader - and also by the same authors, a port of GCC 2.7.2 with the various
Transputers as targets. It built OK on the old 32-bit RedHat Linux I had at the time (this was possibly RedHat 7.3
before it changed to Fedora). 

So in 2005 I could write in C, or assembler, and run it on the emulator.

Then, as tends to happen with large projects, I changed focus onto something else, and put this to one side.....

# Origin - Phase 4, Trains and Modern Operating Systems

... until 2018. I came across my old Transputer books whilst looking for some other old book, and started leafing
through them again, realising that this was an idea that I was once (more than once) keen to pursue. 

So, I started dusting off the old code. 

First, I'd need to get ttools and gcc building on OSX, CentOS, Ubuntu and Windows 10 - I'd need to make this available
on all modern platforms, if it was to be popular and useful. I soon ran into complications. It's old code, and 64-bit
systems weren't around in its day. I spent a month on the train journey trying to get it building on OSX, and on old
VMs of Ubuntu 5.04 - but there are subtle bugs on 64-bit that I ran out of time trying to fix. It might still build
fine on 32-bit, but who would want to have an old VM installed, just to make use of an old toolchain?

So I've abandoned ttools/gcc. If you fancy a challenge, you can find my efforts at making it work at
```
https://bitbucket.org/devzendo/transputer-toolchain
```

I'm looking into using NASM, the netwide assembler, for my next investigations, which will be an attempt to get
eForth running on the Transputer emulator. I've always wanted to get eForth running on something; my last attempt
was on the Psion 3c PDA...

The Transputer emulator can be found at:
```
https://bitbucket.org/devzendo/transputer-emulator
```

Transputer eForth can be found at:
```
https://bitbucket.org/devzendo/transputer-eforth
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
