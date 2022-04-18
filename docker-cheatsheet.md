**To build a docker image:**

  docker build . -t <tagName\>:<version\> [multipleTags]
  
  multipleTags can also be added during build, example if you want to tag a build with latest and specific version like v2.

**To use specific Dockerfile during build:**
  
  docker build -f <pathtoDockerfile\> -t <tagName\>:<version\>
 
**To run a built image:**
  
  docker run --name <name\> -p <localPort\>:<containerPort\> <tagName\>:<version\>
  
  Example: docker run --name testapp -p 8080:8080 testapp:v1
  
**To push a docker image to container registry:**
  
  
  
  
**Links:**
 - https://docs.docker.com/engine/reference/commandline/cli/
  

