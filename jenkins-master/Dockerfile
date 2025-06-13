# Use the official Jenkins LTS image as the base
FROM jenkins/jenkins:lts

# Switch to root to install extra tools
USER root

# Optional: Install additional packages
RUN apt-get update && \
    apt-get install -y curl git && \
    apt-get clean

# Switch back to the Jenkins user
USER jenkins

# Expose Jenkins default port
EXPOSE 8080

# Jenkins automatically runs with: java -jar /usr/share/jenkins/jenkins.war
# and generates /var/jenkins_home/secrets/initialAdminPassword

