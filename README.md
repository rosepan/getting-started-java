# getting-started-java

An application in Java for wercker showing the usage of a wercker environment variable WERCKER_CACHE_DIR. In this application, the WERCKER_CACHE_DIR env var is used by the gradlew commands.

This application uses the `openjdk:8` container obtained from the [Docker Hub](https://registry.hub.docker.com/_/openjdk/)

## Setup & Build
Clone this repo and cd into the directory:

```
git clone https://github.com/rosepan/getting-started-java.git
cd getting-started-java
```

then build using:

```
wercker build
```
This command downloads the gradle artifacts to the directory specified by the wercker env var WERCKER_CACHE_DIR.

## Run
To run the application using wercker cache dir, simply execute:

```
wercker dev --pipeline WerckerCacheDir
```
In this command, there is no need to download gradle artifacts because it's using the cached files downloaded by the 'gradlew build' command.

To run the application using default cache dir, simply execute:

```
wercker dev --pipeline DefaultCacheDir
```
In this command, downloading is required because the default cache dir, which is the .gradle from the user's home directory, is empty.

Check the command execution time from the output of the steps running 'gradlew bootRun' on both pipelines. 

---
Sign up for wercker: http://www.wercker.com
Learn more at: http://devcenter.wercker.com
