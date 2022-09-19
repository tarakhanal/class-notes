# Containers

- Containers helps us achieve "dev/prod parity" from 12factorapp
  - It works on any machine, not just your local machine
- The problem of running software at scale in production

## Terms

### Container Image

- A package with your compiled app and dependencies.

### Container

- A running instance (or paused) of a container image

### Dockerfile

- The build instructions for a container image

### Build

- The process of building a container image from a Dockerfile

### Volumes

- A filesystem made available to the container

### Tag

- A differentiator (version usually)

### MSB

- Multi-stage Build

### Repository

- A collection of related container images

### Registry

- A place to store container images

### Compose

- A utility to run multiple container images together

- [The Twelve Factors](https://12factor.net/)

## Diagram with all the terms

![](/img/containers.svg)

## Service Relationships

![](/img/service-relationships.svg)

Linux Namespaces -> Linux "Containers"

It was hard to setup these stuff and only few knew how to setup until **Docker** came along
