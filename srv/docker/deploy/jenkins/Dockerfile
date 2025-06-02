FROM jenkins/jenkins:2.511-jdk17

USER root

RUN apt-get update && apt-get install -y ssh ansible git \
  && mkdir -p /var/jenkins_home/.ssh \
  && ssh-keyscan -t rsa,ecdsa,ed25519 github.com > /var/jenkins_home/.ssh/known_hosts \
  && chown -R jenkins:jenkins /var/jenkins_home/.ssh \
  && chmod 700 /var/jenkins_home/.ssh \
  && chmod 600 /var/jenkins_home/.ssh/known_hosts

USER jenkins