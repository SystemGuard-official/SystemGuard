# SystemGuard Guide

## Installation

### Prerequisites

Before installing SystemGuard, ensure that the following dependency is installed:

#### **Required Packages**

The following packages are required for the SystemGuard app to function properly:

```bash
# debian based distros
sudo apt-get update
sudo apt-get install git curl wget unzip iptables jq nmap
```

```bash
sudo dnf update -y
sudo dnf install -y git curl wget unzip iptables jq namp
```

```bash
sudo yum update -y
sudo yum install -y git curl wget unzip iptables jq nmap
```

#### **Anaconda3/Miniconda3**

This is required for the app to run properly.
  
To install Miniconda3, run the following commands:

```bash
# Install Miniconda3
wget https://raw.githubusercontent.com/codeperfectplus/HackScripts/main/setup/install_miniconda.sh
chmod +x install_miniconda.sh && ./install_miniconda.sh
```

Install Docker as it is required by the prometheus and grafana services. install docker using the following commands,
based on your distro:

```bash
# debian / apt based distros
wget https://raw.githubusercontent.com/codeperfectplus/HackScripts/refs/heads/main/setup/setup_docker.sh
chmod +x setup_docker.sh && ./setup_docker.sh

# centos / yum based distros
wget https://raw.githubusercontent.com/codeperfectplus/HackScripts/refs/heads/main/setup/setup_docker_centos.sh
chmod +x setup_docker_centos.sh && ./setup_docker_centos.sh
```

#### Installation Steps

1. Download and set up the SystemGuard installer:

```bash
wget https://raw.githubusercontent.com/codeperfectplus/SystemGuard/production/setup.sh
chmod +x setup.sh && sudo mv setup.sh /usr/local/bin/systemguard-installer
```

2. Run the following command to install the SystemGuard app:

```bash
sudo systemguard-installer --install
# if above command doesn't work, try full path
sudo /usr/local/bin/systemguard-installer --install
```

## Uninstallation

To uninstall the SystemGuard app from your system, use the following command:

```bash
sudo systemguard-installer --uninstall
```

This will remove SystemGuard and its related configurations from your system.

---


## Fix Errors

In case you encounter any errors or issues with the SystemGuard app, you can attempt to fix them by running:

```bash
sudo systemguard-installer --fix
```

This command will attempt to automatically fix any issues with the app.

---

## Restore

If you need to restore the SystemGuard app (e.g., after an improper shutdown or system crash), you can run:

```bash
sudo systemguard-installer --restore
```

This will restore the app to its previous functional state without affecting its configurations.

---

## Checking System Status

To get a detailed report on the status of the SystemGuard app, including its services, use the command:

```bash
sudo systemguard-installer --status
```

---

## Health Check

To ensure that SystemGuard and its dependencies are running smoothly, you can perform a system health check by running:

```bash
sudo systemguard-installer --health
```

This will check various system resources and provide insights into the overall health of your system.

---

## Cleaning Backups

To clean up all the backups created by SystemGuard and free up disk space, use the following command:

```bash
sudo systemguard-installer --clean-backups
```

---

## SystemGuard Logs

To check the logs for SystemGuard, which can be helpful for troubleshooting or monitoring purposes, run:

```bash
sudo systemguard-installer --logs
```

---

## Stopping the SystemGuard Server

If you need to stop the SystemGuard server, you can do so by running:

```bash
sudo systemguard-installer --stop
```

---

## Help

For a list of all available commands and their descriptions, run:

```bash
systemguard-installer --help
```

---

## Release Notes

| Version    | Release Date | Status      | Key Features                                        |
| ---------- | ------------ | ----------- | --------------------------------------------------- |
| v1.0.4     | 13/09/2024   | Stable      | Stable version of pre-release features, stability   |
| v1.0.4-pre | 10/09/2024   | Pre-release | Auto-update, website monitoring, graph improvements |
| v1.0.3     | 05/09/2024   | Stable      | Performance optimization, CPU graphs, bug fixes     |
| v1.0.2     | 02/09/2024   | Deprecated  | Minor fixes, initial graph improvements             |
| v1.0.1     | 31/08/2024   | Deprecated  | Initial version with basic monitoring               |
| v1.0.0     | 30/08/2024   | Deprecated  | Initial release                                     |
