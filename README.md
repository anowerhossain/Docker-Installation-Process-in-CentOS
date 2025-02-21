# Docker-Installation-Process-in-CentOS

### Before installing Docker, ensure that your system is up-to-date
```bash
sudo yum update -y
```

### Install the necessary dependencies for Docker installation
```bash
sudo yum install -y yum-utils device-mapper-persistent-data lvm2
```

### Add the official Docker repository to your system
```bash
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```

### Now, install the Docker engine from the Docker repository
```bash
sudo yum install -y docker-ce docker-ce-cli containerd.io
```

### Start the Docker service and enable it to automatically start on boot
```bash
sudo systemctl start docker
sudo systemctl enable docker
```

### Check the status of docker
```bash
sudo systemctl status docker
```

### Download the latest version of Docker Compose
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/$(curl -s https://api.github.com/repos/docker/compose/releases/latest | jq -r .tag_name)/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

### Set the permissions
```bash
sudo chmod +x /usr/local/bin/docker-compose
```

### Verify the Docker Compose installation
```bash
docker-compose --version
```


