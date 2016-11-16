---
permalink: /dev/common-db/
title: "Common Database Access"
excerpt: "Typesafe access to embedded databases."
author_profile: false
---

{% include base_path %}

## About
The <em>Common Database Framework</em> is a Scala library that allows developers to store application data in an embedded relational database. 
It simplifies creation, opening, migrating to updated schemas, data access, and transaction handling. 
It mixes the H2 database engine with Spring-JDBC, in a type-safe style.



## Resources

* **License:** <a href="http://www.apache.org/licenses/LICENSE-2.0.html">Apache License v2</a>
* **Documentation:** <a href="https://devzendo@bitbucket.org/devzendo/common-db/src/4c4121f4c10044b6dc8b46a1e34275f2157d1472/docs/Framework%20user%20guide%200.1.1.pdf?at=default">Framework User Guide</a> \[PDF\]
* **Change history**: [change history]({{ base_path }}/dev/commondb-change-history).
* **Current release:** 0.1.1 for Scala 2.10
* **Release announcements:**
  * [0.1.1 18 September 2013]({{ base_path }}/development/commondb-0.1.1)
* **Release schedule:** The plugin is released as part of the [DevZendo.org release schedule]({{ base_path }}/dev/release-schedule) which allows for 8 releases per year.
* **Availability**: This is available from the <a href="http://search.maven.org/#browse%7C-125156780">Central Maven Repository</a>
* **Source code:** <a href="https://devzendo@bitbucket.org/devzendo/commondb">Mercurial source repository, hosted on Bitbucket
* **Contact:** there is no mailing list at the moment, please use the [contact us page]({{ base_path }}/contact), or <a href="http://twitter.com/devzendo">follow/tweet to us on Twitter</a>.


## Acknowledgements

The framework is built from many fine Open Source / Free Software components:

* [The Scala Programming Language](http://www.scala-lang.org/)
* [H2 Database Engine](http://www.h2database.com/)
* [Spring Framework](http://www.springsource.org/documentation)
* [Log4J](http://logging.apache.org/log4j/)
* [The Simple Logging Framework for Java](http://www.slf4j.org/)
* [Apache Commons-Lang](http://commons.apache.org/lang/)

We also make use of the following tools:

* [The IntelliJ IDEA IDE (Community Edition)](http://www.jetbrains.com/idea/)
* [Apache Maven](http://maven.apache.org/)
* [Mercurial](http://mercurial.selenic.com/)
* [Jenkins CI](https://jenkins.io/)
* [JUnit](http://www.junit.org/), [ScalaTest](http://scalatest.org), and [Easymock](http://easymock.org/)

<script type="text/javascript" src="http://www.ohloh.net/p/603200/widgets/project_basic_stats.js"></script>
