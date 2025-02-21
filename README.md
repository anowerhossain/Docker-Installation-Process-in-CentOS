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


