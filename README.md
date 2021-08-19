# HOW to get BASIC UBUNTU docker?
- Web vscode
- ssh connection

# Get Web VScode
```
docker run -it -p 8080:8080 -p 22:22 -e PASSWORD='password' -e SUDO_PASSWORD='sudo password' -u "$(id -u):$(id -g)" codercom/code-server:latest
```

# Reset Password
reset root password
```
sudo passwd root
```

reset coder password
```
su
passwd coder
exit
```

# Build SSH Connection
APT Repository 최신 업데이트
```
sudo apt-get update
sudo apt-get upgrade
```
  
SSH 서버 완전 삭제 후 재설치
```
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```
  
config 파일 설정
```
sudo nano /etc/ssh/sshd_config
```

다음의 내용을 '/etc/ssh/sshd_config'에 추가한다.
```
Port 22
Protocol 2
```

```
PasswordAuthentication no -> yes
```

SSH 서버 재시작
```
sudo service ssh --full-restart
sudo service ssh restart
```

로컬접속 확인
```
ssh localhost
```
접속에 성공했다면 다음 스텝으로 넘어갈 준비가 되었다.



