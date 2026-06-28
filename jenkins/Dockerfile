FROM jenkins/jenkins:lts

USER root

# Install Docker CLI and Git
RUN apt-get update && \
    apt-get install -y \
    docker.io \
    docker-compose \
    git && \
    apt-get clean

USER jenkins