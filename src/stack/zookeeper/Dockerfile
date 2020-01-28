FROM openjdk:11-jre-slim

# Useful variables
ARG NAME="zookeeper"
ARG VERSION="3.5.5"
ARG ARTIFACT="apache-${NAME}-${VERSION}-bin"
ARG DIRECTORY="/opt/${NAME}"
ARG URL="https://www.apache.org/dist/${NAME}/${NAME}-${VERSION}/${ARTIFACT}.tar.gz"

# Install required packages
RUN set -eux; \
    apt-get update; \
    apt-get install -y --no-install-recommends wget; \
    rm -rf /var/lib/apt/lists/*;

# Download Apache Zookeeper, untar, and clean up
RUN set -eux; \
    wget -O output ${URL}; \
    tar -xzf output -C /opt; \
    rm output; \
    mv /opt/${ARTIFACT} ${DIRECTORY}; \
    mkdir -p ${DIRECTORY}/data ${DIRECTORY}/dataLog;

# Copy the configuration file
COPY files/zoo.cfg ${DIRECTORY}/conf/

# Expose Apache Zookeeper's ports:
# - 2181: used by Zookeeper clients to connect to the Zookeeper servers
# - 2888: used by peer Zookeeper servers to communicate with each other
# - 3888: used for leader election
# - 8080: used for accessing the AdminServer
EXPOSE 2181 2888 3888 8080

# Add the Apache Zookeeper's bin directory to the PATH variable
ENV PATH="${PATH}:${DIRECTORY}/bin"

CMD ["zkServer.sh", "start-foreground"]
