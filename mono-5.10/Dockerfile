FROM debian:stretch-slim

# Mono runtime
MAINTAINER Hanspeter Gysin <hpgy59@gmail.com>

ENV MONO_VERSION 5.10.0.140

RUN apt-get update && apt-get install -y gnupg \
  && apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF \
  && echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list \
  && apt-get update && apt-get install -y mono-runtime \
  && apt-get purge -y gnupg && apt-get autoremove -y && apt-get clean \
  && rm -rf /var/lib/apt/lists/* /tmp/*
