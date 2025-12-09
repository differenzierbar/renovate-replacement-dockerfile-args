# renovate-replacement-dockerfile-args

First, read the [Renovate minimal reproduction instructions](https://github.com/renovatebot/renovate/blob/main/docs/development/minimal-reproductions.md).

Then replace the current `h1` with the Renovate Issue/Discussion number.

## Current behavior

Renovate fails to create a PR for (replacement) dependency updates in Dockerfiles when the [Dockerfile](Dockerfile) contains ARGs with dependencies:
```
ARG BASE_IMAGE_NAME=amd64/python
ARG BASE_IMAGE_TAG=3.11

FROM  ${BASE_IMAGE_NAME}:${BASE_IMAGE_TAG}
```

Renovate does **not** fail to create a PR for (replacement) dependency updates in Dockerfiles when the Dockerfile does **not** contain ARGs with dependencies:
```
FROM  amd64/python:3.11
```

## Expected behavior

Renovate creates the PR (as it does when the Dockerfile does not contain ARGs with dependencies).

## Link to the Renovate issue or Discussion

Put your link to the Renovate issue or Discussion here.
