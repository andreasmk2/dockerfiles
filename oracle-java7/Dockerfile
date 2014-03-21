#
# Oracle java 7 image
#
FROM andreas/base-ubuntu
MAINTAINER Andreas Bakurov andreasmk2@gmail.com

# Prepare apt for custom ppa
RUN apt-get update
RUN apt-get install -y software-properties-common python-software-properties

# Install Oracle Java
RUN add-apt-repository -y ppa:webupd8team/java
RUN apt-get update

# mark oracle eula as accepted
RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
RUN apt-get install -y oracle-java7-installer

