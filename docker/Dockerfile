FROM ubuntu:trusty

#ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64

RUN apt-get update

RUN apt-get install -y curl unzip bzip2 zip git #openjdk-8-jdk build-essential
RUN curl -s get.sdkman.io | bash
RUN /bin/bash -c "source /root/.sdkman/bin/sdkman-init.sh && \
    sdk install java 8u151-oracle"
RUN /bin/bash -c "source /root/.sdkman/bin/sdkman-init.sh && \
    git clone https://github.com/DICE-UNC/jargon-training.git && \
    git clone https://github.com/DICE-UNC/jargon.git && \
    cd jargon && \
    sdk install maven 3.5.2 && \
    mvn install -Dmaven.test.skip=true && \
    cd .. && \
    sdk install groovy && \
    sh"
