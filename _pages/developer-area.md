---
permalink: /developer-area/
title: "Libraries and Tools"
excerpt: "The materials of craftsmanship."
author_profile: false
---

{% include base_path %}

These pages are intended for software developers, not end-users. If you are here looking for our Open Source applications, please visit the [applications]({{ base_path }}/applications/) page.

There are several Open Source projects available here - the following pages will give you more information about the projects,
how to use them, how to get involved with their development, source code repositories, and mailing lists.

Recently we have started publishing via the <a href="http://search.maven.org/#search|ga|1|org.devzendo">Central Maven Repository</a>, under the **org.devzendo** group id.
See below for signing details.

For our earlier releases, you will need to [enable our Maven 2 Repositories]({{ base_path }}/dev/maven-2-repositories).

## Frameworks and Tools

* The [Common Database Framework]({{ base_path }}/dev/common-db) is a small Scala wrapper around Spring-JDBC and the embedded H2 database, to abstract out the common operations of creating, opening, upgrading, and closing embedded relational databases, and working with the DAO pattern. The ideas here were first expressed in part of the <a href="/content/minimiser-framework">MiniMiser Framework</a>, but in Java.
* The [Cross-Platform Launcher Plugin]({{ base_path }}/dev/xplp) is a Maven plugin for generating application launchers for Windows, Mac OS X, and Ubuntu Linux, based on some elementary configuration, and a list of dependencies.

 
## Third party Mavenisations

* The [Quaqua Look and Feel library]({{ base_path }}/dev/mavenised-quaqua)


## Signing

Artifacts in the central repository are signed by Matt Gumbley: 

*  Mail address is at gumbley dot me dot uk, the address being matt, (if you see what I mean!)
*  GPG key ID is 0x5BF15889
*  GPG fingerprint 0A86 31FA 90FD 263B D7C8  E16E B6F3 E26A 5BF1 5889
*  Public key is available from most fine key servers, e.g. from <a href="http://pgp.mit.edu:11371/pks/lookup?op=get&amp;search=0xB6F3E26A5BF15889">pgp.mit.edu</a>, and is posted below should you wish to import it directly:


<pre>
-----BEGIN PGP PUBLIC KEY BLOCK-----
Version: SKS 1.1.0

mQGiBEClOUERBADEjawglzTNZmGLbIdpQqORF2CBsv4VcH6//wgVJdANvMoh6nTsDWLJj8rq
ZECg6yW0USoiOp4lSkiinOAIjwGrHYUeFiBZo0sm+2yqStuBuaRC6+ZGVKtHp3cnKawMqXqq
jHr2M4fAMBqd+Hn4zF0wxz99QGn3KkX6ivUrVaNgiwCgzpErCF3ImkqZjwR2i4vrftgniAED
/2DrbppLue3jxjTjfUR+eQ35Hhzz0fVfcLjyNgOjUWsllNsfYZLumHacEQi2pIDQpLyY00C2
6wi5NPPQvshCtSKwyFG4LKjbVbiNn1LHzZF4pHpcYitOXilR09ZAGkFQyB1XmWT6M1PO2o8E
53feA98VroJ78xQ7ZGqtMKE4Z4pbA/9a9oCpWJ/xp1zJNRwjqZAChm50f3djTHHIzwOJiqll
8j4GLYzAvPJPG6kSgkO8kSHi/nA78bVrtKRSx392X9VbKEEm51ocKt7W0X+myrLPBIpXwTC7
m3mH0ospAkLNfalZFUeGk5TBVrBTtXw95yPoe8PpSaOLilHDjfS5P9bH6rQhTWF0dCBHdW1i
bGV5IDxtYXR0QGd1bWJsZXkubWUudWs+iF4EExECAB4FAkClOUECGwMGCwkIBwMCAxUCAwMW
AgECHgECF4AACgkQtvPialvxWImp4gCfZh9DKN81yyQ7bmmP0FoJPWLLkkMAoJxkmdIRXz9j
OG0LhPkG0AtNtQDruQENBEClOUUQBACQIwurA+S9IRMLLRzJzmJNIghSInRuZg9E52EajKoJ
SP1KNLPWwR2uxxQu23l7VodkZOvP3+CLYW5acQZTBd2XJECdQGNvvDh2c0aXtyecmor24Ekp
28uSLKmyo6LUkXS+Gw1vdcgm0WhC0J+LRUvEcBRQugVMkfv8Oa67OQLcNwADBwP9H/YwJ+gh
en4b0A+mD+O5dXJEhsQIg6rlPiZxmmf92D+2bxhZE1v2fPF2uq+50LQsb3UDbcij4EmolJci
Mn1O4kV/0BKBGOEJ88pciTj+g2CEryI/a6sDY/jHwGXB4YSDo2dz0VdVZTN33a+AHfymXupE
0KY3UjFGy3K0XQBQmZ2ISQQYEQIACQUCQKU5RQIbDAAKCRC28+JqW/FYiZL3AKC1F4SNjvSy
2oaMFWIy8kqYs3pwvACbBn5W/+6XW9OBAg+/q5xh6y7vmZ8=
=q4bu
-----END PGP PUBLIC KEY BLOCK-----
</pre>

TODO
