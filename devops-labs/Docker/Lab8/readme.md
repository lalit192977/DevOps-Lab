# Docker Lab 8: Custom Docker Networks & Inter-Container Communication

## 📘 Overview
This lab explores Docker container **networking** with a focus on:
- Inspecting default bridge networks
- Creating isolated containers
- Creating custom networks with subnets/gateway
- Linking containers over customized Docker networks for communication

## 🎯 Learning Objectives
- Work with default and custom networks
- Detach network connectivity using `--network none`
- Use custom subnet/gateway with bridge driver
- Deploy multi-container apps using `--network` and `--link`

## 🖥 Lab Environment
- Platform: KodeKloud Docker Lab


## 🚀 How to Use This Repo


Explore each step via `lab-tasks.md` and refer to `screenshots/` for visual output.

## 🧪 Key Concepts Covered
- Docker bridge vs none network
- Container discovery via `--link`
- Assigning subnets and gateways to networks
- Multi-container web app + MySQL deployment

## 🔗 Related Labs
- [Docker Lab 7 – Data Volumes](../docker-lab-7/)
- [Docker Lab 9 – Docker Compose (Coming Soon)](../docker-lab-9/)

## 📚 Resources
- [Docker Networking Overview](https://docs.docker.com/network/)
- [Docker Custom Networks](https://docs.docker.com/network/network-tutorial-standalone/)
