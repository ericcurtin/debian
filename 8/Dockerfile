FROM debian:8

RUN apt -y update &&\
    apt -y upgrade &&\
    apt -y install gcc\
                   g++\
                   cmake\
                   vim\
                   dmidecode\
                   libcurl3\
                   perl\
                   liburi-perl\
                   apt-transport-https\
                   bind9-host\
                   dnsutils\
                   lsb-release\
                   libconfig-std-perl\
                   automake\
                   libtool-bin\
                   pkg-config\
                   make\
                   libssl-dev\
                   libcurl4-openssl-dev\
                   dpkg-dev\
                   wget\
                   gettext\
                   sudo\
                   net-tools\
                   clang\
                   silversearcher-ag\
                   ccache &&\
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN cd /tmp &&\
    wget http://www.kernel.org/pub/software/scm/git/git-2.7.4.tar.gz &&\
    tar xf git-2.7.4.tar.gz &&\
    cd /tmp/git-2.7.4 &&\
    make -j3 configure &&\
    ./configure --prefix=/usr &&\
    make -j3 &&\
    make -j3 install &&\
    rm -rf /tmp/git-2.7.4*

