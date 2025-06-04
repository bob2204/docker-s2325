FROM   debian:12
RUN    apt update \
    && apt install -y openssh-server \
    && mkdir -p /data \
    && date > /data/date.log
EXPOSE 22
CMD    ["/usr/sbin/sshd","-D"]
