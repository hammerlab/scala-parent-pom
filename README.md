# scala-parent-pom
POM with miscellaneous boilerplate for Scala 2.11.8 projects:
- build/output-directory configuration.
- disable surefire plugin, enable (and depend on) ScalaTest.
- configure scala (incremental) compilation.
- `coverage` profile, activated automatically on Travis CI, for computing code-coverage and reporting to Coveralls.
- `release` profile, containing release, source jar, java-doc, GPG plugins, and more.
- `2.10` profile: switches to Scala 2.10.6.

Extend your POM from it like:

```
<parent>
  <groupId>org.hammerlab</groupId>
  <artifactId>scala-parent-pom</artifactId>
  <version>1.0.0</version>
  <relativePath />
</parent>
```
