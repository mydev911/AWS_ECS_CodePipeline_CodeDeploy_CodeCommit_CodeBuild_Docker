#### ON root user
Create a folder inside /opt
```
ls
```
```
cd /opt/
```
Create folder
```
mkdir docker
```
```
cd docker
```
Create docker file
```
vim dockerfile
```
```
FROM centos:centos6
MAINTAINER VarunMnaik
RUN yum -y install httpd
COPY index.html /var/www/html/
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]
EXPOSE 80
```
#### Create index.html
```
vim index.html
```
```
<html>
<body><h1>CICD & Docker Tutorial By Varun Kumar Manik </h1>
<p style="background-color:DodgerBlue;">Version One (V2.0) in Blue Color.</p>
</body>
</html>
```
```
docker build -t webserver .
```


