# 파이썬 환경 만들기 및 필요 라이브러리 설치

### Python virtual environment

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.10 python3.10-venv python3.10-distutils python3-tk python3.10-dev
sudo apt install graphviz-dev
```

```bash
python3.10 -m venv .venv_hailo
source .venv_hailo/bin/activate
```

### install hailo drivers
- [로그인 하여 버전에 맞는 파일 다운로드](https://hailo.ai/developer-zone/software-downloads/)

```bash
sudo dpkg -i hailort_4.20.0_amd64.deb
sudo dpkg -i hailort-pcie-driver_4.20.0_all.deb
```

### 라이브러리 설치

```bash
pip install netifaces
pip install pygraphviz
pip install update setuptools==68.0.0
pip install update numba==0.56.4
pip install update numpy==1.23.3
pip install to_install/hailo_dataflow_compiler-3.30.0-py3-none-linux_x86_64.whl
pip install to_install/hailort-4.20.0-cp310-cp310-linux_x86_64.whl
pip install to_install/hailo_model_zoo-2.14.0-py3-none-any.whl
```