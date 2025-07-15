# Docker Lab 7: Volume Mounting and MySQL Data Persistence

## Overview

In this lab, we focus on working with Docker **volumes** by attaching persistent storage to MySQL containers. You'll learn how to locate Docker's volume data, attach it using `-v`, and test persistence by rerunning initialization scripts.

## Objectives

- Understand Docker volumes and bind mounts
- Inspect volume directories directly in the Docker host
- Run MySQL containers with persistent data
- Mount local/existing volumes manually
- Use `/opt/data` as named volume path

## Lab Environment

- Platform: KodeKloud / Docker


## Getting Started


Start with `commands.md` and see screenshots in `/screenshots`.

## Tasks Summary

1. Run MySQL with password env var
2. Explore Docker volumes in host
3. Reuse volume and initialize MySQL
4. Attach `/opt/data` for better persistence

## Screenshots

Each CLI task output is captured inside the `screenshots/` directory.

## Related Labs

- [Docker Lab 6 - Data Persistence & Layers](../docker-lab-6/)
- [Docker Lab 8 - Docker Compose & Named Volumes](../docker-lab-8/)

## Resources

- [Docker Docs: Volumes](https://docs.docker.com/storage/volumes/)
- [MySQL Image on Docker Hub](https://hub.docker.com/_/mysql)
