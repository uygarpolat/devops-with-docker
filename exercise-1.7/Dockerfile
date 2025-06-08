FROM ubuntu:24.04

WORKDIR /usr/src/app/

RUN apt-get update && apt-get -y install curl

COPY script.sh .

RUN chmod +x script.sh

ENTRYPOINT ["./script.sh"]