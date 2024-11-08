FROM rockylinux:9.3
USER root

# パッケージの更新とPythonのインストール
RUN dnf -y update
RUN dnf -y install python3.9
RUN dnf -y install python3-pip
RUN dnf clean all

# 必要なライブラリのコピー
COPY requirements.txt .
RUN python3.9 -m pip install -r requirements.txt

## 環境変数の指定
ENV DOCKER_TEST=docer-test