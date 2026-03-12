
請建立一個 personal branding web app，作為我的 digital business card。
頁面只包含三個區塊：
- About：照片、姓名、職稱、Email、一句簡短介紹
- Expertise：用標籤呈現專長，例如 Data、AI、Training、Speaking、Community
- Contact：顯示  Instagram、LinkedIn、GitHub 按鈕，並在下方放 Email 輸入欄位和 Send 按鈕
設計請保持簡潔、專業、現代、乾淨，適合求職與對外分享。
並參考這個 layout

====================

我想要有一個後端資料庫，可以讓使用者填寫聯絡我資訊後存起來，讓我之後可以再來慢慢處理，並與我的筆記整合，我已經做好前端介面了
 
你推薦那些方案，請詳細進行比較然後一一列出優缺點，最後提供你的建議以及你為什麼推薦這個方案
 
需要穩定、方便查看、最好免費
 
也要有介面可以直接查看，不需要額外再撰寫或製作，且方便我有機會可以跟我在 NOTION 上作的筆記來整合
 
 
 
===================
 
 
那我決定要使用 Notion Database，請詳細分析我現在的專案，幫我規劃實作方案，請以現有的欄位為基礎
 
純前端方案就好，這是一個 DEMO專案，主要確保展示能正確執行就好
 
堅持：
 
- 純前端
- 不做自己的後端
- 資料真的要進 Notion Database
- 因為 DEMO，所以  secret token 還是放在前端，DEMO結束後我會立即刪除
 
因為純前端呼叫 NOTION API 會遇到 CORS 問題，所以我們需要使用 CORS Proxy 服務來解決這個問題。使用 corsproxy.io 這個免費的 CORS Proxy 服務
 
 
 
資料庫設計如下:
 
## Notion Database 架構
 
| 欄位名稱 | Notion 屬性類型 | 說明 | 由誰填寫 |
|----------|----------------|------|----------|
| **Name** | Title（標題，預設欄位） | 訪客的 email，作為每筆記錄的識別 | 自動（前端） |
| **Email** | Email | 訪客的 email 地址 | 自動（前端） |
| **Submitted At** | Date | 表單提交時間 | 自動（前端） |
| **Source** | Text（文字） | 來源標記，固定值 `digital-business-car-demo` | 自動（前端） |
| **Status** | Select | 處理進度 | 自動設為 `New`，之後你手動更新 |
| **Notes** | Text（文字） | 你的筆記欄位，事後手動填寫 | 你手動 |
 
### Status 的 Select 選項
 
請建立以下選項：
 
| 選項名稱 | 建議顏色 | 用途 |
|----------|----------|------|
| `New` | 🔵 Blue | 新進、尚未處理 |
| `In Progress` | 🟡 Yellow | 處理中 |
| `Done` | 🟢 Green | 已完成 |
 
研究完成後，給我一個完整的實作計畫，不需要任何除了完整計畫以外的內容，讓我可以直接複製貼上
 
.env 使用
VITE_NOTION_TOKEN=
VITE_NOTION_DATABASE_ID=
 
重要: 不需要任何除了完整計畫以外的內容，也不要產生程式碼


=======================

