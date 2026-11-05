---
name: awesome-design-md
description: 品牌设计系统知识库，收录 84 套真实网站提炼的 DESIGN.md（Stitch 格式规范：色彩 token、字体层级、组件样式、间距栅格、阴影层级、Do/Don't、响应式断点、Agent Prompt）。当用户要求把界面做得像某个品牌/网站（如 Apple、Stripe、Linear、Notion、Vercel、Nike、Spotify、Claude、Figma），或要求指定风格的 UI、网页、落地页、应用界面、设计稿、组件库、配色与排版规范时使用；也用于对标某一品牌视觉体系做风格迁移、设计走查和多品牌风格对比。不处理纯图片生成、品牌 logo 重绘或需要版权的品牌资产复刻。
---

# awesome-design-md

84 套已提炼的品牌设计系统，来源为公开网站的可见 CSS 值。每套一个目录：`design-md/<slug>/DESIGN.md`。

**本目录路径**：本 Skill 目录下的 `design-md/`（素材已在本地，无需联网）。

## 使用流程

1. **定位品牌**：按下文索引表找到目标 `slug`。用户没说品牌、只给风格关键词（例如"暖色编辑感""极简黑白""暗黑霓虹"）时，从索引的「视觉特征」列挑 2–3 个候选并向用户确认。
2. **完整读取**：`Read design-md/<slug>/DESIGN.md` 全文。文件较长（约 500–900 行），先读前 120 行拿到 frontmatter 里的 colors / typography token，再按需读组件、布局、阴影、响应式章节。**禁止只凭本 SKILL.md 里的短描述就开始写代码。**
3. **落地为 CSS 变量**：把 frontmatter 的 `colors:` 逐条映射为 `--color-*` 自定义属性，`typography:` 的每一档映射为 `--font-*`（fontFamily / fontSize / fontWeight / lineHeight / letterSpacing 五项都要带上），再写组件。不要用近似色替代原始 hex。
4. **遵守 Do / Don't**：DESIGN.md 的 "Do's and Don'ts" 与 "Component Stylings" 是硬约束，遇到与本能的审美判断冲突时以文件为准。
5. **产出后自检**：对照文件里的 "Agent Prompt Guide" 最后一节，检查主色是否只用于最高优先级 CTA、标题字重/字号层级是否与规范一致、圆角与阴影是否取自 token。成品必须实际渲染出来看一眼，不能只交代码。

## 索引

### AI & LLM Platforms

| slug | 名称 | 视觉特征 |
|---|---|---|
| `claude` | Claude | Anthropic's AI assistant. Warm terracotta accent, clean editorial layout |
| `cohere` | Cohere | Enterprise AI platform. Vibrant gradients, data-rich dashboard aesthetic |
| `elevenlabs` | ElevenLabs | AI voice platform. Dark cinematic UI, audio-waveform aesthetics |
| `jobright` | Jobright | AI job-hunting platform. Spring-mint green, black pill buttons, condensed Titillium headlines |
| `minimax` | Minimax | AI model provider. Bold dark interface with neon accents |
| `mistral.ai` | Mistral AI | Open-weight LLM provider. French-engineered minimalism, purple-toned |
| `ollama` | Ollama | Run LLMs locally. Terminal-first, monochrome simplicity |
| `opencode.ai` | OpenCode AI | AI coding platform. Developer-centric dark theme |
| `replicate` | Replicate | Run ML models via API. Clean white canvas, code-forward |
| `runwayml` | Runway | AI creative-tools platform with an editorial film-festival aesthetic — cinematic dark heroes, paper-white reading bands, single proprietary sans, and pure black pill CTAs. |
| `together.ai` | Together AI | Open-source AI infrastructure. Technical, blueprint-style design |
| `voltagent` | VoltAgent | AI agent framework. Void-black canvas, emerald accent, terminal-native |
| `x.ai` | xAI | Elon Musk's AI lab. Stark monochrome, futuristic minimalism |

### Developer Tools & IDEs

| slug | 名称 | 视觉特征 |
|---|---|---|
| `cursor` | Cursor | AI-first code editor. Sleek dark interface, gradient accents |
| `expo` | Expo | React Native platform. Dark theme, tight letter-spacing, code-centric |
| `lovable` | Lovable | AI full-stack builder. Playful gradients, friendly dev aesthetic |
| `raycast` | Raycast | Productivity launcher. Sleek dark chrome, vibrant gradient accents |
| `superhuman` | Superhuman | Fast email client. Premium dark UI, keyboard-first, purple glow |
| `vercel` | Vercel | Frontend deployment platform. Black and white precision, Geist font |
| `warp` | Warp | Modern terminal. Dark IDE-like interface, block-based command UI |

### Backend, Database & DevOps

| slug | 名称 | 视觉特征 |
|---|---|---|
| `clickhouse` | ClickHouse | Fast analytics database. Yellow-accented, technical documentation style |
| `composio` | Composio | Tool integration platform. Modern dark with colorful integration icons |
| `hashicorp` | HashiCorp | Infrastructure automation. Enterprise-clean, black and white |
| `mongodb` | MongoDB | Document database. Green leaf branding, developer documentation focus |
| `oracle` | Oracle | Enterprise cloud and database software. Warm neutral ladder, charcoal-only actions, red saved for the wordmark |
| `posthog` | PostHog | Product analytics. Playful hedgehog branding, developer-friendly dark UI |
| `sanity` | Sanity | Headless content platform with a dark-first editorial marketing surface — 112px display type, IBM Plex Mono technical eyebrows, and a single coral-red accent reserved for the highest-priority CTA. |
| `sentry` | Sentry | Error monitoring. Dark dashboard, data-dense, pink-purple accent |
| `supabase` | Supabase | Open-source Firebase alternative. Dark emerald theme, code-first |

### Productivity & SaaS

| slug | 名称 | 视觉特征 |
|---|---|---|
| `cal` | Cal.com | Open-source scheduling. Clean neutral UI, developer-oriented simplicity |
| `intercom` | Intercom | Customer messaging. Friendly blue palette, conversational UI patterns |
| `linear.app` | Linear | Project management for engineers. Ultra-minimal, precise, purple accent |
| `mintlify` | Mintlify | Documentation platform. Clean, green-accented, reading-optimized |
| `notion` | Notion | All-in-one workspace. Warm minimalism, serif headings, soft surfaces |
| `resend` | Resend | Email API for developers. Minimal dark theme, monospace accents |
| `sap` | SAP | Enterprise business software. White canvas, flat blue bands, application-frame chrome |
| `zapier` | Zapier | Automation platform. Warm orange, friendly illustration-driven |

### Design & Creative Tools

| slug | 名称 | 视觉特征 |
|---|---|---|
| `airtable` | Airtable | Spreadsheet-database hybrid. Colorful, friendly, structured data aesthetic |
| `clay` | Clay | Creative agency. Organic shapes, soft gradients, art-directed layout |
| `figma` | Figma | Collaborative design tool. Vibrant multi-color, playful yet professional |
| `framer` | Framer | Website builder. Bold black and blue, motion-first, design-forward |
| `miro` | Miro | Visual collaboration. Bright yellow accent, infinite canvas aesthetic |
| `webflow` | Webflow | Visual web builder. Blue-accented, polished marketing site aesthetic |

### Fintech & Crypto

| slug | 名称 | 视觉特征 |
|---|---|---|
| `binance` | Binance | Crypto exchange. Bold Binance Yellow on monochrome, trading-floor urgency |
| `coinbase` | Coinbase | Crypto exchange. Clean blue identity, trust-focused, institutional feel |
| `kraken` | Kraken | Crypto trading platform. Purple-accented dark UI, data-dense dashboards |
| `mastercard` | Mastercard | Global payments network. Warm cream canvas, orbital pill shapes, editorial warmth |
| `mercury` | Mercury | Startup banking platform. Ink-violet night world, indigo action pill, light custom sans |
| `nerdwallet` | NerdWallet | Personal finance comparison platform. Deep spruce green, mint washes, near-square corners |
| `revolut` | Revolut | Digital banking. Sleek dark interface, gradient cards, fintech precision |
| `stripe` | Stripe | Payment infrastructure. Signature purple gradients, weight-300 elegance |
| `wise` | Wise | International money transfer. Bright green accent, friendly and clear |

### E-commerce & Retail

| slug | 名称 | 视觉特征 |
|---|---|---|
| `airbnb` | Airbnb | Travel marketplace. Warm coral accent, photography-driven, rounded UI |
| `meta` | Meta | Tech retail store. Photography-first, binary light/dark surfaces, Meta Blue CTAs |
| `mydealz` | mydealz | German deals community. Dense white-card feed, hot and cold voting pill, brand green |
| `nike` | Nike | Athletic retail. Monochrome UI, massive uppercase Futura, full-bleed photography |
| `shopify` | Shopify | E-commerce platform. Dark-first cinematic, neon green accent, ultra-light display type |
| `starbucks` | Starbucks | Coffee retail flagship. Four-tier earth-green system, warm cream canvas, proprietary SoDoSans typography |

### Media & Consumer Tech

| slug | 名称 | 视觉特征 |
|---|---|---|
| `1win` | 1win | Crypto casino and sportsbook. Near-black canvas, vivid green action color, dense game-tile rails |
| `aljazeera` | Al Jazeera | Global news network. Flat white paper, dense Roboto headlines, orange signature and live red |
| `apple` | Apple | Consumer electronics. Premium white space, SF Pro, cinematic imagery |
| `dji` | DJI | Drone and camera maker. Studio product tiles, engineering-blue pills, tight Open Sans |
| `hp` | HP | PC and printer maker. Pure white canvas, HP Electric Blue signal CTA, geometric Forma DJR Micro, blue chevron decorations |
| `ibm` | IBM | Enterprise technology. Carbon design system, structured blue palette |
| `nvidia` | NVIDIA | GPU computing. Green-black energy, technical power aesthetic |
| `oura` | Oura | Smart ring wellness brand. Warm paper cream, editorial serif, earth-tone accents |
| `pinterest` | Pinterest | Visual discovery platform. Red accent, masonry grid, image-first |
| `playstation` | PlayStation | Gaming console retail. Three-surface channel layout, cyan hover-scale interaction |
| `spacex` | SpaceX | Space technology. Stark black and white, full-bleed imagery, futuristic |
| `spotify` | Spotify | Music streaming. Vibrant green on dark, bold type, album-art-driven |
| `theverge` | The Verge | Tech editorial media. Acid-mint and ultraviolet accents, Manuka display type |
| `uber` | Uber | Mobility platform. Bold black and white, tight type, urban energy |
| `vodafone` | Vodafone | Global telecom brand. Monumental uppercase display, Vodafone Red chapter bands |
| `wired` | WIRED | Tech magazine. Paper-white broadsheet density, custom serif, ink-blue links |

### Automotive

| slug | 名称 | 视觉特征 |
|---|---|---|
| `bmw` | BMW | Luxury automotive. Dark premium surfaces, precise German engineering aesthetic |
| `bmw-m` | BMW M | Performance automotive. Motorsport-inspired contrast, M color accents, precision-driven layout |
| `bugatti` | Bugatti | Luxury hypercar. Cinema-black canvas, monochrome austerity, monumental display type |
| `ferrari` | Ferrari | Luxury automotive. Chiaroscuro black-white editorial, Ferrari Red with extreme sparseness |
| `lamborghini` | Lamborghini | Luxury automotive. True black cathedral, gold accent, LamboType custom Neo-Grotesk |
| `renault` | Renault | French automotive. Vivid aurora gradients, NouvelR proprietary typeface, zero-radius buttons |
| `tesla` | Tesla | Electric vehicles. Radical subtraction, cinematic full-viewport photography, Universal Sans |

### Other

| slug | 名称 | 视觉特征 |
|---|---|---|
| `dell-1996` | Dell (1996) | Catalog-era enterprise web. Literal black page frame, flat color-block "ribbon cards", chunky Helvetica-Black titles over Times Roman body, and hand-cut GIF stickers (NEW! bursts, award seals, beveled product photos). |
| `nintendo-2001` | Nintendo.com (2001) | Y2K "console chrome" web. Brushed-periwinkle beveled metal panels, a halftone-dotted carbon nav glowing amber, outlined Arial-Black box-art wordmarks over circuit-board hero fields, and a pixel Mario welcome bubble. |

### 无 README 条目（按目录名调用）

| slug | 名称 | 视觉特征 |
|---|---|---|
| `slack` | slack | 未收录描述，直接读 DESIGN.md 判读 |

## 注意

- 这些文件描述的是**设计语言的规律**，不构成品牌授权。用于内部原型、练习、风格研究是合适的；对外商用且需要品牌露出时，请自行确认商标与视觉资产的使用权限。
- 需要原仓库更新时：`https://github.com/VoltAgent/awesome-design-md`（本目录已存入 `README.md` / `LICENSE` 作为存档）。
