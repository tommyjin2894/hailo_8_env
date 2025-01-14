https://docs.docker.com/desktop/setup/install/linux/ubuntu/

### 기존 도커 관련 삭제하기
```bash
for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done
```

### gnome 설치 안되어 있을 시에
```bash
sudo apt install gnome-terminal
```

### 도커 설치
```
# 도커 공식 GPG 키 등록:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# apt 레포지 토리 등록 후 업데이트:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

# 도커 최신 버전 설치
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# 잘 설치 되었는지 확인
sudo docker run hello-world
```

### 도커 이미지 만들기
```
sudo docker build -t hailo .
```
