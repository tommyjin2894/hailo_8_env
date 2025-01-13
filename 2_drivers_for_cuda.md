### 시스템 요구사항

```bash
GPU driver version 535.183.01 (이상)
CUDA 11.8
CUDNN 8.9
```

### NVIDIA 관련 모두 삭제

```bash
sudo apt-get --purge remove 'cuda*'
sudo apt-get autoremove --purge 'cuda*'
sudo apt-get remove --purge '^nvidia-.*'
sudo rm -rf /usr/local/cuda*
sudo rm -rf /usr/lib/nvidia-*
sudo apt-get autoremove
sudo apt-get autoclean
sudo apt-get update

```
### installs

```
sudo apt install build-essential
sudo apt update && sudo apt upgrade
```

```
sudo apt install nvidia-driver-550
sudo apt install cuda-toolkit-11.8
```

### CUDA Toolkit 11.8 설치

[참고](https://developer.nvidia.com/cuda-11-8-0-download-archive?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=22.04&target_type=deb_local)

```bash
wget https://developer.download.nvidia.com/compute/cuda/11.8.0/local_installers/cuda_11.8.0_520.61.05_linux.run
sudo sh cuda_11.8.0_520.61.05_linux.run
```

### cudnn 설치

https://developer.nvidia.com/rdp/cudnn-archive
```bash

```
