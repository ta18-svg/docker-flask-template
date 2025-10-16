#  Docker Flask Template

## 概要
**Python（Flask）アプリケーションを Docker 環境で構築・実行**
Flask の基本構造と Docker のコンテナ化をシンプルに作成したものです。
作成理由　Flask アプリを Docker コンテナで動かす仕組みが理解するため

## 使用技術
カテゴリ　　　　｜　技術・ツール
言語　　　　　　　　Python 3.10
フレームワーク　　　Flask　2.3.3
仮想化　　　　　　　Doccker / DockerDesktop
開発環境　　　　　　VSCode
バージョン管理　　　Git /　GitHub

## ディレクトリ構成
DOCKER-FLASK-TEMPLATE/
├─ .vscode/                 # VS Code の設定フォルダ
│  └─ tasks.json            # Docker build/run をワンクリック実行できる設定
│
├─ .dockerignore            # Dockerビルド時に無視するファイル一覧
├─ .gitignore               # Git管理対象から除外するファイル一覧 
│
├─ app.py                   # Flask アプリのメインスクリプト
├─ requirements.txt         # Python の依存パッケージ一覧（Flaskなど）
├─ Dockerfile               # コンテナ環境の設定ファイル
├─ commands.txt             # よく使う Docker コマンドまとめ（学習・確認用）
└─ README.md（任意）       # プロジェクトの説明

実行手順
# 1. イメージをビルド
docker build -t flask-docker-app .

# 2. コンテナ起動
docker run -d -p 5000:5000 --name flask-app flask-docker-app

# 3. 確認
docker ps
# → http://localhost:5000 にアクセス

Hello, Docker World! (Flask on Docker)と表示

#　コンテナ停止
docker stop flask-app

#　コンテナ削除
docker rm flask-app