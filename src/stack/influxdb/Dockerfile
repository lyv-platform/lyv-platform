FROM debian:buster-slim

# Useful variables
ARG NAME="influxdb"
ARG VERSION="1.7.9"
ARG ARTIFACT="${NAME}-${VERSION}-static_linux_amd64"
ARG DIRECTORY="/opt/${NAME}"
ARG URL="https://dl.influxdata.com/${NAME}/releases/${ARTIFACT}.tar.gz"

# Install required packages
RUN set -eux; \
    apt-get update; \
    apt-get install -y --no-install-recommends wget ca-certificates; \
    rm -rf /var/lib/apt/lists/*;

# Download InfluxDB, untar, create dirs, and clean up
RUN set -eux; \
    wget -O output ${URL}; \
    mkdir ${DIRECTORY}; \
    tar -xzf output -C ${DIRECTORY} --strip-components 2; \
    rm output; \
    mkdir -p ${DIRECTORY}/conf;

# Copy the configuration file
COPY files/influxdb.conf ${DIRECTORY}/conf

# Expose InfluxDB's ports:
# - 8086: the port is available for client-server communication using the
#         InfluxDB API.
EXPOSE 8086

# Add the InfluxDB's bin directory to the PATH variable
ENV PATH="${PATH}:${DIRECTORY}"

WORKDIR ${DIRECTORY}

CMD ["influxd", "-config", "conf/influxdb.conf"]
