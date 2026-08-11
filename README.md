# Chatinable Open

**インストーラを1つ実行するだけで、Java・Spring Boot・SQL・Python・TypeScript の
学習環境がまるごと手に入る、オールインワン学習デスクトップアプリです。**

JDK も Node.js も Python も DB も、個別にインストールする必要はありません。
教材・コードエディタ・実行環境・AI Teacher がひとつのアプリに統合されています。

Chatinable Open は **BYOK 版**です。AI Teacher 機能はご自身の
[Anthropic API キー](https://console.anthropic.com/) で動作します
（Bring Your Own Key）。

---

## ダウンロード

**［[最新版をダウンロード](../../releases/latest)］**

`Chatinable-Open-Setup-<version>.exe` をダウンロードして実行してください。

| | |
|---|---|
| 対応 OS | Windows 10 / 11（64bit） |
| インストーラサイズ | 約 200MB |
| インストール後 | 約 600MB |
| 管理者権限 | 不要（ユーザー領域にインストールされます） |

インストーラは署名されていないため、SmartScreen の警告が出る場合があります。
「詳細情報」→「実行」で進めてください。

インストーラの起動時に言語を選択できます（日本語・英語・フランス語・ドイツ語・
スペイン語・ポルトガル語(BR)・簡体中文・韓国語・インドネシア語）。
選択した言語がアプリの初期 UI 言語になります。

---

## 初回設定

AI Teacher を使うには API キーの登録が必要です。⚙ 設定パネルから登録してください。
キーは OS の資格情報ストア（`safeStorage`）で暗号化して端末内に保存され、
外部に送信されるのは各 API 提供元のみです。

| キー | 用途 | 必須 | 取得先 |
|---|---|---|---|
| Anthropic API キー | AI Teacher のチャット（ヒント・レビュー・自由質問） | 必須 | [console.anthropic.com](https://console.anthropic.com/) |
| Gemini API キー | AI Teacher の回答の音声読み上げ | 任意 | [aistudio.google.com](https://aistudio.google.com/apikey) |

> **料金について**
> API の利用料金は、各 API 提供元からお客様に直接請求されます。
> 本アプリの作者は課金に関与しません。

---

## 収録コース

| コース | 種別 | 問数 |
|---|---|---|
| Java 基礎編 | Java | 136 |
| Java 上級編 | Java | 70 |
| Java テスト 基礎＆実践 | JUnit 5 / Gradle | 137 |
| Spring Boot 基礎編 | Spring Boot 4 | 10 |
| Spring Boot + RDB 基礎編 | Spring Boot 4 + JPA | 3 |
| Java + RDB 基礎編 | Java + HSQLDB | 5 |
| SQL 基礎編 | HSQLDB | 8 |
| Python 基礎編 | Python | 10 |
| TypeScript 基礎編 | TypeScript | 8 |

教材は全 9 言語にローカライズされています。

---

## 同梱されるもの

個別インストールは一切不要です。すべてアプリに同梱されています。

| ランタイム | 内容 | 用途 |
|---|---|---|
| Java | Temurin JDK 25 を jlink で最小化（`javac` 同梱） | Java / テスト / Spring Boot 系 |
| Node.js | portable Node.js 24 LTS | TypeScript（type stripping で `.ts` を直接実行） |
| Python | embeddable Python 3.13 | Python |
| HSQLDB | hsqldb 2.7.3 | SQL / RDB 系 |

Gradle は Spring Boot コースの初回実行時に Gradle Wrapper が自動取得します
（このときだけネットワーク接続が必要です）。

---

## 主な機能

- **設問 × エディタ × 実行結果 × AI Teacher** を1画面に統合
- **AI Teacher**（💡ヒント / 🔍レビュー / 自由質問）。会話は設問ごとに保持されます
- **音声読み上げ**。AI の回答を Gemini Live で音声解説（声・話し方を選択可）
- **ワークスペース**。書いたコードと学習履歴は `~/chatinable-open/` に保存されます
- **ライト / ダークテーマ**、フォント・フォントサイズ変更
- **簡易ターミナル**、Spring Boot アプリのブラウザプレビュー

---

## アンインストール

Windows の「設定」→「アプリ」から **Chatinable Open** をアンインストールしてください。

ワークスペース（`~/chatinable-open/`）と設定は残ります。
完全に削除する場合は、以下も手動で削除してください。

```
%USERPROFILE%\chatinable-open\
%APPDATA%\Chatinable Open\
```

---

## このリポジトリについて

**このリポジトリは Chatinable Open のインストーラを配布するためのものです。
アプリケーションのソースコードは公開していません。**

- 不具合の報告・要望は [Issues](../../issues) へお願いします
- 配布物は [Releases](../../releases) にあります

`LICENSE`（MIT）はこのリポジトリに含まれるファイルに適用されます。
アプリケーション本体の使用条件はインストーラに表示される使用許諾に従います。
