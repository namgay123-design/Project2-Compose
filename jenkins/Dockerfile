# Start from official Jenkins LTS with Java 17
FROM jenkins/jenkins:lts-jdk17

# Switch to root so we can install extra packages
USER root

# Install Docker CLI + helpful tools
RUN apt-get update && apt-get install -y \
    docker.io \
    git \
    curl \
    jq \
 && rm -rf /var/lib/apt/lists/*

# Switch back to the Jenkins user (more secure)
USER jenkins
