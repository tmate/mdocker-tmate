FROM tmate-java

ARG MAVEN_VERSION=3.3.9

RUN \
    wget -q -O- https://archive.apache.org/dist/maven/maven-3/$MAVEN_VERSION/binaries/apache-maven-$MAVEN_VERSION-bin.tar.gz | tar xzf - -C /usr/share && \
    ln -s /usr/share/apache-maven-$MAVEN_VERSION /usr/share/maven
