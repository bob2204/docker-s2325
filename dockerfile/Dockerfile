FROM debian:12
WORKDIR /data
ARG  LOGIN
RUN  apt update && echo "${LOGIN}" > /data/user.txt
COPY . /data/
ENV  STAGE=Docker
ENV  USER=${LOGIN}
ENTRYPOINT ["/data/start.sh"]
