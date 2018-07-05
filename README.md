# Docker-Webserver
Hosting simple static website using Docker

```terminal
Sending build context to Docker daemon 347.6 kB
Step 1/4 : FROM nginx
latest: Pulling from library/nginx
683abbb4ea60: Already exists 
6ff57cbc007a: Already exists 
162f7aebbf40: Already exists 
Digest: sha256:2cf71a9320ea65566c0738e87400407aaffd8dd11a411ceb2f2b585ad513469e
Status: Downloaded newer image for nginx:latest
 ---> 649dcb69b782
Step 2/4 : COPY wrapper.sh /
 ---> 23543434b6d2
Removing intermediate container d4507de71a1c
Step 3/4 : COPY html /usr/share/nginx/html
 ---> 877697dce7b5
Removing intermediate container 1736ef1a815b
Step 4/4 : CMD ./wrapper.sh
 ---> Running in fc2c90a2caee
 ---> 6a56344cc132
Removing intermediate container fc2c90a2caee
Successfully built 6a56344cc132
```
