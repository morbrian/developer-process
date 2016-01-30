# Project Developer Guidelines

## Table of Contents

* [Overview](#overview)
* [Developer Workflow](#develper-workflow)
    * [Git Process](#git-process)
    * [Repository Guidelines](#repository-guidelines)
* [Java Programming](#java-programming)
    * [Code Style](#code-style)
    * [Dependency Management](#dependency-management)
    * [Unit Tests](#unit-tests)
    * [Integration Tests](#integration-tests)
* [Swift Programming](#swift-programming)
    * [Code Style](#code-style)
    * [Dependency Management](#dependency-management)
    * [Unit Tests](#unit-tests)
    * [Integration Tests](#integration-tests)

## Configuration Overview

This document provides the basic developer guidelines for my github repositories. Although these are my preferred best practice guidelines for my GitHub repositories, I frequently find myself using other practices and workflows depedending on customer needs, legacy conventions and tools available to other environments. In other words, while these are my preferred personal best practices, I do understand the value of alternate tools and work flows.

# Java
## Code Style

Project developers use the [Google Java Style](http://google.github.io/styleguide/javaguide.html) found at GitHub.

* [Eclipse Code Style Configuration](https://github.com/google/styleguide/blob/gh-pages/eclipse-java-google-style.xml)

        Import into eclipse.

* [IntelliJ Code Style Configuration](https://github.com/google/styleguide/blob/gh-pages/eclipse-java-google-style.xml)

        Import this eclipse XML into IntelliJ. After import, the line indent will still be set to 4, edit and change to 2.

## Dependency Management        

All Java based repositories should use Maven.

1) Dependencies should be ordered such that:

        - sibling modules are listed first.
        - 3rd party modules second.
        - test scoped modules last.
        - otherwise, list alphabetically by groupId-artifactId within each of the above categories.
       
2) Dependencies which are not scoped as `test` should never list a version in child poms,
instead add the correct version to the parent pom's `dependencyManagement`. 

## Unit Tests

All public methods must have an associated JUnit test. Developers may optionally provide unit
tests for protected and private methods.

## Integration Tests

TODO: identify integration test strategy. I have been using Arquillian lately and I like it, but this section needs a bit more detail.
        




