---
permalink: /parachute-history/
title: "The Parachute Project: History"
excerpt: "Let's stick with the past, 'cos the future won't last."
author_profile: false
---

{% include base_path %}

# Versions 1 and 2, Keele University

The origin of this project was around December 1995 to March 1996. 

The final year project in my computer science undergraduate degree was to write an emulator for the Inmos T800
Transputer. This was at Keele University, under Dr. Barry Cook. 

The first version was written in occam (converted from occam to C via the SPOC system) - and was very slow. I rewrote
it around March 1996, in C (a language with which I was more familiar at a low level). This version 2 was much faster.

# Version 3, The Lost Version

A couple years after I graduated, I started afresh with a third version in C++, with Microsoft Visual Studio and MFC;
a graphical version with an indended debugger/disassembler user interface inspired by Microsoft CodeView. It would run
binary T800 programs compiled by SPOC etc... sadly I never got it to a fully working point, and the code was lost.

# Version 4 Part I, On The Train

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

# Version 4 Part II, Modern Operating Systems

... until Feb 2018. I came across my old Transputer books whilst looking for some other old book, and started leafing
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

I started looking into using NASM, the netwide assembler, for my next investigation: an attempt to get
eForth running on the Transputer emulator. I've always wanted to get eForth running on something; my last attempt
was on the Psion 3c PDA...

... however this did not yield a successful build.

So I set about building my own MASM clone - just the subset needed to assemble eForth. This is now working, and
assembling in exactly the same way as MASM does.

I now need to write an assembler client library for my emulator's I/O server protocol, wire this into eForth.

This will give me an emulated system I can work with in eForth.
