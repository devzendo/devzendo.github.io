---
permalink: /dev/commons/
title: "Common libraries"
excerpt:  "Small acorns from which mighty oaks may grow."
author_profile: false
---

{% include base_path %}

## About
We have several small utility libraries that underlie most of the other projects we write.
These don't warrant their own page; consult their JavaDoc for details.
All of them are in Java/Scala, and are built and managed with Maven 3.

These projects are all due to be refreshed, and republished to Maven Central soon, with names that adhere to the Maven artifact naming convention, which is lower-case-words-separated-by-hyphens, instead of CamelCase.
{: .notice--info}

Unless otherwise stated:

* **License:** <a href="http://www.apache.org/licenses/LICENSE-2.0.html">Apache License v2</a>
* **Release schedule:** Released as part of the [DevZendo.org release schedule]({{ base_path }}/dev/release-schedule) which allows for 8 releases per year.
* **Availability**: Available from the <a href="http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22org.devzendo%22">Central Maven Repository</a>
* **Source code:** All available from <a href="https://github.com/devzendo">GitHub</a>

## group-parent
* Common Maven settings for all DevZendo Java projects.
* **Current release:** 1.1.10 (named group-parent)
* **Source code:** <a href="https://github.com/devzendo/group-parent.git">

## group-parent-scala
* Common Maven settings for all DevZendo Scala projects.
* **Current release:** 1.0.2
* **Source code:** <a href="https://github.com/devzendo/group-parent-scala.git">

## common-code
* Small, low-dependency utility library for:
  * collections, 
  * concurrency, 
  * date/time, 
  * exception handling, 
  * process execution, 
  * file handling, 
  * logging, 
  * OS detection, 
  * patterns, 
  * preferences storage, 
  * resource handling, 
  * string manipulation, 
  * type aliasing.
  {: .small}

* **Current release:** 1.1.4 (named common-code)
* **Source code:** <a href="https://github.com/devzendo/common-code.git">

## common-code-scala
* Small, low-dependency Scala specific utility library.
* **Current release:** not yet released
* **Source code:** <a href="https://github.com/devzendo/common-code-scala.git">

## common-app
* Small library that provides an application lifecycle and service management layer, using the Spring framework.
* **Current release:** 1.1.0 (named common-app)
* **Source code:** <a href="https://github.com/devzendo/common-app.git">

## common-gui
* Small library that provides some of our common Swing-based GUI helper functionality.
* **Current release:** 0.4.0 (named CommonGui)
* **Source code:** <a href="https://github.com/devzendo/common-gui.git">

## bsd-third-party
* Small library that provides code written by others, that is not otherwise published on the central Maven repository, that is licensed under the BSD license.
* **License:** <a href="https://opensource.org/licenses/BSD-3-Clause">BSD 3-Clause License v2</a>
* **Current release:** 1.1.0
* **Source code:** <a href="https://github.com/devzendo/bsd-third-party.git">Git source repository, hosted on Github

