# lsi-kintai-fullstack

## 概要
このリポジトリは、勤怠管理システムのフルスタック実装です。  
バックエンドは NestJS、フロントエンドは Next.js を使用しています。

---

## 必要条件

- [Docker](https://www.docker.com/) & [Docker Compose](https://docs.docker.com/compose/)
- [Git](https://git-scm.com/)

---

## セットアップ手順

### 1. ベースフォルダをクローン

```bash
git clone https://github.com/CrimsonSunTonic/lsi-kintai-fullstack.git

cd lsi-kintai-fullstack
```

### 2. バックエンドをクローン

```bash
git clone https://github.com/CrimsonSunTonic/lsi-kintai-nestjs-backend.git
```

### 3. フロントエンドをクローン

```bash
git clone https://github.com/CrimsonSunTonic/lsi-kintai-nextjs-frontend.git
```

### 4. `.env` ファイルを作成

#### Windows

```powershell
cp .\lsi-kintai-nestjs-backend\.env.dev .\lsi-kintai-nestjs-backend\.env

cp .\lsi-kintai-nextjs-frontend\.env.example .\lsi-kintai-nextjs-frontend\.env
```

#### Linux / macOS

```bash
cp ./lsi-kintai-nestjs-backend/.env.dev ./lsi-kintai-nestjs-backend/.env

cp ./lsi-kintai-nextjs-frontend/.env.example ./lsi-kintai-nextjs-frontend/.env
```

### 5. データベースフォルダを作成

```bash
mkdir db-data
```

### 6. サーバーを立ち上げる

```bash
docker compose up -d --build
```

## フォルダ構成

```
lsi-kintai-fullstack/
├── docker-compose.yml          # 全体構成ファイル
├── db-data/                    # PostgreSQL 永続化データ
├── lsi-kintai-nestjs-backend/  # NestJS バックエンド
│   ├── prisma/                 # Prisma スキーマとマイグレーション
│   ├── src/                    # ソースコード
│   ├── .env.dev                # 開発用環境変数ファイル
│   └── Dockerfile              # バックエンド用 Docker 設定
├── lsi-kintai-nextjs-frontend/ # Next.js フロントエンド
│   ├── src/                    # ページやコンポーネント
│   ├── public/                 # 静的ファイル
│   ├── .env.example            # 環境変数テンプレート
│   └── Dockerfile              # フロントエンド用 Docker 設定
└── README.md                   # このドキュメント
```