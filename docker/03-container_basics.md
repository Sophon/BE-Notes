# CONTAINER BASICS

**Images** are read-only self-contained templates that has everything the app needs to run.

**Containers** are running instances of images.

Containers are very similar to a process. In fact, `ps` displays them.

## Anatomy

1. Base layer - a Linux distro, like Alpine (minimal) or Ubuntu (more complex)
2. Runtime environment - whatever the app needs, like Python or Node.js
3. Libraries, dependencies - external code the app relies on
4. Application code - our app code or binaries
5. Configuration - Docker config like environment