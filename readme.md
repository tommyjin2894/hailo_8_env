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

# deb 필수 요소 파일들 설치
![image](hailo_1.png)
```
sudo dpkg -i hailort_4.20.0_amd64.deb hailort-pcie-driver_4.20.0_all.deb 
```
