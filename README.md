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
:processResources
:classes
:compileTestJava
:compileTestJava - is not incremental (e.g. outputs have changed, no previous execution, etc.).
:processTestResources NO-SOURCE
:testClasses
:test

BUILD SUCCESSFUL
```

### 2nd run - notice 43% from cache

```
7 tasks in build, out of which 0 (0%) were executed
2  (29%) up-to-date
2  (29%) no-source
3  (43%) loaded from cache
```

### 3rd run - everything is now up-to-date or no-source

```
7 tasks in build, out of which 0 (0%) were executed
5  (71%) up-to-date
2  (29%) no-source
```

## How the project was started

git clone git@github.com:vydra/sample-gradle-java-app.git
cd sample-gradle-java-app/
gradle wrapper --gradle-version 3.5
gw init --type java-application