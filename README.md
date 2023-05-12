# Grafana

##Install Grafana on Debian or Ubuntu

- This topic explains how to install Grafana dependencies, install Grafana on Linux Debian or Ubuntu, and start the Grafana server on your Debian or Ubuntu system.

 - There are multiple ways to install Grafana: using the Grafana Labs APT repository, by downloading a .deb package, or by downloading a binary .tar.gz file. Choose only one of the methods below that best suits your needs.

###Install from APT repository

**To install required packages and download the Grafana repository signing key, run the following commands:**
  sudo apt-get install -y apt-transport-https
  sudo apt-get install -y software-properties-common wget
  sudo wget -q -O /usr/share/keyrings/grafana.key https://apt.grafana.com/gpg.key
