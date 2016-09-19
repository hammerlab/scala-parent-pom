# scala-parent-pom

[![Maven Central](https://img.shields.io/maven-central/v/org.hammerlab/scala-parent-pom.svg?maxAge=25920)](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.hammerlab%22%20AND%20a%3A%22scala-parent-pom%22)

POM with miscellaneous boilerplate for Scala projects:
- defaults to Scala 2.11.8, but can be made to use 2.10.6 by enabling the `2.10` profile.
  - see [hammerlab/magic-rdds](https://github.com/hammerlab/magic-rdds#building) for an example simultaneously maintaining 2.10 and 2.11 versions through build and release processes.
- build/output-directory configuration.
- disable surefire plugin, enable (and depend on) ScalaTest.
- configure scala (incremental) compilation.
- `github.repo` property fills out `<licenses>` and `<scm>` blocks automatically.
- `coverage` profile, activated automatically on Travis CI, for computing code-coverage and reporting to Coveralls.
- `release` profile, containing release, source jar, java-doc, GPG plugins, and more.

Extend your POM from it like:

```
<parent>
  <groupId>org.hammerlab</groupId>
  <artifactId>scala-parent-pom</artifactId>
  <version>1.0.3</version>
  <relativePath />
</parent>
```
