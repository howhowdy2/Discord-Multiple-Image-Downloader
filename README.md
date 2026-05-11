# Discord Image Batch Downloader｜Discord 批量圖片下載

A Tampermonkey userscript that adds a **"Download All as ZIP"** button to Discord messages containing multiple images.

在 Discord 網頁版含有多張圖片的訊息下方，自動新增「**下載全部圖片 ZIP**」按鈕。

---

## Features｜功能

- Detects messages with 2 or more image attachments and injects a download button automatically
- Fetches all images and packages them into a single `.zip` file
- Images are named sequentially (`001.png`, `002.png`, …) in the order they appear
- Works with Discord's mosaic (multi-image grid) layout
- No external dependencies — JSZip is bundled inside the script

---

- 自動偵測含有 2 張以上附件圖片的訊息並注入下載按鈕
- 將所有圖片抓取後打包成單一 `.zip` 壓縮檔
- 圖片依顯示順序命名（`001.png`、`002.png`……）
- 支援 Discord 多圖 mosaic 格局
- 無需外部依賴，JSZip 已內嵌於腳本中

---

## Installation｜安裝步驟

**1. Install Tampermonkey｜安裝 Tampermonkey**

Install the Tampermonkey extension for your browser:
安裝對應瀏覽器的 Tampermonkey 擴充套件：

- [Chrome](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)
- [Firefox](https://addons.mozilla.org/firefox/addon/tampermonkey/)
- [Edge](https://microsoftedge.microsoft.com/addons/detail/tampermonkey/iikmkjmpaadaobahmlepeloendndfphd)

**2. Install the script｜安裝腳本**

Download [`discord_scheduler.user.js`](./discord_scheduler.user.js) and drag it into the Tampermonkey dashboard, then click **Install**.

下載 [`discord_scheduler.user.js`](./discord_scheduler.user.js)，拖曳到 Tampermonkey 管理頁面，點擊「**安裝**」。

---

## Usage｜使用方式

1. Open Discord in your browser and navigate to any channel
2. Find a message containing multiple images
3. A blue **「下載全部圖片 ZIP（N 張）」** button will appear below the message automatically
4. Click the button — the script will fetch all images and trigger a `.zip` download

---

1. 用瀏覽器開啟 Discord，進入任意頻道
2. 找到含有多張圖片的訊息
3. 訊息下方會自動出現藍色的「**下載全部圖片 ZIP（N 張）**」按鈕
4. 點擊按鈕，腳本會自動抓取所有圖片並下載 `.zip` 壓縮檔

---

## Notes｜注意事項

- The button only appears for messages with **2 or more** images. Single images can be saved with right-click → Save
- Discord image URLs expire after some time. Download promptly after the message is sent
- If the button shows ❌, open the browser console (F12) for error details

---

- 按鈕只會在含有 **2 張以上**圖片的訊息出現，單張圖片請直接右鍵另存
- Discord 圖片 URL 有時效性，請在訊息傳送後盡快下載
- 若按鈕顯示 ❌，請按 F12 開啟主控台查看錯誤詳情
