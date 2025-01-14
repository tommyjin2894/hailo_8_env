### 시스템 설치 사항

```bash
GPU driver version 550.120
CUDA 12.4
CUDNN 9.6.0
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

### nvidia 드라이버 및 CUDA Toolkit 설치

[링크](https://developer.nvidia.com/cuda-11-8-0-download-archive?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=22.04&target_type=deb_local)

```bash
wget https://developer.download.nvidia.com/compute/cuda/12.4.0/local_installers/cuda_12.4.0_550.54.14_linux.run
sudo sh cuda_12.4.0_550.54.14_linux.run
```

### cudnn 설치

[링크](https://developer.nvidia.com/cudnn-downloads?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=22.04&target_type=deb_local)
```bash
wget https://developer.download.nvidia.com/compute/cudnn/9.6.0/local_installers/cudnn-local-repo-ubuntu2204-9.6.0_1.0-1_amd64.deb
sudo dpkg -i cudnn-local-repo-ubuntu2204-9.6.0_1.0-1_amd64.deb
sudo cp /var/cudnn-local-repo-ubuntu2204-9.6.0/cudnn-*-keyring.gpg /usr/share/keyrings/
sudo apt-get update
sudo apt-get -y install cudnn

sudo apt-get -y install cudnn-cuda-12
```

### conda 설치

```
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm ~/miniconda3/miniconda.sh
```

```
source ~/miniconda3/bin/activate
conda init --all
```
