#  Docker Flask Template

## 概要
**Python（Flask）アプリケーションを Docker 環境で構築・実行**
Flask の基本構造と Docker のコンテナ化をシンプルに作成したものです。
作成理由　Flask アプリを Docker コンテナで動かす仕組みが理解するため

## 使用技術
カテゴリ: 技術・ツール<br>
言語: Python 3.10<br>
フレームワーク: Flask　2.3.3<br>
仮想化: Doccker / DockerDesktop<br>
開発環境: VSCode<br>
バージョン管理: Git /　GitHub<br>

## ディレクトリ構成
DOCKER-FLASK-TEMPLATE/<br>
├─ .vscode/                 # VS Code の設定フォルダ<br>
│  └─ tasks.json            # Docker build/run をワンクリック実行できる設定<br>
│<br>
├─ .dockerignore            # Dockerビルド時に無視するファイル一覧<br>
├─ .gitignore               # Git管理対象から除外するファイル一覧 <br>
│<br>
├─ app.py                   # Flask アプリのメインスクリプト<br>
├─ requirements.txt         # Python の依存パッケージ一覧（Flaskなど）<br>
├─ Dockerfile               # コンテナ環境の設定ファイル<br>
├─ commands.txt             # よく使う Docker コマンドまとめ（学習・確認用）<br>
└─ README.md（任意）       # プロジェクトの説明<br>

実行手順
## 1. イメージをビルド
docker build -t flask-docker-app .

## 2. コンテナ起動
docker run -d -p 5000:5000 --name flask-app flask-docker-app

## 3. 確認
docker ps<br>
 → http://localhost:5000 にアクセス<br>

Hello, Docker World! (Flask on Docker)と表示

## コンテナ停止
docker stop flask-app

## コンテナ削除
docker rm flask-app