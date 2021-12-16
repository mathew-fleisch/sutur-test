# sutur-test

[![Build Containers](https://github.com/mathew-fleisch/sutur-test/actions/workflows/build-containers.yaml/badge.svg)](https://github.com/mathew-fleisch/sutur-test/actions/workflows/build-containers.yaml)

This container is a simple alpine container that includes a text file at `/BUILD_DATE.txt` that contains output from the date command when the container was built. This should give each container a unique sha and a unique container built daily.

A [Github Action](.github/workflows/build-containers) will build + push this [Dockerfile](Dockerfile) to [docker hub](https://hub.docker.com/r/mathewfleisch/sutur-test/tags)