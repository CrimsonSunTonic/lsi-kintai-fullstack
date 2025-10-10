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
cp .\lsi-kintai-nextjs-frontend\.env.dev .\lsi-kintai-nextjs-frontend\.env
```

#### Linux / macOS

```bash
cp ./lsi-kintai-nestjs-backend/.env.dev ./lsi-kintai-nestjs-backend/.env
cp ./lsi-kintai-nextjs-frontend/.env.dev ./lsi-kintai-nextjs-frontend/.env
```

### 5. サーバーを立ち上げる

```bash
docker compose up -d --build
```
