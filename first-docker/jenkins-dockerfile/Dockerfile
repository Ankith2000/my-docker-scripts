FROM jenkins/jenkins:lts
USER ROOT
RUN apt-get update && apt-get install -y jenkins.io
USER JENKINS
EXPOSE 8080
