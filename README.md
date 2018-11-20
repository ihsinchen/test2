##Use Vagrant install ubuntu
Use Vagrant init to create default vagrantfile and if you are the first time to create ubuntu1804 this box, the box will be download from Vagrant cloud.
Vagrant init generic/ubuntu1804
enable the ubuntu1804 box via below command.
Vagrant up
Then the system is enabled.
Use Vagrant ssh to access to the VM.
Could Create RSA Key
turn off the VM via below command
vagrant halt

##Docker installation steps
Installation
1. update existing packages   
$ sudo apt update   
2. Install packages which let apt use packages over HTTPS   
$ sudo apt install apt-transport-https ca-certificates curl software-properties-common   
3.add GPG keys   
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -   
4. add docker repository to APT sources   
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"   
5. update package database   
sudo apt update   
6.install from the Docker repo instead of the default Ubuntu    
$ apt-cache policy docker-ce   
7. install docker   
sudo apt install docker-ce   
8. the daemon started, and the process enabled to start on boot.   
$ sudo systemctl status docker   
