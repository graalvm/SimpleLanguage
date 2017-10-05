# SimpleLanguage

A simple demonstration language built using Truffle for the GraalVM.

SimpleLanguage is heavily documented to explain the how and why of writing a
Truffle language. A good way to read this documentation is to generate HTML of
the JavaDoc comments and read that, and then read the source alongside the
comments.

This repository is licensed under the permissive UPL licence. Fork it to begin
your own Truffle language.

## Prerequisites
* JDK 8
* [maven3](https://maven.apache.org/download.cgi)

## Installation

* Clone SL repository using
  `git clone https://github.com/graalvm/simplelanguage`
* Download Graal VM Development Kit from
  http://www.oracle.com/technetwork/oracle-labs/program-languages/downloads
* Unpack the downloaded `graalvm_*.tar.gz` into `simplelanguage`
* Verify that the file `simplelanguage/graalvm/bin/java` exists and is executable
* Change into the `simplelanguage` directory
* Execute `mvn package`

## Running

* Execute `./sl tests/HelloWorld.sl` to run a simple language source file
* Execute `./sl -disassemble tests/SumPrint.sl` to see assembly code for Truffle compiled functions

## IGV

* Download the Ideal Graph Visualizer (IGV) from
  https://lafo.ssw.uni-linz.ac.at/pub/idealgraphvisualizer/
* Unpack the downloaded `.zip` file
* Change into the `idealgraphvsiualizer` directory
* Execute `bin/idealgraphvsiualizer` to start IGV. In case IGV selects JDK9 and shows this exception `InaccessibleObjectException` , you can set `jdkhome` to JDK8 with
`export jdkhome=/Library/Java/JavaVirtualMachines/jdk`
* Execute `./sl -dump tests/SumPrint.sl` to dump graphs to IGVc

## Debugging

* Execute `./sl -debug tests/HelloWorld.sl`
* Attach a Java remote debugger (like Eclipse) on port 8000

## IDE Setup

### Eclipse
* Tested with Eclipse Mars SR2
* Open Eclipse with a new workspace
* Install `m2e` *Maven integration for Eclipse* and `m2e-apt` plugins from the Eclipse marketplace (Help -> Eclipse Marketplace...)
* File -> Import... -> Maven -> Existing Maven Projects -> Select `simplelanguage` folder -> Finish

### Netbeans
* Tested with Netbeans 8.1
* Open Netbeans
* File -> Open Project -> Select `simplelanguage` folder -> Open Project

### IntelliJ IDEA
* Tested with IntelliJ 2016.1.3 Community Edition
* Open IntelliJ IDEA
* File -> New -> Project from existing Sources -> Select `simplelanguage` folder -> Click next and keep everything default on several screens -> Finish

## Tested Compatibility

Simple language is compatible to:

* Truffle-Version: 0.28
* GraalVM-Version: 0.28


## Further information

* [Truffle JavaDoc](http://lafo.ssw.uni-linz.ac.at/javadoc/truffle/latest/)
* [Truffle on Github](http://github.com/graalvm/truffle)
* [Graal on Github](http://github.com/graalvm/graal-core)
* [Truffle Tutorials and Presentations](https://wiki.openjdk.java.net/display/Graal/Publications+and+Presentations)
* [Truffle FAQ and Guidelines](https://wiki.openjdk.java.net/display/Graal/Truffle+FAQ+and+Guidelines)
* [Graal VM]( http://www.oracle.com/technetwork/oracle-labs/program-languages/overview) on the Oracle Technology Network
* [Papers on Truffle](http://ssw.jku.at/Research/Projects/JVM/Truffle.html)
* [Papers on Graal](http://ssw.jku.at/Research/Projects/JVM/Graal.html)

## License

The Truffle framework is licensed under the [GPL 2 with Classpath exception](http://openjdk.java.net/legal/gplv2+ce.html).
The SimpleLanguage is licensed under the [Universal Permissive License (UPL)](http://opensource.org/licenses/UPL).
