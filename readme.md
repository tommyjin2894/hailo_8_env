# Hailo model pt 모델 추론 과정

pt 모델 변환 부터 hailo-8 에서 구동하여 추론까지의 과정

### 사용 환경
```bash
우분투 22.04
파이썬 3.10 with virtualenv(.venv)
GPU RTX3060ti
GPU NVIDIA-SMI 535.183.01
cuda 11.8
cuDNN 8.9
```

### 목차

1. [우분투 설치후](tutorial/1_after_ubuntu_installed.md)
2. [드라이버 및 쿠다 설치](tutorial/2_drivers_for_cuda.md)
3. [파이썬 환경 만들기 및 필요 라이브러리](tutorial/3_python_env.md)
4. [hailo 8 1_parsing](tutorial/4_parsing_process.ipynb)
5. [hailo 8 2_optimization and compile](tutorial/5_Optimization_compile.ipynb)