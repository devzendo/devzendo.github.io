---
permalink: /parachute-download/
title: "The Parachute Project: Downloads"
excerpt: "Portable Parallel Processing."
author_profile: false
---

{% include base_path %}

Download The Parachute Parallel Programming System

Free/Libre Open Source Software. Transputer Emulation/Virtual Machine & Languages.

{% assign version = 0.0.1-SNAPSHOT %}
{% assign repourl = https://repo.maven.apache.org/maven2/org/devzendo/transputer-emulator %}
{% assign baseurl = {{ repourl }}/{{ version }}/parachute-{{ version }}- %}

<p/>
<b>Current version: {{ version }}</b>
<p/>

<table>
<tbody>
<tr>
  <td><img src="/images/apple-logo-old-white.png" height=200 width=200></td>
  <td><img src="/images/ubuntu-logo32.png"height=200 width=200></td>
  <td><img src="/images/centos-logo-transparent.png"height=200 width=200></td>
  <td><img src="/images/raspberry-pi-logo-white.png"height=200 width=200></td>
  <td><img src="/images/windows-logo-transparent.png"height=200 width=200></td>
</tr>
<tr>
  <td bgcolor="#0000FF"><img src="/images/download-white.svg" width=18px height=18px>
    macOS
    <small>El Capitan</small>
  </td>
  <br/>
  <a href="{{ baseurl }}-mac-x86_64.tar.gz">Download .tar.gz</a>
</tr>
<tr>
  <td bgcolor="#0000FF"><img src="/images/download-white.svg" width=18px height=18px>
    Ubuntu LTS
    <small>16.04 (Xenial Xerus), 18.04 (Bionic Beaver)</small>
  </td>
  <br/>
  <a href="{{ baseurl }}-ubuntu-16.04-linux-x86_64.tar.gz">Download 16.04 .tar.gz</a>
  <br/>
  <a href="{{ baseurl }}-ubuntu-18.04-linux-x86_64.tar.gz">Download 18.04 .tar.gz</a>
</tr>
<tr>
  <td bgcolor="#0000FF"><img src="/images/download-white.svg" width=18px height=18px>
    CentOS
    <small>7.6</small>
  </td>
  <br/>
  <a href="{{ baseurl }}-centos-7-linux-x86_64.tar.gz">Download 7.6 .tar.gz</a>
</tr>
<tr>
  <td bgcolor="#0000FF"><img src="/images/download-white.svg" width=18px height=18px>
    Raspberry Pi
    <small>Raspbian Stretch</small>
  </td>
  <br/>
  <a href="{{ baseurl }}-raspbian-9-linux-arm_32.tar.gz">Download .tar.gz</a>
</tr>
<tr>
  <td bgcolor="#0000FF"><img src="/images/download-white.svg" width=18px height=18px>
    Windows
    <small>Windows 10</small>
  </td>
  <br/>
  <a href="{{ baseurl }}-windows-x86_64.zip">Download .zip</a>
</tr>
</tbody>
</table>

