# DOCKER IMAGES

An image is a read-only, self-contained template that has everything needed to run the app.

A container is a running instance of an image.

## Anatomy

1. Base layer - a Linux distro, like Alpine (minimal) or Ubuntu (more complex)
2. Runtime environment - whatever the app needs, like Python or Node.js
3. Libraries, dependencies - external code the app relies on
4. Application code - our app code or binaries
5. Configuration - Docker config like environment

## Registries

### Why
- sharing
- versioning
- automation - like via CICD

### Types

- public
  - Docker Hub
  - public for everybody
  - general use images
- private
  - proprietary software
  - custom images
- fully custom
  - we create them
