---
permalink: /dev/xplp/
title: "Maven Cross-Platform Launcher Plugin"
excerpt: "Create launchable applications."
author_profile: false
---

{% include base_path %}

With a minimum of configuration, this Maven plugin will generate a tree of files that contain your application jar, all its
dependencies, and the necessary launcher scripts/executables/control-file structure needed to launch your application on Windows, Mac OS X, and Ubuntu Linux.

Note that this plugin only creates the launcher structure - you will need additional plugin work to turn this output into an installer.

To find the correct JVM and launch it, the plugin uses shell scripts on Linux, Janel on Windows, and the Universal Java Application Stub on Mac OS X.
## Resources

* **License:** 
  * Plugin: <a href="http://www.apache.org/licenses/LICENSE-2.0.html">Apache License v2</a>
  * <a href="https://github.com/tofi86/universalJavaApplicationStub">Universal Java Application Stub</a> (embedded in this plugin) is Copyrighted by Tobias Fischer: <a href="https://opensource.org/licenses/MIT">MIT License</a>
  * <a href="https://github.com/michaelknigge/janel">Janel</a> (embedded in this plugin) is Copyrighted by Copyright (c) 2017 Timothy Kil, Michael Knigge and others who had contributed code to Janel: <a href="https://opensource.org/licenses/MIT">MIT License</a>
   
* **Documentation:** <a href="{{ base_path }}/static/xplp-site/index.html" target="_blank">Plugin site documentation</a> (open in new tab)
* **Change history:** [change history]({{ base_path }}/dev/xplp-change-history).
* **Current release:** 1.2.0
* **Release announcements:**
  * [1.2.0 21st February 2019]({{ base_path }}/development/xplp-1.2.0)
  * [1.1.1 28th September 2017]({{ base_path }}/development/xplp-1.1.1)
  * [0.2.2 25th September 2013]({{ base_path }}/development/xplp-0.2.2)
  * [0.2.1 19th April 2011]({{ base_path }}/development/xplp-0.2.1)
  * [0.2.0 28th September 2010]({{ base_path }}/development/xplp-0.2.0)
  * [0.1.0 1st August 2010]({{ base_path }}/development/xplp-0.1.0)
* **Release schedule:** The plugin is released as part of the [DevZendo.org release schedule]({{ base_path }}/dev/release-schedule) which allows for 8 releases per year.
* **Availability**: This is available from the <a href="http://search.maven.org/#browse%7C-125156780">Central Maven Repository</a>
* **Source code:** <a href="https://github.com/devzendo/xplp">Git source repository

