## ON aws ec2 create docker image with centos and install http 
#### https://youtu.be/d7PTjQiahOQ

#### Create Ec2 and Attetch with elestic ip
```
sudo -i
```
Update
```
yum update -y
```
##### install docker
https://github.com/mydev911/Docker_example/blob/739e4eca3865494114d11ca857a4cf75bf2a0608/Install_docker/install_docker_1.md

#### Pull centos 
```
docker pull centos:centos6
```
```
docker images
```
Create container with the centos6 images
```
docker run -it -p 80:80 IMAGE_ID
```
##### install Httpd on the container we create
```
yum install httpd
```

### Getting Centos install problem
https://arstech.net/centos-6-error-yumrepo-error-all-mirror-urls-are-not-using-ftp-http/
### html file is created and go inside the html file
```
cd /var/www/html/
```
```
echo first website
```
```
service httpd start
```
#### Centos will run
