# HOW to get BASIC UBUNTU docker?
- Web vscode
- ssh connection
- beautiful terminal

# Get Web VScode
```
docker run -it -p 58888:8080 -p 58889:22 -e PASSWORD='password' -e SUDO_PASSWORD='sudo password' -u "$(id -u):$(id -g)" codercom/code-server:latest
```

# Build SSH Connection
