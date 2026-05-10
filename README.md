# CISC 2026 論文專案（XeLaTeX）

本儲存庫為投稿 **全國資訊安全會議（CISC）** 格式之 **XeLaTeX** 論文原始碼，主題為邊緣原生、加密威脅流量之 **安全事件訊號（security event signal）** 管線。

**論文標題：** *From Encrypted Flows to Security Event Signals: An Edge-Native Pipeline for Threat-Aware Traffic Analysis*

**單位：** 輔仁大學人工智慧與資訊安全學士學位學程（Fu Jen Catholic University）；Ching-Hao Mao 另列 International Cybersecurity Talent Development and Promotion Association（見 `main.tex` 作者區塊）。

---

## 專案結構

```
.
├── main.tex              # 主檔（CISC 雙欄版型、摘要／關鍵字中文標籤）
├── main.pdf              # 建置產出（可選擇是否納入版控）
├── reference.bib         # BibTeX 參考文獻
├── sections/             # 各節內容（\input 載入）
│   ├── 00_abstract.tex
│   ├── 01_introduction.tex
│   ├── 02_related_work.tex
│   ├── 03_system_design.tex
│   ├── 04_methodology.tex
│   ├── 05_experiments.tex
│   └── 08_conclusion.tex
├── tables/               # 表格片段
└── figures/              # 圖檔（如 system_overview.pdf）
```

---

## 編譯環境

- **建議：** [TeX Live](https://tug.org/texlive/)（含 **XeLaTeX**）、**BibTeX**
- **替代：** [Tectonic](https://tectonic-typesetting.github.io/)（單一指令可連帶處理 `.bib`）

### XeLaTeX + BibTeX（典型流程）

於專案根目錄執行：

```bash
xelatex main
bibtex main
xelatex main
xelatex main
```

### Tectonic

```bash
tectonic main.tex
```

---

## 中文字型（CISC 模板）

`main.tex` 內優先使用專案根目錄下的 **`kaiu.ttf`**（標楷體）；若不存在，則 fallback 為 **Kaiti SC**（常見於 macOS）。

投稿前請依主辦單位說明，將字型檔放置於與 `main.tex` 相同目錄，或改為指定之系統字型。

---

## 主要論點（概要）

- 在 **HTTPS/TLS** 環境下，將 **加密流量推論** 轉為 **結構化、門檻一致（threshold-consistent）** 的安全事件訊號，供下游關聯與分析使用。
- **兩階段** 設計：Stage 1 良性／惡意篩選與派發；Stage 2 威脅行為語意標籤。
- **實驗驗證** 著重事件訊號層與重播（replay）一致性；完整威脅推理、開集偵測、時序融合等列為後續工作。

---

## 遠端儲存庫

- GitHub：<https://github.com/ericmao/cisc2026B.git>

---

## 授權與聲明

論文內容、數據與圖表之著作權與投稿規範，請依 **CISC 2026 主辦單位** 與作者約定為準。本 README 僅說明專案之技術用途與建置方式。
