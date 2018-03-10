# docker-mono-xsp
Create docker images with mono-runtime and xsp

The base image is built from a minimal (slim) debian 9 (stretch) with 
mono-runtime.

The mono-xsp4 images adds XSP to the base image and is ready to run an ASP.NET 
application with the XSP web server.

Simply map the port 80 to the port you want to use and share your published 
application to the /app folder.

```
docker run -p 8080:80 -v <path to my web app>:/app hpgy/mono-xsp
```
