# canto-0243-lyricist

粵語填詞 Skill — 精確 0243 聲碼、書面語、可稽核輸出。

專門為香港 0243 聲碼系統而設的 AI 填詞工具。
給任何支援 Skills 的 AI（Claude、Grok 等）用的填詞人角色，專注旋律對位、精確字數、繁體書面語、語義同原創性。

**完全開源（MIT）**，歡迎 fork、改、提 PR 幫我改善呢個 Skill。

## 點用

1. 將成個 folder 放到你的 skills 目錄，或者直接貼 `SKILL.md` 入對話。
2. 提供聲碼（0243 / 02493 / 394052）、字數、題材、韻腳（可選）、長音位置等。
3. AI 會按流程鎖輸入、生成候選、逐字驗碼、交正文 + 逐字對照 + 驗收結果。

詳細輸入格式見 `templates/request.md`。

## 感謝同來源

呢個 Skill 只係為香港 0243 系統而做，唔涉及其他聲碼系統。

- 0243 聲碼理論由黃志華提出，參考站 [0243.hk](https://www.0243.hk/)
- 詞庫查詢依賴 [Canto-0243](https://github.com/bill-iu/Canto-0243)（bill-iu）
- 創作過程中多謝 Manus 同其他幫手
- 原創指令同輔助腳本由 newgod2727 / newgodev 整理開源

## 同 Canto-0243 的關係（重要）

呢個 repo **唔包含** `lyrics.db` 詞庫。

用戶要自己合法取得 Canto-0243 的 `lyrics.db`，並遵守其 CC BY-NC-SA 4.0 + 附加條款。
本 Skill 的 `scripts/` 只係唯讀適配器，唔會分發或改動上游詞庫，唔會影響其他人的權利。

## 結構

- `SKILL.md` — 完整角色同工作流程
- `scripts/` — `lookup.py`（查詞）、`audit.py`（驗碼）、`test_audit.py`
- `templates/` — 輸入模板、例子（包括《A Million Dreams》145 字保義示範）

## 授權

MIT License。
Copyright (c) 2026 newgod2727

完全開源，歡迎 fork 同貢獻改善。
用、改、分發都得。記住詞庫部分要遵守 Canto-0243 的條款，唔影響上游。
