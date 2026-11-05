# awesome-design-md · 品牌设计系统技能包

84 套从真实网站提炼的 `DESIGN.md`（Google Stitch 格式），可直接喂给 AI 编码代理，生成与目标品牌视觉一致的界面。

A skill pack of 84 `DESIGN.md` design systems extracted from real websites (Google Stitch format), ready to feed any AI coding agent so it generates UI that matches a given brand's visual language.

---

## 这是什么 · What this is

`DESIGN.md` 是一份纯文本设计系统规范：AI 代理读它，就能拿到色彩 token、字体层级、组件状态、间距栅格、阴影层级、响应式断点和正误示例，不用 Figma 导出、不用 JSON schema。

`DESIGN.md` is a plain-text design-system spec. An AI agent reads it and gets colour tokens, type scale, component states, spacing grid, elevation, breakpoints and do/don't guardrails — no Figma export, no JSON schema.

本目录把它打包成一个可直接安装的技能（Skill），而不只是一堆散落的文档。

This directory packages the collection as an installable skill rather than a loose pile of documents.

## 目录结构 · Layout

```
awesome-design-md/
├── SKILL.md              # 技能入口：使用流程 + 84 套索引表（slug / 品牌 / 视觉特征）
├── design-md/            # 84 个品牌目录，各含一份 DESIGN.md
│   ├── claude/DESIGN.md
│   ├── stripe/DESIGN.md
│   ├── linear/DESIGN.md
│   └── ...
├── LICENSE               # 上游 MIT 许可
├── CONTRIBUTING.md       # 上游贡献指南
└── UPSTREAM-README.md    # 上游原始说明（存档）
```

## 使用方式 · How to use

**方式一：作为技能安装（推荐）** —— 把整个 `awesome-design-md/` 目录放到宿主代理的技能目录下，例如：

```text
<workspace>/.user_skills/awesome-design-md/
```

之后说"做个像 Linear 那样的界面"，代理会自动读取对应 `DESIGN.md`。

**方式二：手动引用** —— 把某个品牌的 `DESIGN.md` 复制到你的项目根目录，告诉代理"按 DESIGN.md 的规范做这个页面"。

**Option A — install as a skill (recommended):** drop the whole `awesome-design-md/` folder into your agent's skill directory (e.g. `<workspace>/.user_skills/awesome-design-md/`). The agent then auto-selects a system when you say "build a page that looks like Linear".

**Option B — manual reference:** copy one brand's `DESIGN.md` into your project root and tell the agent to follow it.

## 覆盖品牌 · Coverage

| 分类 Category | 数量 | 代表 Brands |
|---|---|---|
| AI & LLM Platforms | 13 | Claude, Cohere, ElevenLabs, Runway, xAI |
| Developer Tools & IDEs | 7 | Cursor, Vercel, Raycast, Warp |
| Backend, Database & DevOps | 9 | Supabase, Sentry, PostHog, Sanity |
| Productivity & SaaS | 10 | Linear, Notion, Zapier, SAP |
| Design & Creative Tools | 7 | Figma, Framer, Airtable, Webflow |
| Fintech & Crypto | 10 | Stripe, Coinbase, Revolut, Mastercard |
| E-commerce & Retail | 7 | Nike, Shopify, Airbnb, Starbucks |
| Media & Consumer Tech | 16 | Apple, Spotify, NVIDIA, PlayStation |
| Automotive | 8 | Tesla, BMW, Ferrari, Bugatti |
| Retro Web (1990s–2000s) | 2 | Dell (1996), Nintendo (2001) |

完整索引见 `SKILL.md`。 / Full index lives in `SKILL.md`.

## 来源与许可 · Source & License

- 上游仓库 Upstream: <https://github.com/VoltAgent/awesome-design-md>（MIT License，见 `LICENSE`）
- `DESIGN.md` 中的 token 取自公开网站可见的 CSS 值；原仓库与整理者不主张对任何品牌视觉识别的所有权。
- 这些文件描述的是**设计语言的规律**，不构成品牌授权。用于内部原型、练习、风格研究是合适的；对外商用且需要品牌露出时，请自行确认商标与视觉资产的使用权限。

The design tokens are publicly observable CSS values. This collection documents the *rules* of a design language; it grants no brand authorisation. Fine for prototypes, practice and style study — confirm trademark and asset rights yourself before commercial use that surfaces a real brand.

本项目仅做了打包（技能入口、索引、校验），未改动任何 `DESIGN.md` 内容。

This packaging repo only adds a skill entry point, an index and verification — no `DESIGN.md` content was altered.
