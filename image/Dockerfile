FROM ubuntu:22.04

LABEL maintainer="alzhahir"

ENV DEBIAN_FRONTEND noninteractive

## add container user
RUN useradd -m -d /home/container container
ENV USER=container HOME=/home/container

RUN apt update && apt upgrade -y

RUN apt install software-properties-common -y

RUN add-apt-repository ppa:dotnet/backports

RUN apt update

RUN apt install -y gcc g++ libgcc1 libgcc-s1 lib32gcc1-amd64-cross libc++-dev gdb libc6 libstdc++6 ca-certificates git wget curl tar zip unzip binutils xz-utils liblzo2-2 cabextract iproute2 net-tools netcat telnet libatomic1 libsdl1.2debian libsdl2-2.0-0 \
        libfontconfig libgssapi-krb5-2 libicu70 liblttng-ust1 icu-devtools libunwind8 libssl3 sqlite3 libsqlite3-dev libzip4 locales ffmpeg apt-transport-https init-system-helpers \
        libcurl3-gnutls liblua5.1-0 libluajit-5.1-2 libsqlite3-0 bzip2 zlib1g libevent-dev mono-complete dotnet-sdk-8.0

## configure locale
RUN update-locale lang=en_US.UTF-8 \
 && dpkg-reconfigure --frontend noninteractive locales
 
## Test stuff
# RUN ln -sf /.local/share/Terraria /home/container

WORKDIR /home/container
COPY ./entrypoint.sh /entrypoint.sh
CMD ["/bin/bash", "/entrypoint.sh"]
