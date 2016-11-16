---
permalink: /dev/xplp-change-history/
title: "Maven Cross-Platform Launcher Plugin: Change history"
excerpt: "Create launchable applications."
author_profile: false
---

{% include base_path %}

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

