# RUNNING CONTAINERS

### Basic commands

- `docker pull nginx`
- `docker run nginx`
  - `-d` (`docker run -d nginx`) - detached mode
  - `-p` (`docker run -p 8080:80 nginx`) - port
    - can verify with `curl http://localhost:8080` or visiting that on our browser
  - `--name ourName`
- `docker ps`
  - we can refer to specific images via the generated name
- `docker kill docker_name` - kills the container
- `docker stop docker_name` - gracefully shuts down the container

### Lifecycle

