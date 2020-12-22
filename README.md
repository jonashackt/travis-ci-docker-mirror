# travis-ci-docker-mirror
Example project showing how to configure a Docker registry mirror for TravisCI

[![Build Status](https://travis-ci.com/jonashackt/travis-ci-docker-mirror.svg?branch=main)](https://travis-ci.com/jonashackt/travis-ci-docker-mirror)
[![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/jonashackt/travis-ci-docker-mirror/blob/master/LICENSE)

We want to work around Docker Registry rate-limiting problems [like this](https://travis-ci.org/github/codecentric/spring-boot-admin/builds/751003082):

```shell
Caused by: org.testcontainers.containers.ContainerFetchException: Failed to get Docker client for hazelcast/hazelcast:4.0

Caused by: com.github.dockerjava.api.exception.DockerClientException: Could not pull image: toomanyrequests: You have reached your pull rate limit. You may increase the limit by authenticating and upgrading: https://www.docker.com/increase-rate-limit
```

See also https://travis-ci.community/t/docker-hub-you-have-reached-your-pull-rate-limit/10517, https://github.com/travis-ci/travis-ci/issues/6418