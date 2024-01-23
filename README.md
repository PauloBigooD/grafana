## What is  ![](https://grafana.com/static/assets/internal/grafana_logo-web-white-text.svg) ?


Grafana is a powerful tool for real-time data analysis. The platform is highly customizable, allowing users to create dashboards with different types of graphs, tables, alerts and interactive panels. Grafana supports a wide variety of data sources, including relational databases, NoSQL, monitoring systems, and other cloud services. In addition, it has an active community and a large number of plugins and integrations available.

**The Grafana installation can be installed in three ways:**

- Installation from source code
- Installation from packages
- Docker Image

---
`Whichever installation method you choose, the process is generally well documented and can easily be found in the official Grafana documentation.` 

Source:  ![](https://img.shields.io/badge/Grafana-F4FA58?style=plastic&logo=grafana&logoColor=write)


## Installation of Grafana using Docker containers.


### Install [![Docker](https://img.shields.io/badge/Docker-2496ED?style=plastic&logo=docker&logoColor=white)]() Engine on Ubuntu

**OS requirements🔗**

+ **To install Docker Engine, you need the 64-bit version of one of these Ubuntu versions:**

    * Ubuntu Lunar 23.04
    * Ubuntu Kinetic 22.10
    * Ubuntu Jammy 22.04 (LTS)
    * Ubuntu Focal 20.04 (LTS)
    * Ubuntu Bionic 18.04 (LTS)
 
+ Docker Engine is compatible with `x86_64` (or `amd64`), `armhf`, `arm64`, and `s390x` architectures.

#### Uninstall old versions

Older versions of Docker went by the names of `docker`, `docker.io`, or `docker-engine`, you might also have installations of `containerd` or `runc.` Uninstall any such older versions before attempting to install a new version:

    sudo apt-get remove docker docker-engine docker.io containerd runc

> `apt-get` might report that you have none of these packages installed.

Images, containers, volumes, and networks stored in `/var/lib/docker/` aren’t automatically removed when you uninstall Docker. If you want to start with a clean installation, and prefer to clean up any existing data, read the uninstall Docker Engine section.

### Install using shell script

If you wish, there is the option to run the automatic Docker installation script `install-docker.sh`. After accessing the **zabbix/zabbix-server-docker** repository, type the following command:

      ./install-docker.sh

Now just wait for the installation to finish!

---
## Install Grafana using the apt repository
 on [![Debian](https://img.shields.io/badge/Debian-gray?style=plastic&logo=Debian&logoColor=red)](https://www.debian.org/) or [![Ubuntu](https://img.shields.io/badge/Ubuntu-black?style=plastic&logo=Ubuntu&logoColor=write)](https://ubuntu.com/)

- This topic explains how to install Grafana dependencies, install Grafana on Linux Debian or Ubuntu, and start the Grafana server on your Debian or Ubuntu system.

 - There are multiple ways to install Grafana: using the Grafana Labs APT repository, by downloading a .deb package, or by downloading a binary `.tar.gz` file. Choose only one of the methods below that best suits your needs.

#### Install from APT repository

- [ ] 1  **To install required packages and download the Grafana repository signing key, run the following commands:**

      sudo apt-get install -y apt-transport-https
  
      sudo apt-get install -y software-properties-common wget
  
      sudo wget -q -O /usr/share/keyrings/grafana.key https://apt.grafana.com/gpg.key

- [ ] 2  **To add a repository for stable releases, run the following command:**

      echo "deb [signed-by=/usr/share/keyrings/grafana.key] https://apt.grafana.com stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list

- [ ] 3  **To add a repository for beta releases, run the following command:**

      echo "deb [signed-by=/usr/share/keyrings/grafana.key] https://apt.grafana.com beta main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
      
- [ ] 4  **After you add the repository, run the following commands to install the OSS or Enterprise release:**

      # Update the list of available packages
      sudo apt-get update

      # Install the latest OSS release:
      sudo apt-get install grafana

      # Install the latest Enterprise release:
      sudo apt-get install grafana-enterprise
      
> Source: [![Grafana](https://img.shields.io/badge/Grafana-F4FA58?style=plastic&logo=grafana&logoColor=write)](https://grafana.com/docs/grafana/latest/setup-grafana/installation/debian/#install-from-apt-repository)

<img align="right" width="100" height="100" src="https://uploaddeimagens.com.br/images/004/463/466/full/st_small_507x507-pad_600x600_f8f8f8-removebg-preview_%281%29.png?1683896989">

