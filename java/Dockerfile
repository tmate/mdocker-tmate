FROM tmate-base

ARG JAVA_VERSION=6

RUN \
  (echo "deb http://ppa.launchpad.net/webupd8team/java/ubuntu trusty main" | tee /etc/apt/sources.list.d/webupd8team-java.list) && \
  (echo "deb-src http://ppa.launchpad.net/webupd8team/java/ubuntu trusty main" | tee -a /etc/apt/sources.list.d/webupd8team-java.list) && \
  apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys EEA14886 && \
  apt-get update

RUN \
  echo oracle-java$JAVA_VERSION-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
  apt-get install -y oracle-java$JAVA_VERSION-installer

RUN \
  rm -rf /var/lib/apt/lists/* && \
  rm -rf /var/cache/oracle-jdk$JAVA_VERSION-installer
