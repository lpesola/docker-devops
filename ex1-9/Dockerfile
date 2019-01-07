FROM debian:stable-slim 

WORKDIR /var/libcoap
RUN mkdir /var/compilation
RUN apt update && apt install -y git build-essential autoconf automake libtool pkgconf libssl-dev
RUN git clone https://github.com/obgm/libcoap.git
RUN cd libcoap && \
 ./autogen.sh && \
 ./configure --disable-documentation && \
 make && \
 make install
ENV LD_LIBRARY_PATH=/usr/local/include;/usr/local/lib/
ENTRYPOINT ["gcc -l coap-2-openssl"]


