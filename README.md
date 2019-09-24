# Jenkins docker
* Jenkins CI with docker client

# Pre-requisites

1. volume mount for jenkins directory requires permission(eg chmod 777 jenkins-mount).
2. Host port (eg:5000) to be available.
 

# CMD(Command to fire docker in docker): 
docker run -p 5000:8080 -p 50000:50000 \
           -v /home/ubuntu/jenkins-docker/jenkins-mount:/var/jenkins_home \
           -v /var/run/docker.sock:/var/run/docker.sock \
           --name Jenkins-docker -d jenkins-docker
