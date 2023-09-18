# keycloak-issue-reproducer

This project uses Quarkus, the Supersonic Subatomic Java Framework and is a reproducer project for an issue where connecting
to an OIDC auth server which is not available causes a blocked Vertx event-loop thread.

## Reproducing the bug

Build the project as a docker image:
```shell script
docker build -f src/main/docker/Dockerfile.jvm -t quarkus/keycloak-issue-reproducer-jvm .
```

Start the docker container using:
```shell script
docker run -i --rm -p 8080:8080 quarkus/keycloak-issue-reproducer-jvm
```