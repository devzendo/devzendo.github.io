---
permalink: /apps/shell/
title: "Object Shell"
excerpt: "Cross-platform object shell, inspired by PowerShell and UNIX."
author_profile: false
---

{% include base_path %}

The DevZendo.org Shell is a small console shell (command-line environment) that takes 
the idea of UNIX pipelines, and extends it with Java/Scala objects. It is a 
work-in-progress cross-platform homage to PowerShell and Scala, sort-of.

It is written in Scala, and some Java.

## Overview

Commands can be given that generate streams of objects - which may be Strings (as with UNIX), 
or other Java objects such as Files, Integers, Doubles, Booleans, Arrays or other containers. 
These streams can be piped into other commands to transform them or filter them. 
The commands in a pipeline each execute in their own thread.

e.g. `find-files "." -recurse | select-property "name" -endswith ".java" | select-property "size" -filter { _ > 2kb } | foreach { echo _ " is rather large" }`

This gives a flavour; the commands shown have not yet been written, but much of the infrastructure allowing them to execute works. 

<ul>
<li>find-files will list the given directory, recursing as necessary, and push the java.io.Files it finds into its output pipe. </li>
<li>select-property is asked to get the "name" property of each object it finds on its input pipe (java.io.File in this case), which it does by calling getName() on it. It then responds to its -endswith switch by calling endsWith(".java") on the resulting name String. If this yields true, the java.io.File is pushed into its output pipe.</li>
<li>select-property then runs on each of these Files, getting the size by calling getSize(), and running a filter block of { _ > 2kb } on each. This is a subcommand, which has the size object aliased to the _ pseudovariable, and the > ordering relation command run with it, and a further argument of 2048 (literals can have SI suffixes). If the subcommand yields true, the File is yet again piped to the output...</li>
<li>...where foreach receives it. It runs a subcommand on it, aliasing it to _, and calling the echo command, which outputs all its arguments to the output pipe, in this case _, the File, which has its toString() called to display it, followed by the String " is rather large".</li>
<li>This command pipeline is not directed to a variable, so the final output pipe is wired to the Shell's equivalent of standard output, which causes a Log4J log at INFO level.</li>
</ul>


The Shell has a small (growing) library of commands, and the library is user-extensible. Commands can be written in Java or Scala. 

The Shell language is not yet fully realised. The basic support for commands, the evaluation of their arguments, and scoping of variables is done. Delayed evaluation of command arguments and blocks is not yet done, so there are no control structures at the moment. 

A typical set of "operator" commands is provided:

<ul>
<li> + - / * for Integers and Doubles; + and * also provide String concatenation and replication; % is Integer modulus</li>
<li> ! && || ^^ logical ops for Booleans </li>
<li> ^ | & ~ bitwise ops for Integers and Booleans </li>
<li> &lt; &gt; &lt;= &gt;= != == ordering relations and inequality/equality </li>
</ul>

The language has no notion of operators and their precedence; there are only commands, and such "operator" commands must have the desired precedence explicitly given with parentheses.

Commands can be given via three syntax styles:

<ul>
<li>Infix command: 3 + 2</li>
<li>Prefix command: + 3 2</li>
<li>Prefix function: +(3, 2)</li>
</ul>

These commands invoke the + command, giving it the arguments 3 and 2. The result, 5, is pushed into the + command's output pipe. If the output is not redirected to a variable, it is displayed.

The arguments to commands need not be primitives, as above, but could be variables containing the output of previous pipelines.

Some commands work with their arguments, some work with the data presented on their input pipe. i.e. it makes no sense to pipe data into the + command. (I suppose it could perform a summation).


## Exploratory Testing

One use of the Shell is as a tool that allows the user to explore an object/system's API by driving it by interactively via an extensible command language.

Before solidifying/characterising the use of an object by writing unit/integration tests, you sit at the keyboard and play with (or explore) the object/system. To make use of the shell, the commands you enter are programmed as methods of a <em>Shell Plugin</em>: an Adapter [GoF] to the object/system. This shell plugin is dynamically loaded by the shell; its command methods are then available interactively.

The interactive exploratory approach should not be used as a replacement for unit/integration tests; it is ideal where the problem being solved is not well understood (e.g. when writing an API to control some hardware or new API). Note that it can be difficult trying to convince agile/TDD developers who have not experienced interactivity or extensibility that they might need interactivity or extensibility.


## Resources

* **License:** <a href="http://www.apache.org/licenses/LICENSE-2.0.html">Apache License v2</a>
* **Documentation:** <a href="http://devzendo.org/sites/default/files/shell-site/index.html">Shell documentation</a> 
* **Current release:** Not yet released
* **Release schedule:** The shell is released as part of the [DevZendo.org release schedule]({{ base_path }}/dev/release-schedule) which allows for 8 releases per year.
* **Availability**: This is available from the <a href="http://search.maven.org/#browse%7C-125156780">Central Maven Repository</a>
* **Source code:** <a href="https://github.com/devzendo/shell.git">Git source repository, hosted on GitHub
* **Contact:** there is no mailing list at the moment, please use the [contact us page]({{ base_path }}/contact), or <a href="http://twitter.com/devzendo">follow/tweet to us on Twitter</a>.


