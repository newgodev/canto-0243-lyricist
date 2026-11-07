# canto-0243-lyricist

Precise Cantonese lyric writing skill for AI agents (Claude, Grok, Manus, etc.).

This skill helps create and revise Traditional Chinese written-language Cantonese lyrics with exact 0243 tone code matching, precise character counts, auditable output, and strong original/semantic constraints.

It is designed specifically for the **Hong Kong 0243** system.

## Why this exists

粵語填詞最難嘅係聲調同旋律對位。0243 系統用簡單數字碼（0最低 → 2 → 4 → 3最高）幫填詞人快速找合碼字詞。呢個 Skill 將成套工作流程（鎖輸入、查詞、逐字驗碼、保義修訂、書面語、押韻）變成可重用嘅 AI 指令，令模型唔再靠直覺「啲音」，而係有可稽核嘅結果。

## Fully open source — forks & improvements welcome

This project is released under the **MIT License**.  
You are free to use, copy, modify, merge, publish, distribute, and sell it.  
**Forks and Pull Requests are strongly encouraged** — help improve the skill, add better examples, fix edge cases, or support more modes.

## How to use

### As an Agent Skill (recommended)
1. Clone or download this repo.
2. Place `SKILL.md` where your agent looks for skills (e.g. Claude skills folder, or Manus skills).
3. Provide the input contract (mode, character count, target codes, theme, etc.). See `templates/request.md`.

### In any chat model
Copy the content of `SKILL.md` into the system prompt / conversation and give the input contract.

## Structure
- `SKILL.md` — Main skill instructions
- `scripts/` — Helper scripts (`lookup.py`, `audit.py`) for use with a locally obtained Canto-0243 database
- `templates/` — Request template and worked examples

## Important: Word database is NOT included

The lookup scripts are thin adapters. They require a separately and lawfully obtained `lyrics.db` from:

**[Canto-0243 by bill-iu](https://github.com/bill-iu/Canto-0243)**

Canto-0243 is licensed under **CC BY-NC-SA 4.0 + additional terms**.  
You must obtain it yourself and comply with its license (no repackaging as a competing product, no paid API/service without permission, share-alike, attribution, etc.).  
This skill does **not** redistribute any wordlist or database.

## Credits & thanks

- **0243 system**: Created by 黃志華 (Wong Chi-wah). Site: [0243.hk](https://www.0243.hk)
- **Canto-0243 offline dictionary & tools**: [bill-iu/Canto-0243](https://github.com/bill-iu/Canto-0243)
- **Manus** and other AI agents that helped develop and refine this skill
- All contributors who improve this via forks and PRs

This skill is original instructions + thin adapters. It does not claim ownership of the 0243 theory or the Canto-0243 wordlist.

## License

MIT License — see [LICENSE](LICENSE).

Copyright (c) 2026 newgod2727

---

**For Hong Kong 0243. Open source so the community can keep improving it.**
