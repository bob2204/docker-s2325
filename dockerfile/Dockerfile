FROM debian:12
RUN  apt update
COPY start.sh /
RUN  mkdir /data
COPY data.txt /data
WORKDIR /data
ENV  STAGE=Docker
ARG  LOGIN
ENV  USER=${LOGIN}
RUN  echo ${LOGIN} > user.txt
ENTRYPOINT ["/start.sh"]
