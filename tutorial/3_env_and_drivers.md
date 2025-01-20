### env
```bash
python3.10 -m venv .venv_hailo
source .venv_hailo/bin/activate
```

### install drivers
```bash
sudo dpkg -i hailort_4.20.0_amd64.deb
sudo dpkg -i hailort-pcie-driver_4.20.0_all.deb
```

### 라이브러리 설치
```
pip install netifaces
pip install pygraphviz
pip install update setuptools==68.0.0
pip install update numba==0.56.4
pip install update numpy==1.23.3
pip install to_install/hailo_dataflow_compiler-3.30.0-py3-none-linux_x86_64.whl
pip install to_install/hailort-4.20.0-cp310-cp310-linux_x86_64.whl
pip install to_install/hailo_model_zoo-2.14.0-py3-none-any.whl
```