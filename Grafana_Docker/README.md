![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Docker_%28container_engine%29_logo.svg/320px-Docker_%28container_engine%29_logo.svg.png)

![](https://grafana.com/static/assets/internal/grafana_logo-web-white-text.svg)
------------------------------
### Install Docker Engine on Ubuntu

**OS requirements🔗**

+ **To install Docker Engine, you need the 64-bit version of one of these Ubuntu versions:**

    * Ubuntu Lunar 23.04
    * Ubuntu Kinetic 22.10
    * Ubuntu Jammy 22.04 (LTS)
    * Ubuntu Focal 20.04 (LTS)
    * Ubuntu Bionic 18.04 (LTS)
 
>Docker Engine is compatible with x86_64 (or amd64), armhf, arm64, and s390x architectures.

#### Uninstall old versions

Older versions of Docker went by the names of `docker`, `docker.io`, or `docker-engine`, you might also have installations of `containerd` or `runc.` Uninstall any such older versions before attempting to install a new version:

    sudo apt-get remove docker docker-engine docker.io containerd runc

> `apt-get` might report that you have none of these packages installed.

Images, containers, volumes, and networks stored in `/var/lib/docker/` aren’t automatically removed when you uninstall Docker. If you want to start with a clean installation, and prefer to clean up any existing data, read the uninstall Docker Engine section.

### Install using the apt repository

Before you install Docker Engine for the first time on a new host machine, you need to set up the Docker repository. Afterward, you can install and update Docker from the repository.

**Set up the repository**

- [ ] **1 Update the `apt` package index and install packages to allow apt to use a repository over HTTPS:**

        sudo apt-get update
        sudo apt-get install ca-certificates curl gnupg
        
- [ ] **2 Add Docker’s official GPG key:**

        sudo install -m 0755 -d /etc/apt/keyrings
        curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
        sudo chmod a+r /etc/apt/keyrings/docker.gpg

- [ ] **3 Use the following command to set up the repository:**

        echo \
        "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
        "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
        sudo tee /etc/apt/sources.list.d/docker.list > /dev/null










#### Instruções para subir o Docker-Compose - Sistemas Debian ####

####--Primeiramente precisamos instalar algumas dependências--####

    apt install apt-transport-https ca-certificates curl gnupg2 software-properties-common bash-completion
    
####--Para instalar as dependências utilizamos o seguinte comando--####

     apt-get update                                                                                                
     apt-get install apt-transport-https ca-certificates curl gnupg2 software-properties-common bash-completion -y 
     
####--Agora é preciso adicionar a public key especifica para o Docker--####

     curl -fsSL https://download.docker.com/linux/$(. /etc/os-release; echo "$ID")/gpg | apt-key add -    
    
####--O próximo passo agora é adicionar o repositório Docker--####

     add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/$(. /etc/os-release; echo "$ID") $(lsb_release -cs) stable" 
    
####--Feito isso, agora podemos finalmente instalar o Docker-ce com o seguinte comando--####

     apt install docker-ce 
    

####--Neste momento o Docker já se encontra devidadente instalado, com isso podemos verificar a versão do Docker instalado--####

     docker version 

####--Para setar o restart automático do Docker.service executamos o seguinte comando--####

     systemctl enable docker 
   
####--Instalando o Docker-Compose--###

     curl -L https://github.com/docker/compose/releases/download/1.16.1/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose 
     chmod +x /usr/local/bin/docker-compose                                                                                                  

####--Para checar a versão do Docker-Compose usamos o seguinte comando--####

     docker-compose version 


############################# Lista de comandos Docker ##############################

-> Listar todos os containers em execusão 
    docker ps
    
-> Listar todos os containers que estão em execução ou não
    
    docker ps -a
    
-> Start, Stop, Restart, Remove
    
    docker start   "Id-Container"
    docker stop    "Id-Container"
    docker restart "Id-Container"
    docker rm      "Id-Container"
    
    docker rm   -f "Id-Container" <--> OBS: Se o container estiver em execusão pode ser preciso forçar a remoção
    
-> Listar imagens dos containers

    docker images
    
-> Verificar uso do container
    
    docker stats


Fonte : https://docs.docker.com/engine/reference/commandline/docker/
