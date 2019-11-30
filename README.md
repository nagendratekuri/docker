# Docker installation on AWS EC2 RHEL

```sh
sudo yum update -y

sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

sudo yum install docker-ce --nobest

sudo yum install docker-ce --nobest

sudo systemctl enable docker.service

sudo systemctl status docker.service

sudo systemctl start docker.service

# sudo systemctl stop docker.service
# sudo systemctl restart docker.service

sudo usermod -a -G docker ec2-user

sudo reboot

docker info

```

### Test your Docker installation
```sh
docker info

docker help | more

docker info

docker run hello-world


```