## Install

+ Build
  * docker build --build-arg USERNAME=admin --build-arg PASSWORD=Password1 -t tim545/cadvisor-basicauth .

+ Run
  * docker run \
   --volume=/:/rootfs:ro \
   --volume=/var/run:/var/run:rw \
   --volume=/sys:/sys:ro \
   --volume=/var/lib/docker/:/var/lib/docker:ro \
   --publish=8080:8080 \
   --detach=true \
   --name=cadvisor-basicauth \
   --restart=always \
  tim545/cadvisor-basicauth:latest
