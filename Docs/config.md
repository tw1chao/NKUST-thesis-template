## NKUST Thesis LaTeX 設定

此版型分為文件格式與使用者資訊二大部分，文件格式皆存放於**Configurations/**中，
使用者資訊皆定義於**config.tex**中。

文件格式用於 PDF 格式樣式以及系統中的套件引入等，其主要設定存放於**Configurations**中，包含了文章中引入的章節、附錄以及版型的設定，而版型設定中的格式等套件設定皆存放於**Templates**中，
當前套件包提供了中英文摘要、誌謝、章節、參考文獻及文件邊界等定義功能。

### 設定作者資訊

作者資訊為本論文中的作者、指導教授、學校、科系、論文題目等相關資料，其設定欄位位於 `config.tex` 中。
在板型設定中，比較特殊的部份是國立高雄科技大學於2018年2月1日由國立高雄應用科技大學、國立高雄第一科技大學、國立高雄海洋大學三所科技大學合併而成，在規範提供之書名頁範本加註合併之學校英文名稱，因此本論文中提供此設定。

### 文件內容設定

為了提供使用者在特定的狀況下調整PDF輸出文件的內容，在 `config.tex` 中提供內容是否載入的設定，其設定為 `true` 表示為載入，設定為 `false` 表示為文建會忽略此一內容。

### 文件版型調整

除論文封面、書名頁的版型位於 `Instances` 中，其餘的位於 `Templates` 中，在 `Templates` 的檔案都是 `.sty` 格式。
文件版面調整僅需對排版的格式進行修改即可大成版型調整的功能。

### 字體調整

此版型中之中文字體使用教育部發布之楷體、宋體、隸書等中文字型以及 "TeX Gyre Termes"、"DejaVu Sans Mono"、"EB Garamond" 等英文字體。如果您想使用其他系統中已有的字體請於 template.tex 中修改字體設定。

請注意，如果您使用了系統不存在的字體，在編譯過程中會因缺乏字體而導致編譯錯誤，因此我們建議您先透過指令查詢系統中是否存在字體。

```
$ fc-list | grep <font-name>
```

上述指令請自行更換為要查詢的字體名稱，如您需要安裝字體可請系統管理員為您提供協助或是自行將字體安裝於家目錄中的 `~/.local/share/fonts/` 位置中。

自行安裝字體指令流程首先為取得字體，後將字體安裝至特定的位置中。

### 邊界調整

由於精裝本書背的位置為紙張的左邊，使用置中排版會造成一部分的文字較偏書背，因此論文檔案的**內容**將會向左偏移，論文檔案的內容包含封面、書名頁、摘要、目錄、誌謝、論文內容、參考文獻等。

> 當您輸出文件時都是膠裝本的狀況下，請忽略邊界調整章節中的後續內容。

當使用膠裝時，輸出封面時若使用上述之**內容**時，會導致封面輸出時偏離封面中心的問題，此問題可以透過額外的指令產生無偏移之封面，該指令請見編譯篇。
