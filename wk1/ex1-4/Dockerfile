FROM ubuntu:16.04 

WORKDIR /curler
RUN apt update && apt install -y curl
COPY curler.sh .
RUN chmod u+x curler.sh
ENTRYPOINT ["./curler.sh"]


