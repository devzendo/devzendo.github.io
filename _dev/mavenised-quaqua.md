---
permalink: /dev/mavenised-quaqua/
title: "Quaqua look-and-feel library"
excerpt: "The Quaqua look-and-feel library, available from Maven Central."
author_profile: false
---

{% include base_path %}

Werner Randelshofer's excellent <a href="http://randelshofer.ch/quaqua/index.html">Quaqua</a> Look and Feel library for Mac OS X is available from his site as a .zip download.
To make it easier to use in Maven-based projects, I have converted it to a set of zips/jars containing javadocs, sources, Java library and Native library, and have deployed this to the Central Maven Repository.

**Note that Werner's domain is randelshofer.ch, which would give a Maven group id of ch.randelshofer, however, I can't deploy under that, so, these artifacts are deployed under the org.devzendo group id.**
 
The latest release to central is his 9.1 version; there is also an older release of 7.3.4.

Note that this does not make any changes to Quaqua, it's just a repackaging and distribution. Quaqua is &copy; 2003-2017 Werner Randelshofer, and is distributed under the Modified BSD and LGPL licenses. Please see <a href="http://randelshofer.ch/quaqua/license.html">the Quaqua license page</a> for more details.

## Using the Quaqua libraries via Maven

Two versions are published, please take care with the capitalisation of the artifacts as this has changed with 9.1. 
I am now adhering to the maven artifact naming convention of 'all lower case, words separated with hyphens'.

### Version 9.1

To make use of Quaqua 9.1 via Maven, add the following dependency to your pom.xml:

<font size="-1">
<pre>
    &lt;dependency&gt;
        &lt;groupId&gt;org.devzendo&lt;/groupId&gt;
        &lt;artifactId&gt;quaqua&lt;/artifactId&gt;
        &lt;version&gt;9.1&lt;/version&gt;
    &lt;/dependency&gt;
</pre>
</font>

Ensure that org.devzendo quaqua-9.1.jar is on your classpath.

Ensure that the org.devzendo libquaqua-9.1.zip containing Quaqua's native
libraries is unzipped during your package phase, and is available on your classpath during execution.
In the following snippet, I extract this zip into the location where our [Cross-Platform Launcher Plugin]({{ base_path }}/dev/xplp)
will place all libraries, for a Mac OSX GUI .app:

<font size="-1">
<pre>
    &lt;!--
      Copy the Quaqua native libraries into the correct location in the
      Mac OS X launcher structure created above.
    --&gt;
    &lt;plugin&gt;
        &lt;groupId&gt;org.apache.maven.plugins&lt;/groupId&gt;
        &lt;artifactId&gt;maven-dependency-plugin&lt;/artifactId&gt;
        &lt;executions&gt;
            &lt;execution&gt;
                &lt;id&gt;unpack-quaqua-dependencies&lt;/id&gt;
                &lt;phase&gt;package&lt;/phase&gt;
                &lt;goals&gt;
                    &lt;goal&gt;unpack&lt;/goal&gt;
                &lt;/goals&gt;
                &lt;configuration&gt;
                    &lt;artifactItems&gt;
                        &lt;artifactItem&gt;
                            &lt;groupId&gt;org.devzendo&lt;/groupId&gt;
                            &lt;artifactId&gt;libquaqua&lt;/artifactId&gt;
                            &lt;version&gt;9.1&lt;/version&gt;
                            &lt;type&gt;zip&lt;/type&gt;
                            &lt;overWrite&gt;true&lt;/overWrite&gt;
                            &lt;includes&gt;*&lt;/includes&gt;
                            &lt;outputDirectory&gt;
                                ${project.build.directory}/macosx/${appName}.app/Contents/Resources/Java/lib
                            &lt;/outputDirectory&gt;
                        &lt;/artifactItem&gt;
                    &lt;/artifactItems&gt;
                    &lt;!-- other configurations here --&gt;
                &lt;/configuration&gt;
            &lt;/execution&gt;
        &lt;/executions&gt;
    &lt;/plugin&gt;
</pre>
</font>

(See the [Cross-Platform Launcher Plugin]({{ base_path }}/dev/xplp) page for more information.)

### Version 7.3.4

To make use of Quaqua 7.3.4 via Maven, add the following dependency to your pom.xml:

<font size="-1">
<pre>
    &lt;dependency&gt;
        &lt;groupId&gt;org.devzendo&lt;/groupId&gt;
        &lt;artifactId&gt;Quaqua&lt;/artifactId&gt;
        &lt;version&gt;7.3.4&lt;/version&gt;
    &lt;/dependency&gt;
</pre>
</font>

Ensure that org.devzendo Quaqua-7.3.4.jar is on your classpath.

Ensure that the org.devzendo LibQuaqua-7.3.4.zip containing Quaqua's native
libraries is unzipped during your package phase, and is available on your classpath during execution.
In the following snippet, I extract this zip into the location where our [Cross-Platform Launcher Plugin]({{ base_path }}/dev/xplp)
will place all libraries, for a Mac OSX GUI .app:

<font size="-1">
<pre>
    &lt;!--
      Copy the Quaqua native libraries into the correct location in the
      Mac OS X launcher structure created above.
    --&gt;
    &lt;plugin&gt;
        &lt;groupId&gt;org.apache.maven.plugins&lt;/groupId&gt;
        &lt;artifactId&gt;maven-dependency-plugin&lt;/artifactId&gt;
        &lt;executions&gt;
            &lt;execution&gt;
                &lt;id&gt;unpack-quaqua-dependencies&lt;/id&gt;
                &lt;phase&gt;package&lt;/phase&gt;
                &lt;goals&gt;
                    &lt;goal&gt;unpack&lt;/goal&gt;
                &lt;/goals&gt;
                &lt;configuration&gt;
                    &lt;artifactItems&gt;
                        &lt;artifactItem&gt;
                            &lt;groupId&gt;org.devzendo&lt;/groupId&gt;
                            &lt;artifactId&gt;LibQuaqua&lt;/artifactId&gt;
                            &lt;version&gt;7.3.4&lt;/version&gt;
                            &lt;type&gt;zip&lt;/type&gt;
                            &lt;overWrite&gt;true&lt;/overWrite&gt;
                            &lt;includes&gt;*&lt;/includes&gt;
                            &lt;outputDirectory&gt;
                                ${project.build.directory}/macosx/${appName}.app/Contents/Resources/Java/lib
                            &lt;/outputDirectory&gt;
                        &lt;/artifactItem&gt;
                    &lt;/artifactItems&gt;
                    &lt;!-- other configurations here --&gt;
                &lt;/configuration&gt;
            &lt;/execution&gt;
        &lt;/executions&gt;
    &lt;/plugin&gt;
</pre>
</font>

(See the [Cross-Platform Launcher Plugin]({{ base_path }}/dev/xplp) page for more information.)

## Using Quaqua in your code

In your code, you can then:

UIManager.setLookAndFeel("ch.randelshofer.quaqua.QuaquaLookAndFeel");

## Mavenisation scripts

The scripts used to prepare the Mavenised artifacts and deploy them to the Central Repository are available from <a href="https://github.com/devzendo/quaqua">their Git repository</a>.


