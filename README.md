# 戴廷翰醫師｜官網設計提案

單頁靜態網站，預設深色，可切換米白淺色並記住偏好。使用 Andrew 提供的醫師形象照，首頁以醫師姓名為主標題，包含醫師背景、四項診療專長、三項精選研究、兩則公開衛教報導及兩間院所入口。

**目前為設計草稿，尚未作為正式醫師官網公開發布。**

## 預覽

直接用瀏覽器開啟 `index.html`，或在此目錄執行 `python3 -m http.server 8000` 後開啟 `http://localhost:8000`。無須 npm、建置或 API key。Google Fonts 需要網路；離線時使用系統字型。

## GitHub Pages

已附 `.github/workflows/pages.yml`，只在手動啟動時部署，不會因一般 push 自動發布。發布前先在 repository 的 Settings → Pages 選擇 GitHub Actions，確認網站內容與公開範圍，再執行 `Deploy website to GitHub Pages`。

Workflow 僅發布 `index.html`、`assets/` 與 `.nojekyll`，不發布 README 或內部來源筆記。設定依 [GitHub 官方文件](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)。目前 GitHub Pages workflow 尚未執行，因此不宣稱已完成線上部署驗證。

正式公開前須完成醫師本人核稿、最新執業與診次核對，以及院所對刊登內容的確認。確認正式發布後，再更新頁尾草稿標記與 `noindex` metadata。`noindex` 不是存取控制；草稿目前依靠私人 repository 與本機預覽保留非公開狀態。

## 編輯

- `index.html`：所有內容、設計 token、響應式 CSS 與少量互動 JS。
- `assets/ting-han-tai-portrait.png`：Andrew 本次提供並指定使用的醫師照片，保持原圖未修改。
- `assets/hand-sculpture.png`：第一版原創雕塑意象，保留歷史素材，現行首頁不載入。
- `assets/favicon.svg`：原創 T. 字母識別。
- `CONTENT-SOURCES.md`：內容來源、編輯界線與圖像 prompt。

未放未確認的醫師個人班表、萬芳現職聲明、病患影像、成功率、病歷表單或療效保證。網站只連往院所正式入口，不代收掛號或個資。
