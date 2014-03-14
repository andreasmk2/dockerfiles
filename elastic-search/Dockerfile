#
# Elastic Search based on oracle-java7 image
#

# Use java 7 image
FROM andreas/java7

MAINTAINER Andreas Bakurov andreasmk2@gmail.com

# Fetch ES archive into temp directory
RUN (cd /tmp && wget https://download.elasticsearch.org/elasticsearch/elasticsearch/elasticsearch-1.0.1.tar.gz)

# Extract
RUN mkdir /applications
RUN (cd /applications && tar -xf /tmp/elasticsearch-1.0.1.tar.gz && ln -s ./elasticsearch-1.0.1 ./elasticsearch)
RUN rm /tmp/elasticsearch-1.0.1.tar.gz

# Start ES during boot
ENTRYPOINT /applications/elasticsearch/bin/elasticsearch

# Expose ES port
EXPOSE 9200
EXPOSE 9300
