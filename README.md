# javac-ejc-example

Demonstrates how to create a simple java app and switch between javac and Eclipse Java Compiler while using the local build cache.

## Running the code

Using javac: ./gradlew test --build-cache

Using ECJ: ./gradlew test --build-cache -Decj

## EJC compiler output

```
The executable property on ForkOptions has been deprecated and is scheduled to be removed in Gradle 5.0. Please use javaHome instead.
        at build_d74acwpy5zdrbywz1zdd98zfh$_run_closure3$_closure4.doCall(/Users/dvydra/dev/vydra/javac-ejc-example/build.gradle:45)
Build cache is an incubating feature.
Using directory (/Users/dvydra/.gradle/caches/build-cache-1) as local build cache, push is enabled.
:compileJava
:compileJava - is not incremental (e.g. outputs have changed, no previous execution, etc.).
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=128m; support was removed in 8.0
:processResources NO-SOURCE
:classes
:compileTestJava
:compileTestJava - is not incremental (e.g. outputs have changed, no previous execution, etc.).
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=128m; support was removed in 8.0
incorrect classpath: /Users/dvydra/dev/vydra/javac-ejc-example/build/resources/main
:processTestResources NO-SOURCE
:testClasses
:test

BUILD SUCCESSFUL
```

## How the project was started

git clone git@github.com:vydra/sample-gradle-java-app.git
cd sample-gradle-java-app/
gradle wrapper --gradle-version 3.5
gw init --type java-application