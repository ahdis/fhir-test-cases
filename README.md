# fhir-test-cases

| CI Status (master) | Release Pipeline | Current Release | Latest SNAPSHOT |
| :---: | :---: | :---: | :---: |
| [![Build Status][Badge-AzurePipeline]][Link-AzurePipeline] | [![Build Status][Badge-AzureReleasePipeline]][Link-AzureReleasePipeline] | [![Release Artifacts][Badge-SonatypeReleases]][Link-GithubZipRelease] | [![Snapshot Artifact][Badge-SonatypeSnapshots]][Link-SonatypeSnapshots] |

## CI/CD

All intergration and delivery done on Azure pipelines. Azure project can be viewed [here](https://dev.azure.com/fhir-pipelines/fhir-test-cases).

## Contents

This repository contains:

* r5: r5 test cases (actively maintained)
* r4: r4 test cases (not maintained)
* cda: test case CDA for roundtripping/validation based on FHIR definition of CDA
* ucum: source for ucum 
* validator - test cases for the cross-version validation
* target - maven administrative stuff

## Accessing the test cases

You can access the test cases via Maven. If using Maven doesn't suit, then 
another option is to download the test cases directly from 
https://github.com/FHIR/fhir-test-cases/releases/latest/download/testcases.zip


## Building this Project

This project uses [Apache Maven](http://maven.apache.org) to build. To build:

```
mvn install
```

Note: there's no java code in here. The fact that maven is used is just to make it easy to book up
other maven dependencies to the test cases 

## Publishing Binaries

An brief overview of our publishing process is [here][Link-Publishing].

For more detailed instructions on cutting a release, please read [the wiki][Link-PublishingRelease]

## Download

#### Maven
```xml
<dependency>
    <groupId>org.hl7.fhir.testcases</groupId>
    <artifactId>fhir-test-cases</artifactId>
    <version>(latest version)</version>
</dependency>
```

#### Gradle
```groovy
compile group: 'org.hl7.fhir.testcases', name: 'fhir-test-cases', version: '(latest version)'
```

## Releases
Releases and release notes are published to [GitHub][Link-GitHubReleases], and can also be downloaded from [Maven Central][Link-MavenCentralReleases].

## Maintenance
This project is maintained by the FHIR community to help implementations test their functionality.

[Link-MavenCentralReleases]: https://mvnrepository.com/artifact/org.hl7.fhir.testcases/fhir-test-cases
[Link-GitHubReleases]: https://github.com/FHIR/fhir-test-cases/releases
[Link-Publishing]: https://github.com/FHIR/fhir-test-cases/wiki/Publishing-Binaries
[Link-AzurePipeline]: https://dev.azure.com/fhir-pipelines/fhir-test-cases/_build/latest?definitionId=27&branchName=master
[Link-AzureReleasePipeline]: https://dev.azure.com/fhir-pipelines/fhir-test-cases/_build/latest?definitionId=28&branchName=master
[Link-GithubZipRelease]: https://github.com/FHIR/fhir-test-cases/releases/latest/download/testcases.zip "Sonatype Releases"
[Link-SonatypeSnapshots]: https://oss.sonatype.org/service/local/artifact/maven/redirect?r=snapshots&g=org.hl7.fhir.testcases&a=fhir-test-cases&v=LATEST "Sonatype Snapshots"
[Link-PublishingRelease]: https://github.com/FHIR/fhir-test-cases/wiki/Detailed-Release-Instructions

[Badge-AzureReleasePipeline]: https://dev.azure.com/fhir-pipelines/fhir-test-cases/_apis/build/status/Release%20Branch%20Pipeline?branchName=master
[Badge-AzurePipeline]: https://dev.azure.com/fhir-pipelines/fhir-test-cases/_apis/build/status/Master%20Branch%20Pipeline?branchName=master
[Badge-SonatypeReleases]: https://img.shields.io/nexus/r/https/oss.sonatype.org/org.hl7.fhir.testcases/fhir-test-cases.svg "Sonatype Releases"
[Badge-SonatypeSnapshots]: https://img.shields.io/nexus/s/https/oss.sonatype.org/org.hl7.fhir.testcases/fhir-test-cases.svg "Sonatype Snapshots"
