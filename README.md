# getting-started-java

A sample application in Java for wercker. This is forked from the application git clone https://github.com/wercker/getting-started-java.git

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

## Run
To run the application using cache dir, simply execute:

```
wercker dev --pipeline CacheDir
```

To run the application using cache dir, simply execute:

```
wercker dev --pipeline NoCacheDir
```

---
Sign up for wercker: http://www.wercker.com
Learn more at: http://devcenter.wercker.com
