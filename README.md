# 戴廷翰醫師｜官網設計提案

單頁靜態網站，預設深色，可切換米白淺色並記住偏好。使用 Andrew 提供的醫師形象照，首頁以醫師姓名為主標題，包含醫師背景、四項診療專長、八篇學術發表、六個新聞／活動來源連結，以及兩間院所的簡介與官方預約入口。

**目前為設計提案，GitHub Pages 已有可瀏覽版本，內容仍待醫師核稿。**

2026-10-26 最新版已發布 GitHub Pages：包含六則新聞稿、六張原創配圖、八篇學術發表與兩間院所資訊。45 項瀏覽器檢查通過；線上首頁、醫師照片、六張配圖與 favicon 共 9 個檔案，HTTP 200 且 SHA-256 與本機相同。

公開網址：https://johnshhuang.github.io/ting-han-tai-website/

本次網站部署 commit：`0bb8e0ee231ef0b8edabcbcf76917967c234eefc`；[GitHub Actions 成功紀錄](https://github.com/johnshhuang/ting-han-tai-website/actions/runs/40341917220)。

## 預覽

直接用瀏覽器開啟 `index.html`，或在此目錄執行 `python3 -m http.server 8000` 後開啟 `http://localhost:8000`。無須 npm、建置或 API key。Google Fonts 需要網路；離線時使用系統字型。

## GitHub Pages

已附 `.github/workflows/pages.yml`，只在手動啟動時部署，不會因一般 push 自動發布。發布前先在 repository 的 Settings → Pages 選擇 GitHub Actions，確認網站內容與公開範圍，再執行 `Deploy website to GitHub Pages`。

Workflow 僅發布 `index.html`、`assets/` 與 `.nojekyll`，不發布 README 或內部來源筆記。設定依 [GitHub 官方文件](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)。本次 GitHub Actions run `40341917220` 已成功；最新網站與配圖已完成線上 HTTP／雜湊驗證，詳見 VERIFICATION.md 與 verification.json。

作為正式官網採用前仍需醫師本人核稿、最新執業與診次核對。現有網站保留頁尾設計提案標記及 `noindex` metadata；`noindex` 不是存取控制，repository 與 Pages 現在皆為公開。

## 編輯

- `index.html`：所有內容、設計 token、響應式 CSS 與少量互動 JS。
- `assets/ting-han-tai-portrait.png`：Andrew 本次提供並指定使用的醫師照片，保持原圖未修改。
- `assets/hand-sculpture.png`：第一版原創雕塑意象，保留歷史素材，現行首頁不載入。
- `assets/favicon.svg`：原創 T. 字母識別。
- `assets/news-*.png`：六張內建 imagegen 製作的原創新聞配圖，來源與最終 prompt 見 CONTENT-SOURCES.md。
- `CONTENT-SOURCES.md`：內容來源、編輯界線與圖像 prompt。

未放未確認的醫師個人班表、萬芳現職聲明、病患影像、成功率、病歷表單或療效保證。網站只連往院所正式入口，不代收掛號或個資。

## 本次資料整理重點

- 院所：補兩間院所的簡介、介紹頁與官方預約入口。合杏預約入口已依使用者指定更新為 https://hcbone-booking.hixcare.tw/，確認 HTTP 200 與頁面標題；官網與電話入口保留。
- 新聞稿：六則報導／講座卡片集中呈現，搭配六張原創主題示意圖。第六則已使用使用者補充的完整標題，並以診所公告核對同一中時網址；媒體發布日尚未確認，故不顯示日期。不同分享／追蹤網址不重複計入。
- 論文：五篇回顧研究（其中兩篇明確含 meta-analysis）及三篇 NEJM Images。依原刊標示類型，未宣稱五篇皆為 meta-analysis。
