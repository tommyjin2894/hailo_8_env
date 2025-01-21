# 우분투 설치후

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt autoremove

cd Downloads
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
```

### 파이어 폭스 삭제(선택)

```bash
sudo apt remove firefox 
sudo apt purge firefox 
sudo rm -Rf /usr/bin/firefox 
sudo snap remove firefox
```

### 우분투 한글화 및 한영 키보드 설정

[참고](https://staraube.tistory.com/105)

### graphviz 설치하기

```bash
sudo apt install graphviz
```