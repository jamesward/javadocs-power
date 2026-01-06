---
name: "javadocs"
displayName: "JavaDocs"
description: "Get JavaDoc for Java, Kotlin, and Scala libraries on Maven Central"
keywords: ["javadocs"]
author: "James Ward"
---

# Onboarding

## Step 1: Resolve Dependencies

Before using the javadocs MCP server, resolve the Maven Central artifacts (groupId, artifactId, version) used in the project.

Common build files to determine which build tool the project uses:

Maven = `pom.xml`
Gradle = `build.gradle` or `build.gradle.kts`
sbt = `build.sbt`

Resolve dependencies by running the build tool.

If build tool wrapper / launcher scripts exists, use it.

Maven Wrapper = `mvnw`
Gradle Wrapper = `gradlew`
sbt launcher = `sbt`

Maven Dependency List:
```
./mvnw dependency:list
```

Gradle Dependency List:
```
./gradlew dependencies
```

sbt Dependency List:
```
./sbt dependencyTree
```

# Best Practices

## When using the javadocs MCP server use project dependencies

When using the javadocs MCP server, specify the version of the dependency based on the resolved version.
Looking up the latest version via the javadocs MCP server should only be done if the version isn't known in the resolved dependencies.
