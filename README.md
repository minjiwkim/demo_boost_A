# Demo Boost A

Demo Boost A is a backend web server built with Node.js, designed to support data proxying and basic API routing functionality. It can serve as a base template for more complex backend applications.  
Demo Boost A は、Node.js を使って構築されたバックエンドサーバーで、データのプロキシ処理や基本的な API ルーティング機能をサポートします。より複雑なバックエンドアプリケーションのベーステンプレートとして使用できます。

---

## 📁 Project Structure | プロジェクト構成

```
demo_boost_A-main/
├── boostBackend/
│   ├── app.js             # Main backend server code | メインサーバーコード
│   ├── setupProxy.js      # Proxy configuration | プロキシ設定ファイル
├── package.json           # Node.js dependencies and scripts | Node.js の依存関係とスクリプト
```

---

## 🚀 Getting Started | 開始方法

### 1. Install Dependencies | 必要なモジュールのインストール

```bash
npm install
```

### 2. Run the Server | サーバーの起動

```bash
node boostBackend/app.js
```

Make sure the port defined in `app.js` is available.  
`app.js` に設定されたポートが使用可能であることを確認してください。

---

## ⚙️ Features | 機能

- 🌐 **CORS Configuration | CORS 設定**  
  Fully configured Cross-Origin Resource Sharing (CORS) allowing requests from all domains.  
  すべてのドメインからのリクエストを許可するように CORS（クロスオリジンリソース共有）を設定しました。

- 📦 **Modular Routing | モジュール化されたルーティング**  
  Organized API structure using Express routers:  
  Express のルーターを用いた API 構成：

  - `GET/POST/PUT/DELETE` for `/api/groups`  
  `/api/groups`：グループに関する CRUD 処理

  - CRUD operations for `/api/posts`  
  `/api/posts`：投稿の管理

  - Comments management via `/api/comments`  
  `/api/comments`：コメント処理

  - Badge management via `/api/badges` 
  `/api/badges`：バッジ管理

- 🔁 **Proxy Middleware | プロキシミドルウェア**  
  Requests to `/api` are forwarded to `https://demo-boost-a.onrender.com/` using `http-proxy-middleware`.  
  `/api` へのリクエストは `https://demo-boost-a.onrender.com/` へプロキシ転送されます。

- 🧩 **JSON Parsing & Middleware Setup | JSON 解析とミドルウェア**  
  Automatically parses JSON in request bodies and supports preflight OPTIONS requests.  
  リクエストボディ内のJSONを自動的に解析し、プレフライトOPTIONSリクエストをサポートします。

- 🚀 **Quick Launch | 簡単に起動**  
  Runs on port `3000` by default (or configurable with `PORT` environment variable).  
  デフォルトでポート `3000`（または `PORT` 環境変数で設定）で起動可能です。
