# sutur-test

[![Build Containers](https://github.com/mathew-fleisch/sutur-test/actions/workflows/build-containers.yaml/badge.svg)](https://github.com/mathew-fleisch/sutur-test/actions/workflows/build-containers.yaml)

This container is a simple alpine container that includes a text file at `/BUILD_DATE.txt` that contains output from the date command when the container was built. This should give each container a unique sha and a unique container built daily.

A [Github Action](.github/workflows/build-containers) will build + push this [Dockerfile](Dockerfile) to [docker hub](https://hub.docker.com/r/mathewfleisch/sutur-test/tags) on merges to the main branch AND daily at midnight.


```
docker run mathewfleisch/sutur-test:2021.12.16-1639684875 cat /BUILD_DATE.txt
Unable to find image 'mathewfleisch/sutur-test:2021.12.16-1639684875' locally
2021.12.16-1639684875: Pulling from mathewfleisch/sutur-test
59bf1c3509f3: Pull complete
676a054cbc1b: Pull complete
Digest: sha256:6328641a8c1a9429e31798f984f052cadc4d271438992c831cbfcf45a4b2eb40
Status: Downloaded newer image for mathewfleisch/sutur-test:2021.12.16-1639684875
Thu Dec 16 20:01:25 UTC 2021
```