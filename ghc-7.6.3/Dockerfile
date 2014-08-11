FROM phusion/baseimage:0.9.12

MAINTAINER Christopher Biscardi <chris@christopherbiscardi.com>

ENV HOME /root

RUN /etc/my_init.d/00_regen_ssh_host_keys.sh

CMD ["/sbin/my_init"]

RUN apt-get update
RUN apt-get install software-properties-common
RUN add-apt-repository -y ppa:hvr/ghc
RUN apt-add-repository "deb http://ppa.launchpad.net/hvr/ghc/ubuntu precise main"
RUN apt-get update
RUN apt-get install cabal-install-1.20 ghc-7.6.3 happy-1.19.4 alex-3.1.3 -y

ENV PATH /root/.cabal/bin:/opt/cabal/1.20/bin:/opt/ghc/7.6.3/bin:/opt/happy/1.19.4/bin:/opt/alex/3.1.3/bin:$PATH

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*