# Jenkins Agent Dockerfile (Rocky Linux 9)
FROM rockylinux:9

RUN dnf install -y java-11-openjdk git curl --allowerasing && \
    useradd -m jenkins

WORKDIR /home/jenkins
USER jenkins

CMD ["sleep", "infinity"]

