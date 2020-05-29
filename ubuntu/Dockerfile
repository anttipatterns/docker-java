FROM ubuntu:20.10

USER root

RUN ln -sf /usr/share/zoneinfo/UTC /etc/localtime && \
    apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends openjdk-14-jdk apt-transport-https && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates curl software-properties-common gnupg-agent apt-utils && \
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -

# Official binary for 20.10 (groovy) not yet available, please update later
RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && \
    apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends docker-ce-cli
