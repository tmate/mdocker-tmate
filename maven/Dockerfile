FROM tmate-java

ARG MAVEN_VERSION=3.3.9
ARG MAVEN_OPTS=-Xmx1024m

RUN \
    wget -q -O- https://archive.apache.org/dist/maven/maven-3/$MAVEN_VERSION/binaries/apache-maven-$MAVEN_VERSION-bin.tar.gz | tar xzf - -C /usr/share && \
    ln -s /usr/share/apache-maven-$MAVEN_VERSION /usr/share/maven

RUN \
    apt-get update && apt-get install -y libtcnative-1

ENV PATH /usr/share/maven/bin:$PATH
ENV M2_HOME /usr/share/maven
ENV MAVEN_OPTS $MAVEN_OPTS
