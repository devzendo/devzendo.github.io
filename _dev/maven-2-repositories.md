---
permalink: /dev/maven-2-repositories/
title: "Older repositories"
excerpt: "Deprecated."
author_profile: false
---

{% include base_path %}

Recent DevZendo.org software is <a href="http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22org.devzendo%22">deployed in the central Maven 2 repository</a>, thanks to Sonatype's upload process.

Earlier DevZendo.org software is not yet deployed in the central Maven 2 repository, so in order to make use of it via Maven, you will need to add the DevZendo.org Maven repositories to your development environment.

There are also a number of third-party libraries hosted in the DevZendo.org repository since they are not yet available from the central Maven repository:
<ul>
<li>org.netbeans:wizard - see <a href="https://wizard.dev.java.net/">its home page</a> for details.</li>
<li>ch.randelshofer:quaqua - see <a href="http://www.randelshofer.ch/quaqua/">its home page</a> for details.</li>
</ul>

To add our repositories, you will need to modify your settings.xml file. This can be found in the following locations on different platforms:
<dl>
<dt>Windows up to XP</dt>
<dd>C:\Documents and Settings\username\.m2\settings.xml</dd>
<dt>Windows Vista and above (untested)</dt>
<dd>C:\Users\username\.m2\settings.xml</dd>
<dt>Mac OS X</dt>
<dd>/Users/username/.m2/settings.xml</dd>
<dt>Linux</dt>
<dd>/home/username/.m2/settings.xml</dd>
</dl>

The following settings.xml establishes a 'default' profile, sets it as the active profile and adds our snapshot and releases repositories.
<font size="-1">
<pre>
&lt;settings&gt;
  &lt;activeProfiles&gt;
    &lt;activeProfile&gt;default&lt;/activeProfile&gt;
  &lt;/activeProfiles&gt;
  &lt;profiles&gt;
    &lt;profile&gt;
      &lt;id&gt;default&lt;/id&gt;
      &lt;repositories&gt;
        &lt;repository&gt;
          &lt;id&gt;devzendo-org-repository-releases&lt;/id&gt;
          &lt;name&gt;DevZendo.org Maven2 releases Repository on Google Code&lt;/name&gt;
          &lt;url&gt;http://devzendo-org-repo.googlecode.com/svn/trunk/releases&lt;/url&gt;
          &lt;snapshots&gt;
              &lt;enabled&gt;false&lt;/enabled&gt;
          &lt;/snapshots&gt;
          &lt;releases&gt;
              &lt;enabled&gt;true&lt;/enabled&gt;
          &lt;/releases&gt;
        &lt;/repository&gt;
        &lt;repository&gt;
          &lt;id&gt;devzendo-org-repository-snapshots&lt;/id&gt;
          &lt;name&gt;DevZendo.org Maven2 Snapshots Repository on Google Code&lt;/name&gt;
          &lt;url&gt;http://devzendo-org-repo.googlecode.com/svn/trunk/snapshots&lt;/url&gt;
          &lt;snapshots&gt;
              &lt;enabled&gt;true&lt;/enabled&gt;
          &lt;/snapshots&gt;
          &lt;releases&gt;
              &lt;enabled&gt;false&lt;/enabled&gt;
          &lt;/releases&gt;
        &lt;/repository&gt;
      &lt;/repositories&gt;

      &lt;pluginRepositories&gt;
        &lt;pluginRepository&gt;
          &lt;id&gt;devzendo-org-repository-plugin-releases&lt;/id&gt;
          &lt;name&gt;DevZendo.org Maven2 releases Repository on Google Code&lt;/name&gt;
          &lt;url&gt;http://devzendo-org-repo.googlecode.com/svn/trunk/releases&lt;/url&gt;
          &lt;snapshots&gt;
              &lt;enabled&gt;false&lt;/enabled&gt;
          &lt;/snapshots&gt;
          &lt;releases&gt;
              &lt;enabled&gt;true&lt;/enabled&gt;
          &lt;/releases&gt;
        &lt;/pluginRepository&gt;
      &lt;/pluginRepositories&gt;

    &lt;/profile&gt;
  &lt;/profiles&gt;
&lt;/settings&gt;
</pre>
</font>

So, to download all necessary artifacts for your project, and package its jar using the default profile above: `mvn package`



