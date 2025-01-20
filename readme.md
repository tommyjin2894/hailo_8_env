# 사용 환경 및 요구사항

### 사용 환경

```bash
우분투 22.04
파이썬 3.10 with virtualenv
GPU architecture RTX3060ti
GPU driver version 525
CUDA 11.8
CUDNN 8.9
```

# 기본 설치 및 환경 세팅
```shell
sudo apt install build-essential bison flex libelf-dev dkms
```

### 파이썬 및 가상환경 설치

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.10 python3.10-venv python3.10-distutils python3-tk python3.10-dev
sudo apt install build-essential
sudo apt install graphviz-dev
```
### 환경 생성 및 라이브러리 설치
- [버전선택하여 각각 다운로드](https://hailo.ai/developer-zone/software-downloads/)

```bash
python3.10 -m venv hailo
source hailo/bin/activate

pip install --upgrade pip setuptools
pip install netifaces
pip install pygraphviz
pip install hailo_dataflow_compiler-3.30.0-py3-none-linux_x86_64.whl
pip install hailort-4.20.0-cp310-cp310-linux_x86_64.whl
pip install hailo_model_zoo-2.14.0-py3-none-any.whl 
```

# model zoo 이용

https://github.com/hailo-ai/hailo_model_zoo

```bash
git clone https://github.com/hailo-ai/hailo_model_zoo.git
cd hailo_model_zoo/
pip install -e .
```

- 모델 테스트
  ```bash
  hailomz info mobilenet_v1
  ```

  ```bash
    (hailo_model_zoo) tommy@tommy:~/Downloads/hailo_model_zoo$ hailomz info mobilenet_v1
  <Hailo Model Zoo INFO> Start run for network mobilenet_v1 ...
  <Hailo Model Zoo INFO> 
  	task:                    classification
  	input_shape:             224x224x3
  	output_shape:            1001
  	operations:              1.14G
  	parameters:              4.22M
  	framework:               tensorflow
  	training_data:           imagenet train
  	validation_data:         imagenet val
  	eval_metric:             Accuracy (top1)
  	full_precision_result:   70.97
  	source:                  https://github.com/tensorflow/models/tree/v1.13.0/research/slim
  	license_url:             https://github.com/tensorflow/models/blob/master/LICENSE
  (hailo_model_zoo) tommy@tommy:~/Downloads/hailo_model_zoo$ 
  ```
