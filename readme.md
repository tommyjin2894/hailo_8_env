# 사용 환경 및 요구사항

### System Requirements

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

### 사용 환경

```
우분투 22.04
파이썬 3.10 with virtualenv
GPU architecture RTX3060ti
GPU driver version 525
CUDA 11.8
CUDNN 8.9
```

## 기본 설치 및 환경 세팅
```shell
sudo apt install build-essential bison flex libelf-dev dkms
```

### 파이썬 및 가상환경 설치

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.10 python3.10-venv python3.10-distutils
sudo apt-get install python3.10-dev
sudo apt-get install build-essential
sudo apt-get install graphviz-dev
```
### 환경 생성 및 라이브러리 설치

```bash
python3.10 -m venv hailo_model_zoo
source hailo_model_zoo/bin/activate

pip install --upgrade pip setuptools
pip install netifaces
pip install pygraphviz
pip install hailo_dataflow_compiler-3.30.0-py3-none-linux_x86_64.whl
pip install hailort-4.20.0-cp310-cp310-linux_x86_64.whl
pip install hailo_model_zoo-2.14.0-py3-none-any.whl 
```

## model zoo 이용

```bash
git clone https://github.com/hailo-ai/hailo_model_zoo.git
cd hailo_model_zoo/
```
