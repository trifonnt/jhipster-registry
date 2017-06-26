## Build docker image
```shell
./mvnw -Pprod package docker:build
``

## Tag newly built docker image
```shell
docker tag jhipster-registry trifonnt/jhipster-registry-trifon:v3.0.2
```

## Login to docker hub
```shell
docker login
```

## Push docker image to docker hub
```shell
docker push trifonnt/jhipster-registry-trifon:v3.0.2
```

## Start Jhipster-Registry via Docker container
```shell
docker run -it -p 8761:8761 -d -e jhipster.security.authentication.jwt.secret=xxx trifonnt/jhipster-registry-trifon:v3.0.2
```