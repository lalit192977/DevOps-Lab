# Docker Lab 9: Deploying a Private Docker Registry

## 🔍 Overview

This lab focuses on creating a **local Docker registry**, pushing custom images to it, and verifying them using host port mapping (5000 or 5050). You'll also learn how to manage port conflicts and remove unused images/containers.

## 🎯 Objectives

- Deploy a local private Docker registry
- Tag images for localhost registry usage
- Push and pull images from custom registries
- Manage container port conflicts
- Clean up containers, images, and verify storage savings

## 🧪 Lab Tools

- Docker Engine
- Registry image (`registry:2`)
- `nginx:latest`, `httpd:latest`
- CLI tools: `netstat`, `ss`, `lsof`

## 📦 Lab Environment

- Platform: KodeKloud / Local Docker Host


## ▶️ Quick Start


Follow `commands.md` or detailed walkthrough in `lab-tasks.md`.

## 📷 Screenshots Available

All task screenshots live in `screenshots/`.

## 🔗 Related Labs

- [Lab 8 - Networking](../docker-lab-8/)
- [Lab 10 - Registry with Authentication ⏳](../docker-lab-10/)

## 📚 References

- [Docker Registry (Official Docs)](https://docs.docker.com/registry/)
- [Docker Hub Registry Image](https://hub.docker.com/_/registry)
