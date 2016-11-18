# Docker for building android applications

* Base: Debian 
* Java: openjdk-jdk8
* Android SDK: r24.4.1
* Build tools: 24.0.3
* Android API: 24

## Build an image

```bash
docker build -t abilisense/android-build .
```

## Run an interactive shell

```bash
docker run -ti abilisense/android-build /bin/bash
```
To build project from you local foder - change into it(cd) and run an interactive shell like this:
```bash
docker run -ti --volume=${PWD}:/localDebugRepo --workdir="/localDebugRepo" \
    --memory=4g --memory-swap=4g --entrypoint=/bin/bash abilisense/android-build
```

##License and Copyright

License: [GPL-3.0](LICENSE)

Copyright 2016, [AbiliSense Ltd.](http://www.abilisense.com/)
