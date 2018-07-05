# Docker-Webserver
Hosting simple static website using Docker

```terminal
Sending build context to Docker daemon 347.6 kB
Step 1/4 : FROM nginx
latest: Pulling from library/nginx
683abbb4ea60: Pull complete 
6ff57cbc007a: Pull complete 
162f7aebbf40: Pull complete 
Digest: sha256:2cf71a9320ea65566c0738e87400407aaffd8dd11a411ceb2f2b585ad513469e
Status: Downloaded newer image for nginx:latest
 ---> 649dcb69b782
Step 2/4 : COPY wrapper.sh /
 ---> f21eedf82fda
Removing intermediate container 53710badc21b
Step 3/4 : COPY html /usr/share/nginx/html
 ---> ef3354b14dad
Removing intermediate container da9bccb84cd4
Step 4/4 : CMD ./wrapper.sh
 ---> Running in 25edd8f8a8e8
 ---> ee9f990fc0af
Removing intermediate container 25edd8f8a8e8
Successfully built ee9f990fc0af
```
