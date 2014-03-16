#
# andreas/base-ubuntu
# Base image made from ubuntu:precise
# Workaround for failing apt-get upgrade is included
# https://github.com/dotcloud/docker/issues/1724 
#

FROM ubuntu:precise

# Workaround for apt-get upgrade
RUN dpkg-divert --local --rename /usr/bin/ischroot && ln -sf /bin/true /usr/bin/ischroot

# Upgrade applications
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get autoremove -y
RUN apt-get clean -y
RUN apt-get autoclean -y
