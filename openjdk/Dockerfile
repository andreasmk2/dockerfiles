#
# Open JDK 7 image
#

FROM andreas/base-ubuntu

MAINTAINER Andreas Bakurov andreasmk2@gmail.com 

# Install Open JDK 7
RUN apt-get update
RUN apt-get install -y openjdk-7-jre-headless

# Clean deb cache
RUN apt-get autoremove -y
RUN apt-get clean -y
RUN apt-get autoclean -y

