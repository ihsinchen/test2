##Use Vagrant install ubuntu  
1.Use Vagrant init to create default vagrantfile and if you are the first time to create ubuntu1804 this box, the box will be download from Vagrant cloud.  
Vagrant init generic/ubuntu1804  
2.enable the ubuntu1804 box via below command.  
Vagrant up  
3.Then the system is enabled.  
4.Use Vagrant ssh to access to the VM.  
5.Could Create RSA Key  
6.turn off the VM via below command  
vagrant halt  

##Docker installation steps
Installation
1. update existing packages   
$ sudo apt update   
2. Install packages which let apt use packages over HTTPS   
$ sudo apt install apt-transport-https ca-certificates curl software-properties-common  
3. add GPG keys   
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -   
4. add docker repository to APT sources   
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"  
5. update package database  
$ sudo apt update  
6. install from the Docker repo instead of the default Ubuntu  
$ apt-cache policy docker-ce  
7. install docker  
$ sudo apt install docker-ce  
8. Check it's runnung or not   
$ sudo systemctl status docker    
9. if you don't want to use sudo.  
$ sudo usermod -aG docker ${USER}  
10. su - ${USER}  
11. confirm user is added or not  
$ id -nG  

##Install Portainer  
1. update the package first  
$ sudo apt update  
2. pull Portainer to the local    
$ docker pull portainer/portainer  
3. install portainer   
$ docker volume create portainer_data  
$ docker run -d -p 9000:9000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer  

Note: becaue use virtual box to run Docker, the port setting is needed.  
check local IP and client IP.  
