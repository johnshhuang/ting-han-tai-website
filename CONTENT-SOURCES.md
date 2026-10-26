# 內容與素材紀錄

版本：2026-10-26，網站第一版設計提案。

## 內容依據

Andrew 提供的《戴廷翰醫師_骨科手外科_官網資料整合_20261026.md》為主要內容底稿，當日並查核下列公開頁面：

- [Andrew 個人官網](https://andrewshhuang.com/)：只參考暖黑、銅色、襯線字與層級節奏；未修改或搬用原網站程式與照片。
- [北醫大個人頁](https://hub.tmu.edu.tw/zh/persons/ting-han-tai/)：學歷、訓練與研究入口。博士班以進修呈現，不寫博士學位。
- [豐榮醫院骨科](https://frhosp.rghealth.com.tw/醫療團隊/骨科/)：公開專長與院所資訊；不轉載院方肖像。
- [合杏骨科診所](https://www.hcbone.com.tw/)：地址、電話與官方入口。
- 三篇研究連至 PubMed：PMID [39299603](https://pubmed.ncbi.nlm.nih.gov/39299603/)、[37959267](https://pubmed.ncbi.nlm.nih.gov/37959267/)、[37099343](https://pubmed.ncbi.nlm.nih.gov/37099343/)。書目與類型沿用來源包，未將病例影像當成原創試驗。
- [健康醫療網報導](https://www.healthnews.com.tw/article/69513)、[經濟日報報導](https://money.udn.com/money/story/11800/9644062)：只作簡短原創摘要與超連結；未轉載原文、照片或病患資料。

首屏標語、英文短句與段落標題屬設計文案，不是醫師本人引言。姓名裝飾是排版文字，不是醫師親筆簽名。實際可提供的處置、執業院所與所有正式內容仍須醫師本人核稿。網站是視覺提案，不作醫療廣告合規結論。

## 原創視覺

- 檔案：`assets/hand-sculpture.png`。
- 工具：內建 `image_gen.imagegen`，未使用 CLI fallback、第三方圖片或本機模型。
- 類型：`stylized-concept`；非教學解剖圖、非病患影像。
- `assets/favicon.svg` 與線條裝飾由本次網站原創程式產生。

生成使用的完整 prompt：

> Use case: stylized-concept. Asset type: premium orthopedic and hand surgeon website hero artwork, portrait ratio 4:5. Create an exquisite photorealistic studio photograph of a single sculptural ivory plaster human right hand and lower forearm. Five anatomically plausible fingers visible, relaxed and elegantly reaching upward, palm angled gently toward camera, thumb separated naturally. It is clearly a gallery sculpture, not a patient, not a clinical illustration, not a diagram. Close up but entire hand and fingers inside frame, forearm enters from bottom. Off-white matte porcelain/plaster with fine tactile grain, subtle sculpted palm creases and natural proportions. Single warm copper rim light and soft ivory key light from upper left. Seamless extremely dark warm charcoal-brown background (#0e0d0a), no scene, no plinth, with generous quiet margin around the hand; hand fills 70 percent of image height centered slightly right. Restrained sophisticated editorial art direction, sculptural soft shadows, refined medical brand, photographic 85mm lens, realistic material, high detail. No rings, no jewelry, no bandages, no skeleton, no text, no logos, no graphic elements, no extra hands.
