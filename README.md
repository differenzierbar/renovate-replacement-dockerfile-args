# renovate-replacement-dockerfile-args

First, read the [Renovate minimal reproduction instructions](https://github.com/renovatebot/renovate/blob/main/docs/development/minimal-reproductions.md).

Then replace the current `h1` with the Renovate Issue/Discussion number.

## Current behavior

Renovate fails to create the PR for the (replacement) dependency update in the [Dockerfile](Dockerfile) containing dependencies in ARGs.
```
ARG BASE_IMAGE_NAME=amd64/python
ARG BASE_IMAGE_TAG=3.11

FROM  ${BASE_IMAGE_NAME}:${BASE_IMAGE_TAG}
```

## Expected behavior

Renovate creates the PR (as it does when the Dockerfile does not contain ARGs with dependencies).

## Link to the Renovate issue or Discussion

Put your link to the Renovate issue or Discussion here.
