# 📈 紅k決策王 (RedK Strategy)

> 專為台股「昨日漲停收紅K」量身打造的盤中快速決策與風險評估工具。

[![Cloudflare Pages](https://img.shields.io/badge/Hosted%20on-Cloudflare%20Pages-orange?style=flat-square&logo=cloudflare)](https://redk-strategy.pages.dev/)
[![Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)]()
[![Responsive](https://img.shields.io/badge/Layout-Responsive%20(Mobile%20%26%20PC)-blue?style=flat-square)]()

---

## 🌐 線上預覽
立即使用：👉 **[https://redk-strategy.pages.dev/](https://redk-strategy.pages.dev/)**

---

## 🎯 專案特色

*   **極速盤中決策**：針對「昨日漲停」的強勢股，開盤瞬間透過開盤價與昨收價計算溢價率，迅速判斷今日強弱與應對策略。
*   **響應式雙佈局 (Responsive Design)**：
    *   📱 **手機版**：單欄直式直覺設計，大拇指單手操作極致順暢。
    *   💻 **電腦版**：自動展開為左右雙欄操盤儀表板（左側輸入與速查、右側動態建議與歷史紀錄），大螢幕看盤視野更開闊。
*   **智慧動態高亮邏輯**：系統會自動根據您輸入的開盤價，即時點亮對應的情境建議區塊（強勢續抱、高檔減碼、主力不振或急挫逃命）。
*   **台股漲跌幅一鍵帶入**：支援一鍵帶入漲停 (+10%)、強勢 (+5%)、平盤 (0%)、跌停 (-10%) 價格，省去手動計算時間。
*   **貼心記憶與離線友善**：
    *   自動記憶您上一次輸入的開盤價與昨收價。
    *   支援歷史查詢紀錄儲存功能（最多保留 10 筆）。
    *   完全離線相容（內嵌 SVG 圖示，不依賴外部大型資源）。
*   **貼心佈景切換**：
    *   支援 **深色模式 (Dark Mode)** / **淺色模式** 切換。
    *   支援 **台股紅漲綠跌** 與 **國際綠漲紅跌** 格式自由切換。

---

## 💡 核心操作邏輯

1.  **開盤價 $\ge$ 強勢線 (+5%)**
    *   *判定*：盤中不跌破防守線則大概率續漲。
    *   *建議*：建議留倉。
2.  **開盤價介於 3% ~ 5% 之間**
    *   *判定*：趨勢健康，但若衝高突破滿足點 (+7%) 後急速拉回。
    *   *建議*：建議先減半倉位，落袋為安。
3.  **開盤價介於 0% ~ 2% 之間**
    *   *判定*：主力作多意願不足。
    *   *建議*：開盤半小時內若無法放量上攻，果斷清倉離場。
4.  **開盤價出現負數（低於昨收價）**
    *   *判定*：開盤即弱勢。
    *   *建議*：別猶豫，開盤就跑！

---

## 🛠️ 技術架構
*   **Frontend**: 純前端架構 (HTML5, Tailwind CSS, Vanilla JavaScript)
*   **Hosting**: Cloudflare Pages (全自動 Git 整合持續部署)
*   **Storage**: Browser LocalStorage (離線狀態與歷史紀錄保存)

---

## 📄 免責聲明
本工具主要用於計算開盤溢價率，使用場景前提條件是昨日收盤漲停。其操作建議僅供參考，不代表投資保證，投資有賺有賠，請務必自行評估風險！