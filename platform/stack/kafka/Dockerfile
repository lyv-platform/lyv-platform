FROM openjdk:11-jre-slim

# Useful variables
ARG NAME="kafka"
ARG VERSION="2.3.0"
ARG FULL_VERSION="2.12-${VERSION}"
ARG ARTIFACT="${NAME}_${FULL_VERSION}"
ARG DIRECTORY="/opt/${NAME}"
ARG URL="https://www.apache.org/dist/${NAME}/${VERSION}/${ARTIFACT}.tgz"

# Install required packages
RUN set -eux; \
    apt-get update; \
    apt-get install -y --no-install-recommends wget; \
    rm -rf /var/lib/apt/lists/*;

# Download Apache Kafka, untar, and clean up
RUN set -eux; \
    wget -O output ${URL}; \
    tar -xzf output -C /opt; \
    rm output; \
    mv /opt/${ARTIFACT} ${DIRECTORY}; \
    mkdir -p ${DIRECTORY}/conf

# Copy the configuration file
COPY files/server.properties $DIRECTORY/conf/

# Expose Apache Kafka's ports:
# - 9092: the primary communication port used by producers and consumers; also
#         used for inter-broker communication.
EXPOSE 9092

# Add the Apache Kafka's bin directory to the PATH variable
ENV PATH="${PATH}:${DIRECTORY}/bin"

WORKDIR ${DIRECTORY}

CMD ["kafka-server-start.sh", "conf/server.properties"]
