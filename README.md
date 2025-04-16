# Demo Boost A

Demo Boost A is a backend web server built with Node.js, designed to support data proxying and basic API routing functionality. It can serve as a base template for more complex backend applications.

---

## 📁 Project Structure

```
demo_boost_A-main/
├── boostBackend/
│   ├── app.js             # Main backend server code
│   ├── setupProxy.js      # Proxy configuration
├── package.json           # Node.js dependencies and scripts
```

---

## 🚀 Getting Started

### 1. Install Dependencies

```bash
npm install
```

### 2. Run the Server

```bash
node boostBackend/app.js
```

Make sure the port defined in `app.js` is available.

---

## ⚙️ Features

- 🌐 **CORS Configuration**  
  Fully configured Cross-Origin Resource Sharing (CORS) allowing requests from all domains.

- 📦 **Modular Routing**  
  Organized API structure using Express routers:
  - `GET/POST/PUT/DELETE` for `/api/groups`
  - CRUD operations for `/api/posts`
  - Comments management via `/api/comments`
  - Badge-related APIs on `/api/badges`

- 🔁 **Proxy Middleware**  
  Requests to `/api` are forwarded to `https://demo-boost-a.onrender.com/` using `http-proxy-middleware`.

- 🧩 **JSON Parsing & Middleware Setup**  
  Automatically parses JSON in request bodies and supports preflight OPTIONS requests.

- 🚀 **Quick Launch**  
  Runs on port `3000` by default (or configurable with `PORT` environment variable).

---

# 📘 README（日本語）

Demo Boost A は、Node.js を使って構築されたバックエンドサーバーで、データのプロキシ処理や基本的な API ルーティング機能をサポートします。より複雑なバックエンドアプリケーションのベーステンプレートとして使用できます。

---

## 📁 プロジェクト構成

```
demo_boost_A-main/
├── boostBackend/
│   ├── app.js             # メインサーバーコード
│   ├── setupProxy.js      # プロキシ設定ファイル
├── package.json           # Node.js の依存関係とスクリプト
```

---

## 🚀 開始方法

### 1. 必要なモジュールのインストール

```bash
npm install
```

### 2. サーバーの起動

```bash
node boostBackend/app.js
```

`app.js` に設定されたポートが使用可能であることを確認してください。

---

## ⚙️ 機能

- 🌐 **CORS 設定**  
  すべてのドメインからのリクエストを許可するように CORS（クロスオリジンリソース共有）を設定。

- 📦 **モジュール化されたルーティング**  
  Express のルーターを用いた API 構成：
  - `/api/groups`：グループに関する CRUD 処理
  - `/api/posts`：投稿の管理
  - `/api/comments`：コメント処理
  - `/api/badges`：バッジに関する API

- 🔁 **プロキシミドルウェア**  
  `/api` へのリクエストは `https://demo-boost-a.onrender.com/` へプロキシ転送。

- 🧩 **JSON 解析とミドルウェア**  
  JSON 本文の自動解析と preflight OPTIONS リクエストへの対応。

- 🚀 **簡単に起動**  
  デフォルトでポート `3000`（または `PORT` 環境変数で設定）で起動可能。