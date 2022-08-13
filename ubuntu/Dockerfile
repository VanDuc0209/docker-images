ARG  UBUNTU_VERSION=16.04
FROM ubuntu:${UBUNTU_VERSION}
ARG USER_NAME="duccv"
# USER ${USER_NAME}
USER root
RUN useradd -ms /bin/bash ${USER_NAME}
RUN apt-get update \
    && apt-get install -y sudo \
    && echo ${USER_NAME} ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/${USER_NAME} \
    && chmod 0440 /etc/sudoers.d/${USER_NAME}

USER ${USER_NAME}
WORKDIR /home/${USER_NAME}