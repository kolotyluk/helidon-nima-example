# helidon-nima-example
Helidon Níma Example - Loom based webserver
This example is built on top of an ALPHA-1 release of Helidon 4. Alpha releases serve as prototypes or technology demonstration.

The code is not yet production quality in all of its aspects, and problems may be expected.

Nevertheless, if you encounter an issue with Helidon, please kindly report it at https://github.com/oracle/helidon/issues/new 

## Prerequisites
Java 19 with preview feature "Loom" (now available as RC at https://jdk.java.net/19/)
Maven

### Mac OS

     export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk-19.jdk/Contents/Home

or wherever JDK 19 or newer is

## How to

1. Build the project from the repository root
 
        mvn clean package
2. Run the application

        java --enable-preview -jar nima/target/example-nima-blocking.jar
3. Call the endpoints (default count is 3)

        curl -i http://localhost:8080/one
        curl -i http://localhost:8080/sequence
        curl -i http://localhost:8080/sequence?count=4
        curl -i http://localhost:8080/parallel
        curl -i http://localhost:8080/parallel?count=2
