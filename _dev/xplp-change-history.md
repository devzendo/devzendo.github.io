---
permalink: /dev/xplp-change-history/
title: "Maven Cross-Platform Launcher Plugin: Change history"
excerpt: "Create launchable applications."
author_profile: false
---

{% include base_path %}

## [1.1.1 28th September 2017]({{ base_path }}/development/xplp-1.1.1)

* Second release to Maven Central.
* Source moved to bitbucket, updated many dependencies.
* Fix bug: expand the shell's arguments in double quotes, so that if you use quotes to preserve a single argument
  containing spaces, the Java program receives it as a single argument.
* Built with Java 1.7.
* Added the universal application stub v2.1.0 from Tobias Fischer. This allows OSX launchers to run with JVMs
  more modern than Apple's Java 1.6. The default stub is still Apple's: to switch to the universal stub and run
  with the most modern JVM you have, use the <stubType>Universal</stubType> option in your configuration.
  The universal application stub is licensed under the MIT license.
* 1.1.0 exists but has errors in documentation.

## [0.2.2 25th September 2013]({{ base_path }}/development/xplp-0.2.2)

* First release to Maven Central.

## [0.2.1 19th April 2011]({{ base_path }}/development/xplp-0.2.1)

* This release is tested on Windows 2000, Windows XP, Mac OS X 10.6 and Ubuntu Linux 10.04.1 LTS. 
* Fixes a Linux launching bug where the error code was not being returned correctly
* Changed the Windows-specific janelType configuration property to be available in all builds, and renamed it launcherType. It only makes sense on Windows or MacOSX. Use of janelType now fails the build with a message saying "use launcherType". On MacOSX, use the console launcherType to create a structure like that used on Linux; GUI is still the default and still creates a .app structure.

## [0.2.0 28th September 2010]({{ base_path }}/development/xplp-0.2.0)

* Adds support for the Maven NAR Plugin, in order to create launchers for projects that incorporate JNI code.

## [0.1.0 1st August 2010]({{ base_path }}/development/xplp-0.1.0)

* Initial OSX only release.

