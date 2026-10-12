# DOCKER COMPONENTS

### Core components

1. Docker client
  - docker CLI
  - API calls - calls to the docker host
2. Docker host
  - REST API - receiving from the client
  - daemon - Docker engine; manages the containers
  - containers - both running and the stopped ones
  - image cache 
3. image registry
  - available for download to create containers

Images can be thought of as recipes while containers can be thought of as an instance of an image that's running.

### Running a container

1. CLI: `docker run`
2. CLI → Docker host via API call
3. daemon: downloads it from the registry or gets it from the cache
4. containers - image gets instantiated

### Building & pushing an image

1. CLI: `docker build`
2. CLI → Docker host via API call 
   - with `dockerfile` and context
3. daemon: builds image out of the `dockerfile`
   - might download images mentioned in the `dockerfile` from the registry
4. daemon: tag the image, cache it locally
   - doesn't push to the registry by default
5. cli:`docker push`