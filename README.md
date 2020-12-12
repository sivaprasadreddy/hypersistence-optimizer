# Hypersistence Optimizer

[Hypersistence Optimizer](https://vladmihalcea.com/hypersistence-optimizer/) is a dynamic analyzing tool that can scan your JPA and Hibernate application and provide you tips about the changes you need to make to entity mappings, configurations, queries, and Persistence Context actions to speed up your data access layer.

Once you downloaded the [Full or Trial version](https://vladmihalcea.com/hypersistence-optimizer/), you need to follow a series of steps in order to install Hypersistence Optimizer.

## Unzipping the package

The first thing you need to do is to unzip the package you have just downloaded.

```bash
> unzip hypersistence-optimizer-2.2.0-pack.zip
```

After unzipping the project package, you will get the following file structure:

```bash
creating: hypersistence-optimizer-2.2.0/
   creating: hypersistence-optimizer-2.2.0/lib/
  inflating: hypersistence-optimizer-2.2.0/lib/hypersistence-optimizer-2.2.0-javadoc.jar
  inflating: hypersistence-optimizer-2.2.0/lib/hypersistence-optimizer-2.2.0-sources.jar
  inflating: hypersistence-optimizer-2.2.0/lib/hypersistence-optimizer-2.2.0.jar
   creating: hypersistence-optimizer-2.2.0/configs/
   creating: hypersistence-optimizer-2.2.0/configs/META-INF/
   creating: hypersistence-optimizer-2.2.0/configs/META-INF/services/
  inflating: hypersistence-optimizer-2.2.0/configs/META-INF/services/org.hibernate.boot.spi.SessionFactoryBuilderFactory
   creating: hypersistence-optimizer-2.2.0/docs/
   creating: hypersistence-optimizer-2.2.0/docs/html/
   creating: hypersistence-optimizer-2.2.0/docs/pdf/
  inflating: hypersistence-optimizer-2.2.0/docs/html/asciidoctor.css
  inflating: hypersistence-optimizer-2.2.0/docs/html/coderay-asciidoctor.css
  inflating: hypersistence-optimizer-2.2.0/docs/pdf/InstallationGuide.pdf
  inflating: hypersistence-optimizer-2.2.0/docs/html/InstallationGuide.html
  inflating: hypersistence-optimizer-2.2.0/docs/html/UserGuide.html
  inflating: hypersistence-optimizer-2.2.0/docs/pdf/UserGuide.pdf
  inflating: hypersistence-optimizer-2.2.0/changelog.txt
  inflating: hypersistence-optimizer-2.2.0/LICENSE.txt
  inflating: hypersistence-optimizer-2.2.0/maven-install.bat
  inflating: hypersistence-optimizer-2.2.0/maven-install.sh
  inflating: hypersistence-optimizer-2.2.0/README.txt
```

The package contains the following resources:

* the `lib` folder contains the main `jar` file, as well as the JavaDoc and the Java sources
* the `configs` folder contains a Java service loader configuration file that is going to be explained in the next steps
* the `docs` folder contains the Installation and User Guides
* the `changelog` file contains the release notes for all product versions
* the `LICENSE` file contains the project license info
* the `maven-install` scripts allow you to install the Java artifacts in your local Maven repository
* the `README` file contains a short description of the project

## Installation Guide

In order to install Hypersistence Optimizer, you need to read the Installation Guide, which is available both in
HTML and PDF formats in the unzipped package:

* `hypersistence-optimizer-2.2.0/docs/pdf/InstallationGuide.pdf`
* `hypersistence-optimizer-2.2.0/docs/html/InstallationGuide.html`

> You can also read the [Installation Guide online](https://vladmihalcea.com/hypersistence-optimizer/docs/installation-guide/) if you want.

## User Guide

After you are done with the Installation Guide, you should read the User Guide too, as it shows how you can configure
Hypersistence Optimizer so that you can get the most out of it.

You can find the User Guide in the docs folder as well:

* `hypersistence-optimizer-2.2.0/docs/html/UserGuide.html`
* `hypersistence-optimizer-2.2.0/docs/pdf/UserGuide.pdf`

> You can also read the [User Guide online](https://vladmihalcea.com/hypersistence-optimizer/docs/user-guide/) if you want.

## GitHub repository

This repository contains examples for Spring Boot, Spring Framework, Java EE that can help you set up the tool.

### Full vs. Trial version

By default, this repository is configured for the Full version. 

If you want to use it with the Trial version, you should use the `trial` branch instead:

```bash
> git checkout trial
```

> You should check out the entire repository since the child modules use the versions defined in the parent module `pom.xml`.

### Module descriptions

There are multiple modules in this repository:

- `hypersistence-optimizer-test-case`
- `hypersistence-optimizer-config-example`
- `hypersistence-optimizer-spring-boot-example`
- `hypersistence-optimizer-spring-jpa-example`
- `hypersistence-optimizer-spring-jpa-hibernate4-example`
- `hypersistence-optimizer-spring-jpa-hibernate3-example`
- `hypersistence-optimizer-spring-hibernate-example`
- `hypersistence-optimizer-spring-hibernate4-example`
- `hypersistence-optimizer-spring-hibernate3-example`
- `hypersistence-optimizer-glassfish-hibernate-example`
- `hypersistence-optimizer-glassfish-hibernate4-example`

### `hypersistence-optimizer-test-case`

This module provides a test case template you could use to replicate a certain Hypersistence Optimizer issue.

### `hypersistence-optimizer-config-example`

This module shows various examples of how you can configure Hypersistence Optimizer.

### `hypersistence-optimizer-spring-boot-example`

This module shows how you can use Hypersistence Optimizer with Spring Boot.

### `hypersistence-optimizer-spring-jpa-example`

This module shows how you can use Hypersistence Optimizer with Spring and the JPA `LocalEntityManagerFactoryBean`.

### `hypersistence-optimizer-spring-jpa-hibernate4-example`

This module shows how you can use Hypersistence Optimizer with Spring, the JPA `LocalEntityManagerFactoryBean`, and Hibernate 4.

### `hypersistence-optimizer-spring-jpa-hibernate3-example`

This module shows how you can use Hypersistence Optimizer with Spring, the JPA `LocalEntityManagerFactoryBean`, and Hibernate 3.

### `hypersistence-optimizer-spring-hibernate-example`

This module shows how you can use Hypersistence Optimizer with Spring and the Hibernate `LocalSessionFactoryBean`.

### `hypersistence-optimizer-spring-hibernate4-example`

This module shows how you can use Hypersistence Optimizer with Spring and the Hibernate 4 `LocalSessionFactoryBean`.

### `hypersistence-optimizer-spring-hibernate3-example`

This module shows how you can use Hypersistence Optimizer with Spring and the Hibernate 3 `LocalSessionFactoryBean`.

### `hypersistence-optimizer-glassfish-hibernate-example`

This module shows how you can use Hypersistence Optimizer with Java EE and GlassFish.

### `hypersistence-optimizer-glassfish-hibernate4-example`

This module shows how you can use Hypersistence Optimizer with Java EE, GlassFish, and Hibernate 4.

## How to run tests?

* Install JDK 8
* Install and run MySQL server on localhost with following configuration:
    * DatabaseName: high_performance_java_persistence
    * Port: 3306
    * UserName: mysql
    * Password: admin
 
    You can use **docker-compose** for running mysql server using the command: `hypersistence-optimizer> docker-compose up`
* Run tests: `hypersistence-optimizer> mvn clean install`

## Issue management

If you'd like to create a new issue, be it a feature request or simply reporting a bug, then you can use [this GitHub repository issue list](https://github.com/vladmihalcea/hypersistence-optimizer/issues).

For bugs, it would be awesome if you provided a replicating test case as well. You can use the `EagerFetchingManyToOneTest` as a template to create your new test case scenario.

When you are done, please send your test case as a Pull Request, and I'll take care of it.

Thank you for using Hypersistence Optimizer and stay tuned for more!
