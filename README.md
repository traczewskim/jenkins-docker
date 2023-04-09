# Jenkins as Docker Container

```shell
docker run \
  -u root \
  --name jenkins \
  -d \
  -p 8080:8080 \
  -v jenkins-data:/var/jenkins_home \
  -v $(which docker):/usr/bin/docker \
  -v /var/run/docker.sock:/var/run/docker.sock \
  jenkins/jenkins:lts
```