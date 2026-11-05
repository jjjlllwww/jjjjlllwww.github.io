# jjjlllwww.github.io

一个可被 AI 编码代理直接调用的品牌设计系统库：84 套真实网站提炼的 `DESIGN.md`。

A brand design-system library that AI coding agents can load directly — 84 `DESIGN.md` specs distilled from real websites.

---

## 目录结构 · Repository layout

```
.
├── index.html              # 站点根入口：跳转到设计系统库
├── awesome-design-md/      # 设计系统库：84 套品牌 DESIGN.md + 检索页
│   ├── index.html          # 分类索引页（色块墙 / 搜索 / 筛选）
│   ├── SKILL.md            # 技能入口：使用流程 + 84 套索引表
│   ├── README.md           # 技能包说明（安装、覆盖清单、许可）
│   ├── design-md/          # 84 个品牌目录，各含 DESIGN.md
│   ├── LICENSE             # 上游 MIT 许可
│   └── UPSTREAM-README.md  # 上游原始说明（存档）
└── .gitignore              # 本地自检与构建产物
```

`_shots/`、`_systems.json` 属于本地生成的中间产物，已被 `.gitignore` 排除，不进版本库。

`_shots/` and `_systems.json` are local build/QA artifacts and are gitignored.

## 站点入口 · Entry points

| 路径 Path | 内容 What it is |
|---|---|
| `/` | 跳转页，3 秒后进入设计系统库 Redirect to the library |
| `/awesome-design-md/` | 设计系统库索引页 Design-system library index |

根入口只做跳转，不留内容页；作品集页面不在此仓库维护。

The root page is a redirect only; there is no portfolio page in this repository.

GitHub Pages 的发布源为 `main` 分支根目录；根目录的 `.nojekyll` 让 84 份带 YAML frontmatter 的 markdown 按原始文本提供，不参与 Jekyll 渲染。

GitHub Pages publishes from the repository root of `main`. The root-level `.nojekyll` keeps the 84 YAML-frontmatter markdown files raw instead of routing them through Jekyll.

## 设计系统库是什么 · What the library is

每套是一个 `DESIGN.md`：Google Stitch 格式的纯文本设计规范，写明色彩 token、字体层级、组件状态、间距栅格、阴影层级、响应式断点与正误示例。把它交给 AI 代理，生成的界面会贴近该品牌的视觉语言，而不是套一个通用模板。

Each entry is a `DESIGN.md` — a plain-text design spec in Google Stitch format covering colour tokens, type scale, component states, spacing grid, elevation, breakpoints and do/don't guardrails. Hand it to an AI agent and the generated UI follows that brand's visual language instead of a generic template.

### 两种用法 · Two ways to use it

**作为技能安装（推荐）** — 把整个 `awesome-design-md/` 放进代理的技能目录：

```text
<workspace>/.user_skills/awesome-design-md/
```

之后说「做个像 Linear 那样的界面」，代理会按 `SKILL.md` 的索引命中并读取对应 `DESIGN.md`。

**手动引用** — 把某个品牌的 `DESIGN.md` 复制到项目根目录，告诉代理按它执行。

**Install as a skill (recommended):** drop the whole `awesome-design-md/` folder into your agent's skill directory. **Manual reference:** copy one brand's `DESIGN.md` into your project root.

### 覆盖清单 · Coverage

| 分类 Category | 数量 | 代表 Brands |
|---|---|---|
| AI 与大模型 | 13 | Claude, Cohere, ElevenLabs, Runway, xAI |
| 开发者工具 | 7 | Cursor, Vercel, Raycast, Warp |
| 后端与运维 | 9 | Supabase, Sentry, PostHog, Sanity |
| 效率与 SaaS | 9 | Linear, Notion, Zapier, Slack |
| 设计与创意工具 | 6 | Figma, Framer, Airtable, Webflow |
| 金融与加密 | 9 | Stripe, Coinbase, Revolut, Mastercard |
| 电商与零售 | 6 | Nike, Shopify, Airbnb, Starbucks |
| 媒体与消费电子 | 16 | Apple, Spotify, NVIDIA, PlayStation |
| 汽车 | 7 | Tesla, BMW, Ferrari, Bugatti |
| 复古网页 | 2 | Dell (1996), Nintendo (2001) |

合计 84 套。完整索引（ranked 顺序与每套的一句话视觉特征）见 `awesome-design-md/SKILL.md`。

## 本地预览 · Preview locally

```bash
python -m http.server 8000
```

然后访问 `http://localhost:8000/awesome-design-md/`。直接双击该目录下的 `index.html` 也能看到卡片墙，但搜索与筛选需要 DOM 运行环境，建议走本地服务器。

Visit `http://localhost:8000/awesome-design-md/`. Opening `index.html` with `file://` renders the wall, but search and filters are easiest to verify through a local server.

## 许可与致谢 · License & credits

- 站点代码：本仓库自有内容（跳转入口与检索页），未单独声明许可，转载前请先联系作者。
- 设计系统库：上游为 [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md)，MIT License，**保留原始 `LICENSE` 与归属**；打包环节只增加了技能入口、索引、检索页与校验，未改动任何 `DESIGN.md` 内容。
- `DESIGN.md` 中的 token 取自公开网站可见的 CSS 值。这些文件描述的是设计语言的规律，**不构成对任何品牌的授权**：用于内部原型、练习与风格研究是合适的；对外商用且需要品牌露出时，请自行确认商标与视觉资产的使用权限。

The design-system library comes from VoltAgent/awesome-design-md under the MIT License, with the original `LICENSE` and attribution preserved. Only a skill entry point, an index, a browsable page and verification were added — no `DESIGN.md` content was altered. These documents describe the *rules* of a design language and grant no brand authorisation.
