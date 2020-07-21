# docker-on-centos8

Install docker and docker-compose on centOS 8

## Docker CE

 - `sudo yum install -y yum-utils device-mapper-persistent-data lvm2`
 - `sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo`
 - `sudo yum-config-manager --enable docker-ce-edge`
 - containerd.io first : `sudo yum install -y https://download.docker.com/linux/centos/7/x86_64/stable/Packages/containerd.io-1.2.6-3.3.el7.x86_64.rpm`
 - `sudo yum install -y docker-ce docker-ce-cli`
 - `sudo systemctl enable docker`
 - `sudo systemctl start docker`
 - `sudo systemctl disable firewalld`
 - `sudo usermod -aG docker $USER`
 - `newgrp docker`
 - Test : `sudo docker run hello-world`
 
## Docker Compose

 - `curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o docker-compose`
 - `sudo mv docker-compose /usr/local/bin && sudo chmod +x /usr/local/bin/docker-compose`
 
 
## Links

 - [how-to-install-docker-in-rhel-8](https://linuxconfig.org/how-to-install-docker-in-rhel-8)
 - https://docs.docker.com/engine/install/centos/
 - [Docker fails on CentOS 8 with Error package containerd.io](https://medium.com/@anuketjain007/installation-of-docker-fails-on-centos-8-with-error-package-containerd-io-f7a338b34a71)
 - [Error Docker-ce on CentOS 8](https://forums.docker.com/t/docker-ce-on-centos-8/81648)
 - [Postinstall](https://docs.docker.com/engine/install/linux-postinstall/)
 
 
