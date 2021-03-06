VSTS Agent Docker Image
====================

This repository contains `Dockerfile` definitions for [julioarruda/vsts-maven](https://github.com/julioarruda/docker-vsts-agent) Docker images.

[![Downloads from Docker Hub](https://img.shields.io/docker/pulls/julioarruda/vsts-maven.svg)](https://registry.hub.docker.com/u/julioarruda/vsts-maven)
[![Stars on Docker Hub](https://img.shields.io/docker/stars/julioarruda/vsts-maven.svg)](https://registry.hub.docker.com/u/julioarruda/vsts-maven)

## Supported tags

- [`latest` (*agent/Dockerfile*)]

## Configuration

For `latest`, you need to set these environment variables:
* `AGENT_PAT` - The personal access token from VSTS. Required.
* `VS_TENANT` - The VSTS tenant, a.k.a. the value that goes before .visualstudio.com, i.e., on foo.visualstudio.com, should be `foo`. Required.
* `AGENT_POOL` - The agent pool. Optional. Default value: `Default`

For `docker`, you need to set these additional variables:
* `DOCKER_USERNAME` - Your docker user name. Required.
* `DOCKER_PASSWORD` - Your docker password. Required.

## Running

On Windows, use Docker for Windows and run, on PowerShell:

````powershell
docker run --name vsts-agent -ti -e VS_TENANT=$env:VS_TENANT -e AGENT_PAT=$env:AGENT_PAT -d julioarruda/vsts-maven````

On a Mac, use Docker for Mac, or directy on Linux, run in bash:

````bash
docker run --name vsts-agent -ti -e VS_TENANT=$VS_TENANT -e AGENT_PAT=$AGENT_PAT -d julioarruda/vsts-maven````

## Maintainers

* [Julio Arruda](http://www.julioarruda.com.br/), \\

## License

This software is open source, licensed under the Apache License, Version 2.0.
See [LICENSE.txt](https://github.com/julioarruda/vsts-agent/blob/master/LICENSE.txt) for details.
Check out the terms of the license before you contribute, fork, copy or do anything
with the code. If you decide to contribute you agree to grant copyright of all your contribution to this project, and agree to
mention clearly if do not agree to these terms. Your work will be licensed with the project at Apache V2, along the rest of the code.

* based from projet giggio/vsts-agent
