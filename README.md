![](https://grafana.com/static/assets/internal/grafana_logo-web-white-text.svg)

---------------------------------------------------------------

### Install Grafana on Debian or Ubuntu

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
      
>Source: https://grafana.com/docs/grafana/latest/setup-grafana/installation/debian/#install-from-apt-repository
