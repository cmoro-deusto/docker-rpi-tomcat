docker-tomcat8
==============

[![dockeri.co](http://dockeri.co/image/dordoka/rpi-tomcat)](https://registry.hub.docker.com/u/dordoka/rpi-tomcat/)

HypriotOS Raspberry Pi 1 & 2, Oracle JDK 8 and Tomcat 8 based docker container.

# Description
You should run this container on the background and mount the volume with your web app inside.

Includes:

 - Oracle JDK 1.8
 - Tomcat 8.0.20
 
## Volumes
Exports a volume on `/opt/tomcat/webapps`.
You can mount the volume on run to a local directory containing your war file or exploded war directory.
If you need the management app, remember to have a copy on your hosts volume mount point.

## Ports
Two ports are exposed:

 - 8080: default Tomcat port.
  
 - 8009: default Tomcat debug port.

Remember to map the ports to the docker host on run.


# How to run the container
## Using docker
To get the container up and running, run:
 
```
sudo docker run -d -p 8080:8080 -p 8009:8009 -v /opt/tomcat/webapps:/opt/tomcat/webapps dordoka/rpi-tomcat
```
Remember to change `/opt/tomcat/webapps` to the directory where your app is stored.

Kudos to [Hypriot](http://blog.hypriot.com/)
