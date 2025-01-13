### 시스템 요구사항

```bash
GPU driver version 535.183.01 (이상)
CUDA 11.8
CUDNN 8.9
```

소프트웨어 & 업데이트 -> 추가 드라이버

```bash
sudo lshw -c display
sudo ubuntu-drivers devices
```

### 드라이버 설치

```bash
sudo apt install nvidia-driver-550
```

### CUDA Toolkit 11.8 설치

[참고](https://developer.nvidia.com/cuda-11-8-0-download-archive?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=22.04&target_type=deb_network)

```bash
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2204/x86_64/cuda-keyring_1.0-1_all.deb
sudo dpkg -i cuda-keyring_1.0-1_all.deb
sudo apt-get update
sudo apt-get -y install cuda
```
