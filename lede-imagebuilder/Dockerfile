FROM openwrtorg/imagebuilder

VOLUME [ "/lede" ]

WORKDIR /lede

# install dependencies
RUN sudo apt-get update && \
    sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk \
    gettext git libncurses5-dev libz-dev patch python3 unzip zlib1g-dev \
    lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib \
    p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils \
    upx libelf-dev autoconf automake libtool autopoint device-tree-compiler \
    nano net-tools qemu-utils openssh-server

COPY ["startscripts.sh", "/tmp/"]

ENTRYPOINT [ "bash", "/tmp/startscripts.sh" ]