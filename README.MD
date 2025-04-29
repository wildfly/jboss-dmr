# JBoss DMR

JBoss DMR (Dynamic Model Representation) is a Java library that provides a simple API to build up arbitrarily complex data structures using a small number of Java types.

It is a foundational piece of [WildFly](https://wildfly.org) which uses JBoss DMR to represent its large and complex management model.

JBoss DMR is released as a single Maven artifact with the coordinates:

```
<dependency>
    <groupId>org.jboss</groupId>
    <artifactId>jboss-dmr</artifactId>
</dependency>
```

# Build JBoss DMR

Prerequisites:

* JDK 11 or newer - check `java -version`
* Maven 3.6.0 or newer - check `mvn -v`

To build with your own Maven installation:

```
mvn package
```

# Reporting Issues

JBoss DMR uses JIRA to manage issues. All issues can be found [here](https://issues.redhat.com/projects/DMR/issues).

To create a new issue, comment on an existing issue, or assign an issue to yourself, you'll need to first [create a JIRA account](https://issues.redhat.com/).

# Release Procedure

JBoss DMR is released in [JBoss Nexus Repository](https://repository.jboss.org/nexus/)

To release a new version of JBoss DMR:

* Use the Maven [`release` plugin](https://maven.apache.org/maven-release/maven-release-plugin/):

```
mvn release:prepare
mvn release:perform
```

* Close and publish the staged artifacts from  [JBoss Nexus Repository](https://repository.jboss.org/nexus/)
* Release the published version in [JIRA](https://issues.redhat.com/projects/DMR?selectedItem=com.atlassian.jira.jira-projects-plugin:release-page&status=released-unreleased)
* Update the Release Notes in [GitHub Release page](https://github.com/wildfly/jboss-dmr/releases)


