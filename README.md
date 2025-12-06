# CodeAssist
# Installation

## 1. Docker

### Update System
```bash
sudo apt update -y && sudo apt upgrade -y
```

### Remove Old Docker Packages
```bash
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove -y $pkg; done
```

###
