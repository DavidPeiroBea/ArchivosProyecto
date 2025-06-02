FROM jenkins/jenkins:2.511-jdk17

USER root

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        ssh \
        ansible \
        git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

USER jenkins