# Linux環境作成手順

## 1.Dockerファイルの作成
- [Dockerfile](../rocky_python/Dockerfile)
- [Pythonの場合、ライブラリを追加](../rocky_python/requirements.txt)

## 2.イメージとコンテナの作成
```sh
## イメージの作成
cd {Dockerfileがあるディレクトリパス}
docker build -t docker-python:1.0 .

## コンテナの作成
docker run --name linux-practice -it -d docker-python:1.0

## コンテナ内に入る
docker exec -it linux-practice bash

## 起動中コンテナの確認
docker ps

## コンテナ起動
docker start linux-practice

## コンテナ停止
docker stop linux-practice
```

## ３.dockerの基本コマンド
```sh
##現在稼働中のコンテナ一覧を表示します。docker ps -a で停止したコンテナも含めて一覧を表示できます。
docker ps
docker ps -a

##指定したコンテナを停止します。docker psで表示されるコンテナIDを使って停止します。
docker stop <コンテナID>

## 停止したコンテナを削除します。
docker rm <コンテナID>

## docker起動
docker start <コンテナID>
```