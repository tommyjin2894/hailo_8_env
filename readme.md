# 사용 환경 및 요구사항

System Requirements

```
Ubuntu 20.04/22.04, 64 bit (supported also on Windows, under WSL2)
Python 3.8/3.9/3.10, including pip and virtualenv
Hailo Dataflow Compiler v3.30.0 (Obtain from hailo.ai)
HailoRT 4.20.0 (Obtain from hailo.ai) - required only for inference on Hailo-8.
The Hailo Model Zoo supports Hailo-8 / Hailo-10H connected via PCIe only.
Nvidia’s Pascal/Turing/Ampere GPU architecture (such as Titan X Pascal, GTX 1080 Ti, RTX 2080 Ti, or RTX A4000)
GPU driver version 525
CUDA 11.8
CUDNN 8.9
```

사용 환경

```
우분투 22.04
파이썬 3.10 with virtualenv
GPU architecture RTX3060ti
GPU driver version 525
CUDA 11.8
CUDNN 8.9
```

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
