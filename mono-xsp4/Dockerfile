FROM hpgy/mono-runtime:5.10

MAINTAINER Hanspeter Gysin <hpgy59@gmail.com>

RUN  apt-get update && apt-get install -y mono-xsp \
  && apt-get autoremove -y && apt-get clean \
  && rm -rf /var/lib/apt/lists/* /tmp/*

  
VOLUME /app
WORKDIR /app

EXPOSE 80

ENTRYPOINT [ "xsp4","--port","80","--nonstop"]
