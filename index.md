# 🧑‍💻 ポートフォリオ

こんにちは。  
佐久間 崇征です。  
普段は VB.NET を中心に開発をしていますが、  
副業として **Python を用いた Web 自動化ツールの開発** を行っています。

本ページでは、代表作である **「CSV → Web登録 自動化ツール」** を紹介します。

---

# 🚀 CSV → Web登録 自動化ツール  
**（Python / Streamlit / Selenium / SQLAlchemy）**

このツールは、CSV の内容を基に **Webフォームへ自動で入力・送信するアプリケーション**です。

- Streamlit によるシンプルな UI  
- Selenium によるブラウザ自動操作  
- SQLite / SQLAlchemy によるログ管理  
- pytest による単体テスト  
- メモリDBを活用したテストも実装  

実務レベルの品質を目指して作成しました。

---

## 🎥 デモ動画

https://github.com/user-attachments/assets/e273c326-2261-487c-994f-78ffcd4db0ce

---

# ✨ 主な機能

- CSV をアップロードして即実行  
- 各行を Selenium で自動入力し Web 登録  
- ステージ別エラー判定（input / submit / confirm / unexpected）  
- Run / RunDetail にログ記録  
- Streamlit UI に成功 / 失敗を一覧表示  
- pytest による信頼性の高いテストコード実装  

---

# 🛠 技術スタック

| 分類 | 技術 |
|------|------|
| 言語 | Python |
| UI | Streamlit |
| 自動操作 | Selenium WebDriver |
| ORM | SQLAlchemy |
| DB | SQLite |
| CSV解析 | pandas |
| テスト | pytest（MagicMock / monkeypatch / in-memory DB） |

---

# 📁 ソースコードはこちら

👉 **GitHub リポジトリ**  
https://github.com/SakumaTakayuki/CSVtoWEB

---

# 📘 プロジェクト構成（抜粋）
<img width="610" height="578" alt="image" src="https://github.com/user-attachments/assets/7b2a439d-d437-4389-90f9-8d307d08cc41" />

---

# 🧪 テストについて（品質へのこだわり）

このツールでは、信頼性を高めるために **pytest を活用したテストを徹底** しています。

### 🔹 Selenium処理のテスト  
- MagicMock で DOM 操作を模擬  
- input / confirm / unexpected の分岐を網羅

### 🔹 runner（複数行処理）のテスト  
- SQLite in-memory を利用  
- Run / RunDetail の行数が正しく登録されることを検証

### 🔹 CSV ローダーのテスト  
- カラム不備、型の不正などのチェック

### 🔹 ログ管理のテスト  
- save_log / save_detail の動作確認

---

# 💡 設計ポイント（こだわったところ）

- Selenium の wait をラップして扱いやすくした  
- エラーステージ（input / confirm / unexpected）の分類  
- DBアクセスを log_manager に集約し保守性向上  
- テストしやすい構造を意識  
- メモリDBを使い高速にテストできる仕組みを構築  

---

# 👤 作者について

- 開発経験：VB.NET 実務 2年8ヶ月（2025/12 現在）  
- Python、VBA での自動化ツール作成を経験  
- Selenium × Streamlit × SQLAlchemy の開発が得意  
- テストコード（pytest）を用いた品質改善が強み  
- 副業で自動化ツール開発を希望

---

# 📩 お問い合わせ

- GitHub: https://github.com/SakumaTakayuki  
- ご質問・開発相談などお気軽にどうぞ！

---

ご覧いただきありがとうございます。  
今後も作品を追加していきます！
