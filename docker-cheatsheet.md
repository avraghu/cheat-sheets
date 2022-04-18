**docker build:**

  docker build . -t <tagName\>:<version\> [multipleTags]
  
  multipleTags can also be added during build, example if you want to tag a build with latest and specific version like v2.

**To use specific Dockerfile during build:**
  
  docker build -f <pathtoDockerfile\> -t <tagName\>:<version\>
  
-------------------------------------------------------------------
 
**docker run:**
  
  docker run --name <name\> -p <localPort\>:<containerPort\> <tagName\>:<version\>
  
  Example: docker run --name testapp -p 8080:8080 testapp:v1
  
 To pass environment variables during docker run:
  docker run -e <key\>:<value\> --name <name\> -p <localPort\>:<containerPort\> <tagName\>:<version\>
  
  Example: docker run -e SPRING_APPLICATION_JSON="{\"app.name\":\"testapp\"}" -e DB_CONNECTION_STRING="db_conn_string"  --name testapp -p 8080:8080 testapp:v1
  
-------------------------------------------------------------------  
  
**docker push:**
  
  docker login <registry\> --username <username\>

  docker tag <tagName\>:<version\> <acr\>.azurecr.io/<tagName\>:<version\>

  docker push <acr\>.azurecr.io/<tagName\>:<version\>

-------------------------------------------------------------------
**docker pull:**

  docker login <registry\> --username <username\>

  docker pull <acr\>.azurecr.io/<tagName\>:<version\>
  
-------------------------------------------------------------------  
**Links:**
 - https://docs.docker.com/engine/reference/commandline/cli/
  

