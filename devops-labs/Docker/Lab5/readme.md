# Docker Lab 5: Understanding ENTRYPOINT & CMD, and Custom Image Build

## Overview
This lab explores how `CMD` and `ENTRYPOINT` work within Dockerfiles, how to inspect image startup logic, and how to build and run a custom Ubuntu image using Docker.

## Objectives
- Inspect and compare `ENTRYPOINT` vs `CMD` usage in different Dockerfiles
- Identify the default runtime command for images based on Dockerfile definitions
- Build and run a custom Ubuntu image with an overridden startup process

## Lab Environment
- Platform: KodeKloud / Local Docker


## Quick Start


All step-by-step examples and screenshot evidence are provided in this repository.

## Tasks Overview
1. Inspect Dockerfiles for MySQL, WordPress, and Ubuntu
2. Check and explain the final container startup command (CMD/ENTRYPOINT analysis)
3. Build and run a custom Ubuntu image

## Screenshots
Screenshots for each CLI operation and result are included in the `screenshots/` directory.

## Resources
- [Docker ENTRYPOINT vs CMD – KodeKloud Blog][1]
- [Docker Docs: ENTRYPOINT & CMD][2]

[1]: https://kodekloud.com/blog/docker-entrypoint-cmd/
[2]: https://docs.docker.com/engine/reference/builder/#entrypoint
