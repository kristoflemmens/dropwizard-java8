Dropwizard Java 8 Bundle
========================

[![Build Status](https://travis-ci.org/dropwizard/dropwizard-java8.svg?branch=master)](https://travis-ci.org/dropwizard/dropwizard-java8)
[![Coverage Status](https://img.shields.io/coveralls/dropwizard/dropwizard-java8.svg)](https://coveralls.io/r/dropwizard/dropwizard-java8)

An addon bundle and a set of classes for using Java 8 features like `Optional<T>` and the new Date/Time API (JSR-310) in a [Dropwizard](http://www.dropwizard.io/) application.

Currently it supports Java 8 versions of [dropwizard-auth](http://dropwizard.io/0.7.1/dropwizard-auth/) and [dropwizard-jdbi](http://dropwizard.io/0.7.1/dropwizard-jdbi/).


Usage
-----

Just add `Java8Bundle` to your [Application](http://dropwizard.io/0.7.1/dropwizard-core/apidocs/io/dropwizard/Application.html) class
as described in the manual in the [Bundles](http://dropwizard.io/0.7.1/docs/manual/core.html#man-core-bundles) paragraph.

This will add support for `Optional<T>` to Jersey and support for JSR-310 and `Optional<T>` to Jackson.

    public class DemoApplication extends Application<DemoConfiguration> {
        // [...]
        @Override
        public void initialize(Bootstrap<HelloWorldConfiguration> bootstrap) {
            bootstrap.addBundle(new Java8Bundle());
            // [...]
        }
    }


Maven Artifacts
---------------

This project is available on Maven Central. To add it to your project simply add the following dependencies to your
`pom.xml`:

    <dependency>
      <groupId>io.dropwizard.modules</groupId>
      <artifactId>dropwizard-java8</artifactId>
      <version>0.7.0-1</version>
    </dependency>

    <dependency>
      <groupId>io.dropwizard.modules</groupId>
      <artifactId>dropwizard-java8-auth</artifactId>
      <version>0.7.0-1</version>
    </dependency>

    <dependency>
      <groupId>io.dropwizard.modules</groupId>
      <artifactId>dropwizard-java8-jdbi</artifactId>
      <version>0.7.0-1</version>
    </dependency>


Support
-------

Please file bug reports and feature requests in [GitHub issues](https://github.com/dropwizard/dropwizard-java8/issues).


License
-------

Copyright (c) 2014 Jochen Schalanda

This library is licensed under the Apache License, Version 2.0.

See http://www.apache.org/licenses/LICENSE-2.0.html or the LICENSE file in this repository for the full license text.
