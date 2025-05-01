以下は、提供された内容の日本語訳です：

---

# 🚀 Monad テストネット自動化ツール

![Monad-BOT](https://img.shields.io/badge/Monad-BOT-blue.svg) ![License](https://img.shields.io/badge/License-ISC-green.svg) ![Platform](https://img.shields.io/badge/Platform-MacOS%2FLinux%2FWindows-lightgrey.svg)

**Monad-Testnet-Automation** は、仮想通貨サービスと連携してトークンのスワップやステーキングを自動化するためのブロックチェーン自動化ツールです。**リアルタイムダッシュボード**を通じて操作状況を監視し、トランザクションを記録、トークンの **ラップ/アンラップ** および **ステーキング/アンステーキング** などの操作を自動で行います。

---

## ✨ 特徴

✔️ **インタラクティブダッシュボード** – 残高、ネットワーク状況、取引履歴をリアルタイムで表示  
✔️ **自動サイクル** – スワップやステーキング操作を定期的に実行  
✔️ **ブロックチェーン連携** – `ethers.js` によりスマートコントラクトをスムーズに実行  
✔️ **複数サービス対応** – Rubic Swap、Izumi Swap、Bean Swap などをサポート  
✔️ **秘密鍵の安全な管理** – `private.key` から安全に読み込み  
✔️ **柔軟な設定** – サイクル、RPC、コントラクトアドレスを簡単にカスタマイズ  
✔️ **複数ウォレット対応** – 複数の秘密鍵で同時に実行可能  

---

## 📦 インストールガイド

### ✅ 前提条件

以下のソフトウェアがインストールされている必要があります：
- **Node.js**（バージョン16以上）– [こちらからダウンロード](https://nodejs.org/)
- **Git**（リポジトリをクローンするために必要、任意）

### 🔧 インストール手順

#### 🖥️ MacOS & Linux
1️⃣ ターミナルを開き、以下を実行：
```bash
# リポジトリをクローン
git clone https://github.com/bronkdrop/Monad-Testnet-Bot.git
cd Monad-Testnet-Bot
# 依存パッケージをインストール
npm install
```

2️⃣ `private.key` ファイルに秘密鍵を追加（複数の場合は1行に1つ）：
```bash
nano private.key
```

3️⃣ Bot を起動：
```bash
npm start
```

#### 🖥️ Windows
1️⃣ **PowerShell** を開き、以下を実行：
```powershell
# リポジトリをクローン
git clone https://github.com/bronkdrop/Monad-Testnet-Bot.git
cd Monad-Testnet-Bot

# 依存パッケージをインストール
npm install
```

2️⃣ `private.key` に秘密鍵を追加（メモ帳などで1行ずつ）：
```powershell
notepad private.key  # メモ帳でファイルを編集
```
秘密鍵を貼り付け、保存してメモ帳を閉じてください。

3️⃣ Bot を起動：
```powershell
npm start
```

---

## 🛠️ 設定

`config/config.json` ファイルを編集して以下をカスタマイズ可能：
- **ネットワーク設定**：RPC URL やブロックエクスプローラー
- **API エンドポイント**：ステーキングや流動性サービス用
- **スマートコントラクトのアドレス**
- **サイクルのパラメータ**：実行間隔、クールダウン、遅延時間など

---

## 🚀 使用方法

### 📊 Bot の実行
- Bot を起動：
  ```bash
  npm start
  ```
- ターミナルダッシュボードには以下が表示されます：
  - ✅ 残高の更新
  - 🔄 トランザクションログ
  - ⏳ スワップ／ステーキングの状況
  - 📊 サイクルの進捗状況
  - 🔄 **複数ウォレットの処理**

### 🔄 対応サービス一覧
Bot は以下のサービスに対応しています：
- **トランザクション**：wallets.txt に記載されたウォレットへ MON をランダム送信、スマートコントラクトのデプロイ  
- **スワップ**：Uniswap、Rubic Swap、Izumi Swap、Bean Swap、Monorail  
- **ステーキング**：Magma Staking、aPriori Staking、Kitsu Staking  
- **トークン操作**：残高チェック、自動ラップ／アンステーク  
- **マルチウォレット**：複数のウォレットに対しループ実行対応

---
