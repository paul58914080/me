## Install

Install **Maven** using [SDKMAN](../sdkman/index.md) with the following command:

```
sdk install maven
```

## Wrapper

The Maven Wrapper is an excellent tool to ensure that all developers use the same version of Maven. It is a set of files that you can commit to your project, and it will download the correct version of Maven when you run it.

To create the Maven Wrapper, run the following command:

```
mvn -N wrapper:wrapper
```

We can also specify the version of Maven to use:

```
mvn -N wrapper:wrapper -Dmaven=3.8.1
```

> **Note**: The option `-N` means non-recursive, and it tells Maven to execute the command only in the current project and not in the modules.

## Usage

### Build

To build a project, run the following command:

```shell
mvnw clean install
```

To skip the tests, run the following command:

```shell
mvnw clean install -DskipTests
```
### Test

To run test in a project, run the following command:

```shell
mvnw test
```

### Debug

To debug a Maven build, run the following command:

```shell
mvnw clean install -X
```

### Verify

To verify mvn package is valid and meets quality criteria of a project, run the following command:

```shell
mvnw clean verify
```

### Package

To package a project, run the following command:

```shell
mvnw clean package
```

### Deploy

To deploy a project, run the following command:

```shell
mvnw clean deploy
```

### Release

To release a project, run the following command:

```shell
mvnw release:prepare
mvnw release:perform
```

### Upgrade wrapper

To upgrade the Maven Wrapper, run the following command:

```shell
./mvnw -N wrapper:wrapper -Dmaven=3.8.7
```

## Update dependencies

To display the new versions of the dependencies in a project, run the following command:

```
mvnw versions:display-dependency-updates
```

To update the dependencies in a project, run the following command:

```shell
mvnw versions:use-latest-versions
mvnw versions:update-properties # Update the properties
```

To display the new versions of the plugins in a project, run the following command:

```
mvnw versions:display-plugin-updates
```

