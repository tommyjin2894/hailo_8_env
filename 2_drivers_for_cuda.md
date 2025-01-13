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

### build-essential tools install
```
sudo apt install build-essential
sudo apt update && sudo apt upgrade
```

### nvidia-driver installing
```
sudo apt install nvidia-driver-550
```

### CUDA Toolkit 11.8 설치

[참고](https://developer.nvidia.com/cuda-11-8-0-download-archive?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=22.04&target_type=deb_local)

```bash
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2204/x86_64/cuda-ubuntu2204.pin
sudo mv cuda-ubuntu2204.pin /etc/apt/preferences.d/cuda-repository-pin-600
wget https://developer.download.nvidia.com/compute/cuda/11.8.0/local_installers/cuda-repo-ubuntu2204-11-8-local_11.8.0-520.61.05-1_amd64.deb
sudo dpkg -i cuda-repo-ubuntu2204-11-8-local_11.8.0-520.61.05-1_amd64.deb
sudo cp /var/cuda-repo-ubuntu2204-11-8-local/cuda-*-keyring.gpg /usr/share/keyrings/
sudo apt-get update
sudo apt-get -y install cuda
```

### cudnn 설치

https://developer.nvidia.com/rdp/cudnn-archive
```bash

```
