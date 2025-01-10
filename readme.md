# 사용 환경
ubuntu 22.04

# 기본 설치
```shell
sudo apt install build-essential bison flex libelf-dev dkms
```

# 모듈빌드를 위한 kernel header
```
sudo apt install linux-headers-$(uname -r)
```

# https://github.com/hailo-ai/hailort-drivers/blob/master/download_firmware.sh 다운 받아서 firmware 위치에 옮겨주기
```
cd /home/tommy/Downloads/
```
