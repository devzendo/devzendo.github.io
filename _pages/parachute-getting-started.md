---
permalink: /parachute-getting-started/
title: "The Parachute Project: Getting Started"
excerpt: "Let's get parallel!"
author_profile: false
---

{% include base_path %}

So, you've downloaded Parachute in archive form from the [**Parachute Downloads**]({{ base_path }}/parachute-download/)
page. 

To ensure that you are getting software from legitimate sources, you can verify that what you have was produced by this
developer, not 'enhanced' with malware by a malicious third party, by 
[**verifying the digital signature**]({{ base_path }}/verifying-digital-signatures/) of your download.

Read on to find out how to install Parachute, how to assemble a sample program, and then how to run it.

1.  Unpack the archive into an installation folder.

    **For Windows systems**, you can use File Explorer to open the .zip file, then drag the contents out to
    into a new folder - say `C:\Parachute` - this will give you `C:\Parachute\bin`, `C:\Parachute\lib` folders etc.

    **For UNIX-Like systems** (CentOS, Ubuntu, macOS, Raspbian), extract the archive from the command line.
    Since it isn't (yet) shipped as a package file, such as .deb (Ubuntu, Raspbian) or .rpm (CentOS),
    or .pkg (macOS), you could create a folder for it under the /opt tree:
    
    `sudo bash` (Enter administrator password, then...)
    
    `mkdir -p /opt/parachute && cd /opt/parachute`
    
    `tar xzvf ${HOME}/Downloads/parachute-0.0.1-mac-x86_64.tar.gz` (Say, for the macOS download)
    
    This will give you `/opt/parachute/bin`, `/opt/parachute/lib` folders, etc.
    You _could_ unpack it under `/usr/local`, but note there are a few .md files at the top level of the archive.
    
2.  Add the `bin` folder to the `PATH` environment variable.

    **For Windows systems**: 
       * right-click on the Windows icon in the bottom left of the screen
       * choose `System` from the menu
       * then on the left side of the Control Panel window, choose `Advanced system settings`
       * after entering any administrator password necessary, click the `Environment Variables...` button
       * double-click the `Path` under System variables
       * click the `New` button
       * enter `C:\Parachute\bin`
       * OK all the way out of this
       * you might need to log out/in, or reboot for the change to take effect
       
    **For UNIX-Like systems**, edit your shell's startup file and add `/opt/parachute/bin` to your `$PATH`.
    Since there is such vast scope to customise UNIX-Like systems to work they way you want them to, only
    general instructions can be given, for the typical `bash` shell:
       * edit e.g. `~/.bashrc` in your favourite editor
       * change the setting of `PATH` e.g.
       * `export PATH=$PATH:/opt/parachute/bin`
       * save the file, and log out/in, or `source ~/.bashrc` as appropriately
       
3.  Open a `terminal` or `Command Prompt` window, and run the emulator with the option to show its syntax summary:

    `[matt] ~ $ temulate -h` (macOS, under iTerm2)
    `C:\Users\matt > temulate -h` (Windows 10, Command Prompt)
    
    This should now show you the syntax:
    ```
    INFO  Parachute v0.0.1 Portable Transputer Emulator May  7 2019
    INFO    (C) 2005-2019 Matt J. Gumbley
    INFO    http://devzendo.github.io/parachute
    INFO  Usage:
    INFO  temulate: [options] [romfile]
    INFO  If romfile is given it is loaded at the end of memory, and the Emulator uses Boot From ROM. If it is not
    INFO  given, the Emulator uses Boot From Link, waiting for the boot protocol on Link 0.
    INFO  Options:
    INFO    -c    Displays configuration summary
    INFO    -da   Enables disassembly during emulation
    ...
    ```
    
4.  Now you have the software installed and working, let's run the sample 'Hello World' program.

    You will need two `terminal` or `Command Prompt` windows, one for the Emulator, and one for the I/O server. 
    So create another. 
    
    > The Transputer is just a CPU with memory and four I/O links. It can't access the operating
    > system of the system it's running on directly. Any access to the operating system is done by sending appropriate
    > I/O protocol messages down I/O link #0, to the I/O server that's running on the same system as the emulator.
    
    In the I/O server window, run:
    
    ```
    [matt] ~ $ nodeserver /opt/parachute/examples/hello2/hello2.bin        (UNIX-Like)
    C:\Users\matt > nodeserver C:\parachute\examples\hello2\hello2.bin     (Windows)
    (does not return)
    ```
    
    In the second terminal window...
    ```
    [matt] ~ $ temulate                                                    (UNIX-Like)
    C:\Users\matt > temulate                                               (Windows)
    ```
    
    The first terminal window should now show:
    ```
    [matt] ~ $ nodeserver /opt/parachute/examples/hello2/hello2.bin
    hello world
    (still does not return)
    Ctrl-C <<- you'll have to interrupt it.
    ```
