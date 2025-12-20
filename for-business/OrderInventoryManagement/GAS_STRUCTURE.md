# 🧩 Google Apps Script 構成（ダミー）

本プロジェクトでは、Google Apps Script（GAS）を  
**トリガー / UI / 業務ロジック** に分離した構成としています。

※ 実装詳細は業務ロジックを含むため非公開としています。  
※ 以下は構成理解のためのダミーコードです。

---

## 📂 ファイル構成
/gas  
├─ main.gs // トリガー・処理の入口  
├─ menu.gs // 管理者向けUI  
└─ service.gs // 業務ロジック（ダミー）  

---

## main.gs（トリガー・入口）
役割  
- イベント・トリガーを受け取る
- 業務ロジックは service 層に委譲

```javascript
/**
 * フォーム送信時トリガー（ダミー）
 */
function onFormSubmit(e) {
  // 注文受付処理
  handleOrderReceived(e);
}

/**
 * 定時実行トリガー（ダミー）
 */
function runScheduledTasks() {
  // 在庫整理・ステータス更新
  executeStockAdjustment();
}
```

## menu.gs（管理者向けUI）
役割  
- 管理者操作の導線を提供
- 非エンジニアでも操作可能なUI設計

```javascript
/**
 * スプレッドシート起動時にカスタムメニューを追加
 */
function onOpen() {
  SpreadsheetApp.getUi()
    .createMenu("注文管理")
    .addItem("在庫整理を実行", "executeStockAdjustmentFromMenu")
    .addItem("発送メール送信", "sendShippingMailsFromMenu")
    .addToUi();
}

/**
 * 在庫整理（手動実行）
 */
function executeStockAdjustmentFromMenu() {
  executeStockAdjustment();
}

/**
 * 発送メール送信（手動）
 */
function sendShippingMailsFromMenu() {
  sendShippingMails();
}
```

## service.gs（業務ロジック・ダミー）
役割  
- 業務ルールを service 層に集約
- 実装は非公開（構成・責務のみ公開）

```javascript
/**
 * 注文受付処理（ダミー）
 */
function handleOrderReceived(e) {
  // ・在庫確認
  // ・注文管理シートへの登録
  // ・在庫引当
}

/**
 * 在庫整理処理（ダミー）
 */
function executeStockAdjustment() {
  // ・キャンセル注文の引当解除
  // ・受注完了注文の出庫確定
  // ・在庫整合性の維持
}

/**
 * 発送メール送信処理（ダミー）
 */
function sendShippingMails() {
  // ・発送済ステータスの注文を対象
  // ・未送信分のみ送信
  // ・送信済フラグ更新
}
```