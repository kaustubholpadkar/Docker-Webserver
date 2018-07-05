# Docker-Webserver
Hosting simple static website using Docker

## Step 1 : Create 'wrapper.sh'
```shell
#!/bin/bash

echo "Nginx is running..."

exec nginx -g "daemon off;"
```

## Step 2 : Create 'Dockerfile'
```terminal
FROM nginx

COPY wrapper.sh /

COPY html /usr/share/nginx/html

CMD ["./wrapper.sh"]
```

## Step 3 : Build Image Locally
```terminal
sudo docker build -t linear_regression_webserver .
```

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

## Step 4 : Run the container for the webserver
```terminal
sudo docker run -d -P --name static-linearregression linear_regression_webserver
```
```terminal
0fd044590e60a125ac8f01bf71fe03249edd25a46680470dbb06591c5f47134f
```


## Step 5 : Find the port on which webserver is running
```terminal
sudo docker port static-linearregression
```
```terminal
80/tcp -> 0.0.0.0:32771
```
