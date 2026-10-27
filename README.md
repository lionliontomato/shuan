# 霜霜の歌單 ❣️（原版 fang-fang 排版）

本版依照 https://lionliontomato.github.io/fang-fang/ 的公開 HTML 結構、CSS 類別與 JS 行為重新製作，維持相同的主區塊、搜尋、標籤、歌曲卡、複製按鈕、雙擊歌曲連結、隨機抽歌彈窗及底部版權。

## 上線
1. 解壓 ZIP，把 `index.html`、`style.css`、`script.js`、`butterfly-lavender.png`、`copyright.html`、`.nojekyll` 直接放在 GitHub 儲存庫根目錄。
2. GitHub → Settings → Pages → Deploy from a branch → main / (root)。
3. 請將 Google Sheet 共用設為「知道連結的任何人可以檢視」；公開網站才能讀取。

## 資料欄位
- A：歌名；B：歌手；C：分類；D：歌曲網址；F：網站分類按鈕來源。
- H：設定名稱（例如：網站小標題、抽歌視窗標題、關閉按鈕文字）；I：對應設定值。
- H/I 直接在 Google Sheets 編輯，網站重整後讀取。網站名稱刻意固定為「霜霜の歌單」，以符合此次要求。
- 如果資料不是第一個工作表（gid=0），修改 `script.js` 裡的 `SHEET_GID`。

## 注意
本網站是公開靜態頁面，**不包含**讓網站訪客回寫 H/I 至 Google Sheet 的權限；H/I 是透過試算表編輯、由網站讀取。若要直接在網頁編輯，須另設有安全認證的後端。由於此環境無法存取新試算表實際資料，無法驗證其公開權限與欄位內容，請上線後核對。

© 2026 LionLionTomato. All Rights Reserved.


## 2026-10-27 修正
- 計數列置中，標題上方只保留 ♫。
- 版權頁按原網站原生字體及原始條款內容製作，只替換為「霜霜の歌單」。
- 進入及重新整理時不顯示過期歌單；等 Google Sheets 最新讀取完成後才顯示資料。
- 移除先前快取的 UI 初始值、加入每次讀取不同的查詢參數及版本化 JS/CSS。
- 注意：Google 試算表端資料發布與 Google 快取仍可能有延遲，網站無法控制 Google 伺服器的更新速度。若無法取得最新資料，會提示錯誤，不會用舊資料充數。


## 2026-10-27 更新
- 副標題初次載入／重新整理時會保持隱藏，直到成功取得 Google 試算表 H/I 設定才顯示；若讀取失敗不顯示過時文字。
- 版權頁已套用主頁相同的淺紫色蝴蝶背景，保留原本版權頁文字與字體設定。
