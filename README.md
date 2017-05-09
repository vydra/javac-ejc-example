# javac-ejc-example

Demonstrates how to create a simple java app and switch between javac and Eclipse Java Compiler while using the local build cache.

## Running the code

Using javac: ./gradlew test --build-cache

Using ECJ: ./gradlew test --build-cache -Decj

## How the project was started

git clone git@github.com:vydra/sample-gradle-java-app.git
cd sample-gradle-java-app/
gradle wrapper --gradle-version 3.5
gw init --type java-application