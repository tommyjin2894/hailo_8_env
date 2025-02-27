# 드라이버 및 툴 설치

### 빌드 툴 설치
```bash
sudo apt dkms
sudo apt build-essential
sudo apt linux-headers-generic
sudo apt bison
sudo apt flex
sudo apt libelf-dev
```

### nouveau 그래픽 드라이버 블랙리스트 추가
- 엔비디아 드라이버를 설치하기 위해

    ```bash
    sudo nano /etc/modprobe.d/blacklist.conf
    ```

    ```bash
    #--- 아래 블랙리스트 내용 추가
    blacklist nouveau
    blacklist lbm-nouveau
    options nouveau modeset=0
    alias nouveau off
    alias lbm-nouveau off
    #---
    ```

    ```bash
    sudo reboot
    ```

### nvidia 드라이버 및 CUDA Toolkit 설치
**드라이버 설치**
```bash
sudo add-apt-repository ppa:graphics-drivers/ppa
sudo apt update
sudo apt install nvidia-driver-520
```

[**cuda-toolkit**](https://developer.nvidia.com/cuda-11-8-0-download-archive?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=22.04&target_type=runfile_local)

```bash
wget https://developer.download.nvidia.com/compute/cuda/11.8.0/local_installers/cuda_11.8.0_520.61.05_linux.run
sudo sh cuda_11.8.0_520.61.05_linux.run
```

```bash
nano ~/.bashrc
#---내용 추가---
export PATH=$PATH:/usr/local/cuda-11.8/bin
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda-11.8/lib64
#-------------
source ~/.bashrc
```

### cudnn 설치

[**cudnn-archive**](https://developer.nvidia.com/rdp/cudnn-archive)
```bash
sudo dpkg -i cudnn-local-repo-ubuntu2204-8.9.7.29_1.0-1_amd64.deb
sudo cp /var/cudnn-local-repo-ubuntu2204-8.9.7.29/cudnn-local-8AE81B24-keyring.gpg /usr/share/keyrings/
sudo apt-get update
sudo apt install libcudnn8 libcudnn8-dev
ls /usr/lib/x86_64-linux-gnu/libcudnn*
```

### 참고. NVIDIA 관련 모두 삭제(문제가 생겼을 시에)


```bash
sudo apt-get remove nvidia* && sudo apt autoremove
sudo apt-get --purge remove 'cuda*'
sudo apt-get autoremove --purge 'cuda*'
sudo apt-get remove --purge '^nvidia-.*'
sudo rm -rf /usr/local/cuda*
sudo rm -rf /usr/lib/nvidia-*
sudo apt-get autoremove
sudo apt-get autoclean
sudo apt-get update
```