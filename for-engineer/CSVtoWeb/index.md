# 🚀 CSV → Web登録 自動化ツール
**（Python / Streamlit / Selenium / SQLAlchemy）**

CSV データを基にブラウザ操作を完全自動化し、
Web フォームへ入力 → 送信 → 結果ログ保存まで行うツールです。

- Streamlit によるシンプルな UI
- Selenium によるブラウザ自動操作
- SQLite / SQLAlchemy によるログ管理
- pytest による単体テスト
- メモリDBを活用したテストも実装

実務レベルの品質を目指して作成しました。

---

## 🎥 デモ動画
<video width="100%" controls>
  <source src="./docs/CSVtoWeb.mp4" type="video/mp4">
</video>

---

# ✨ 主な機能
- Streamlit UI で CSV アップロード
- Selenium によるブラウザ自動入力
- ステージ別エラー判定（input / submit / confirm / unexpected）
- SQLite + SQLAlchemy によるログ保存
- pytest（MagicMock / monkeypatch / メモリDB）によるテスト完備

---

# 🛠 技術スタック
| 分類 | 技術 |<br>
|------|------|<br>
| 言語 | Python |<br>
| UI | Streamlit |<br>
| 自動操作 | Selenium WebDriver |<br>
| ORM | SQLAlchemy |<br>
| DB | SQLite |<br>
| CSV解析 | pandas |<br>
| テスト | pytest（MagicMock / monkeypatch / in-memory DB） |

---

# 📁 ソースコード
https://github.com/SakumaTakayuki/CSVtoWEB

---

# 💡 設計ポイント（こだわったところ）
- wait 関数のラップで Selenium の安定化
- エラーステージで精密なログ管理
- log_manager による DB アクセス統一
- テスト容易性を意識した構成
- メモリDBを使った高速テスト


---

## 📫 お問い合わせ

お仕事のご相談はお気軽にどうぞ。

👉 [お問い合わせはこちら](../../contact/index.md)

GitHub: https://github.com/SakumaTakayuki  
X: https://x.com/sakuma_takayuki