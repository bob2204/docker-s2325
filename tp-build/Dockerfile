FROM   debian:12
ARG    LOGIN=bob
RUN    apt update \
    && apt install -y openssh-server \
    && mkdir -p /data \
    && date > /data/date.log \
    && useradd -m -s /bin/bash ${LOGIN} \
    && mkdir -p /home/${LOGIN}/.ssh \
    && mkdir -p /run/sshd
COPY   id_ed25519.pub /home/${LOGIN}/.ssh/authorized_keys
EXPOSE 22
CMD    ["/usr/sbin/sshd","-D"]
