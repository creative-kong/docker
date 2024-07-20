# Docker 
  1. Pull an image
     ```bash
     docker pull {name}:{tag}
     ```
     pull image from registry
     
     ```bash
     kong ~ % docker pull nginx:1.27
     ```

     ```bash
     kong ~ % docker images
     ```
     manage image (show top level images)
     
  2. Run am image
     ```bash
     docker run {name}:{tag}
     ```

     run an image

     ```bash
     kong ~ % docker run nginx:1.27
     ```

     ```bash
     kong ~ % docker ps
     ```

     show running docker image if ```control + c ``` to exit container, container will die

     ```bash
     -d or --detach
     ```

     run container in the background and print out container id

     ```bash
     kong ~ % docker run -d nginx:1.27
     ```

     ```bash
     kong ~ % docker logs {container id}
     kong ~ % docker logs e3456we
     ```

     print log of container

  3. Port binding or Port mapping
     ```bash
     kong ~ % docker stop {container id or container name}
     ```

     ```bash
     kong ~ % docker stop e3456we
     ```

     stop container

     ```bash
     -p or --publish
     ```

     publish a container port to the host

     ```bash
     -p {host port}:{container port}
     kong ~ % docker run -d -p 80:80 nginx:1.27
     ```

  4. Start / Stop Container

     ```bash
     kong ~ % docker start {container}
     ```

     start container

     ```bash
     kong ~ % docker stop {container}
     ```

     stop container

     ```bash
     kong ~ % docker run -d -p 80:80 --name web nginx:1.27
     ```

     ```--name``` assign a name to the container
