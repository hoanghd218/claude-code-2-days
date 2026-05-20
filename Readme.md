# Claude Code 2 Days — Bộ Skills

![Freedom Builders](freedom%20builder.png)

> 💎 **Được chia sẻ bởi Tony Hoang — cộng đồng Freedom Builders.**
> Tham gia cộng đồng: 👉 [whop.com/freedombuilders/freeclub](https://whop.com/freedombuilders/freeclub?a=hoangtranai)
> Theo dõi video kiến thức: 🎥 [YouTube](https://www.youtube.com/@tony-hoang-ai-automation/videos) · 👤 [Facebook](https://www.facebook.com/tranvanhoangcom/)

---

Dự án này gom **66+ skills** cho Claude Code, chia 2 thư mục:

- [.claude/skills/](.claude/skills/) — **53 skills** chính, dùng được ngay khi mở Claude Code trong thư mục này.
- [.agents/skills/](.agents/skills/) — **13 skills** HyperFrames (video) sync từ `heygen-com/hyperframes` qua [skills-lock.json](skills-lock.json).

> **Skill là gì?** Là một "kỹ năng" có sẵn instruction + asset, Claude tự nhận diện và kích hoạt khi prompt của bạn match từ khoá. Bạn **không cần gõ tên skill** — chỉ cần mô tả việc cần làm. Claude sẽ tự gọi skill phù hợp.

# Sách Going Viral được đóng gói thành các agents và skills : https://lab.hookpoint.com/wp-content/uploads/2024/09/Going-Viral-Guide-Free-Version.pdf
---

## Mục lục nhanh

1. [Cách sử dụng (60 giây)](#cách-sử-dụng-60-giây)
2. [Marketing & Content (Kane series)](#1-marketing--content-kane-series) — viết Reels, FB post, YouTube script
3. [Video Production (HyperFrames)](#2-video-production-hyperframes) — render video bằng HTML
4. [Tài liệu (docx / pptx / xlsx / pdf)](#3-tài-liệu-docx--pptx--xlsx--pdf)
5. [Thiết kế & UI](#4-thiết-kế--ui)
6. [Web & App Building](#5-web--app-building)
7. [Dev Tools](#6-dev-tools)
8. [Tiện ích khác](#7-tiện-ích-khác)

---

## Cách sử dụng (60 giây)

1. Mở Claude Code trong thư mục `claude code 2 days`.
2. Gõ yêu cầu bằng ngôn ngữ tự nhiên — Claude tự match skill.
3. Nếu muốn ép gọi skill cụ thể, gõ `/` + tên skill (ví dụ `/skill-creator`).

**Ví dụ tổng quát:**
```
viết bài Facebook về Claude Code hooks theo blend feelings + facts + fun
```
→ Claude tự kích hoạt `mkt-kane-fb-post-communication-algorithm`.

```
tạo file Excel báo cáo doanh thu Q1 với chart
```
→ Claude tự kích hoạt `xlsx`.

---

## 1. Marketing & Content (Kane series)

Bộ 16 skills viết content theo các format đã được validate (Brendan Kane, Daniel Wall, Sabrina Ramonov, Mark Rober, Veritasium, Matt d'Avella…). Hầu hết tiếng Việt, tối ưu cho ngách AI/automation/tech.

### Reels 30-90s

| Skill | Format | Ví dụ prompt |
|---|---|---|
| `mkt-kane-reels-untold-stories` | Behind-the-scenes + 'Oh wait what?!' moment | `viết reels untold stories về cách Claude Code chạy hooks ngầm` |
| `mkt-kane-reels-paste-this-tag-listicle` | Lead magnet + N tag UPPERCASE + 1-line benefit | `viết reels paste tag với 5 secret commands trong Claude Code` |
| `mkt-kane-reels-jenga-tension` | Stack 3 micro-question, payoff close loop | `viết reels jenga theory về MCP server` |
| `mkt-kane-reels-visual-metaphor` | Dùng prop vật lý minh hoạ concept trừu tượng | `viết reels visual metaphor về context window dùng cái xô` |
| `mkt-kane-reels-is-it-worth-it` | Deconstruct 1 product → verdict fair | `viết reels is it worth it review Claude Pro $20/tháng` |

### Facebook post

| Skill | Format | Ví dụ prompt |
|---|---|---|
| `mkt-kane-fb-post-communication-algorithm` | Blend Feelings 30% + Facts 25% + Fun 20% | `viết fb post về AI agent theo communication algorithm` |
| `mkt-kane-fb-post-golden-triangle` | Personal story + Evidence/data + Timeless wisdom | `viết facebook golden triangle về việc bỏ job 9-5 build AI agency` |

### YouTube longform

| Skill | Format | Ví dụ prompt |
|---|---|---|
| `mkt-kane-youtube-jenga-longform` | 10-20 phút Mark Rober/Veritasium style | `viết script youtube jenga 15 phút thử Claude Code build app trong 1 ngày` |
| `mkt-kane-youtube-30-day-challenge` | Documentary 30 ngày kiểu Matt d'Avella | `viết youtube 30 day challenge dùng Claude Code mỗi ngày` |

### Audit & Research

| Skill | Tác dụng | Ví dụ prompt |
|---|---|---|
| `mkt-kane-anti-pattern-auditor` | Phát hiện over-branding, stock imagery, frequency-over-quality | `audit content fb post này có anti-pattern gì không` |
| `mkt-kane-gold-comparison-reviewer` | So sánh draft của bạn vs Gold reference (8 drivers) | `so sánh draft này với gold reference [link]` |
| `mkt-kane-gsb-research-builder` | Build Gold-Silver-Bronze sheet cho 1 creator/format | `tạo gsb sheet cho channel Veritasium` |
| `mkt-kane-viral-format-identifier` | Phân biệt Viral Format (lâu dài) vs Trend (nhất thời) | `video này dùng format gì hay chỉ là trend?` |
| `mkt-kane-cross-industry-viral-scout` | Tìm format ngành khác apply cho ngách AI | `tìm format ngành bác sĩ apply được cho AI educator` |
| `mkt-kane-eov-reverse-engineer` | Bắt đầu từ Effect on Viewer → reverse ra format | `viewer cần cảm thấy 'wow shock' — gợi format` |

### Rewriting

| Skill | Tác dụng | Ví dụ prompt |
|---|---|---|
| `mkt-kane-triple-f-boost` | Retrofit content có sẵn đạt blend ≥75% | `triple f boost bài fb này` |
| `mkt-kane-cta-non-autocratic-rewriter` | Sửa CTA "Mua ngay!" sang Democratic/Benevolent/Laissez-faire | `rewrite cta 'Đăng ký ngay!' nhẹ nhàng hơn` |
| `mkt-kane-generalist-repackager` | Niche tech → mass appeal hook | `repackage topic 'MCP server' thành hook universal` |

---

## 2. Video Production (HyperFrames)

Render video bằng HTML/CSS/JS deterministic. **Skill chính: `hyperframes`** — các skill còn lại là adapter cho thư viện cụ thể.

| Skill | Khi nào dùng | Ví dụ prompt |
|---|---|---|
| `hyperframes` | Composition video, captions, voiceover, transitions | `tạo video 30s giới thiệu product với caption sync audio` |
| `hyperframes-cli` | Dev loop — init, lint, preview, render | `init project hyperframes mới rồi render ra mp4` |
| `hyperframes-media` | TTS, transcribe, remove background | `dùng kokoro TTS đọc script này, sau đó transcribe để làm caption` |
| `hyperframes-registry` | Cài registry blocks/components | `add component hero-banner từ registry vào composition` |
| `website-to-hyperframes` | URL → video promo | `capture trang https://anthropic.com rồi tạo video 15s social ad` |
| `remotion-to-hyperframes` | Port Remotion → HyperFrames | `migrate composition Remotion này sang HyperFrames` |
| `gsap` | Animation timeline GSAP | (Claude tự gọi khi viết animation trong hyperframes) |
| `animejs` | Anime.js timeline | (auto) |
| `waapi` | Web Animations API native | (auto) |
| `css-animations` | CSS keyframes deterministic | (auto) |
| `three` | 3D scene, shader, WebGL | `thêm scene 3D xoay logo trong video` |
| `lottie` | Lottie/dotLottie animation | `embed file .lottie animation vào scene 2` |
| `tailwind` | Tailwind v4 trong composition | (auto khi project init với --tailwind) |

### HeyGen MCP (talking-head video)

Dự án có sẵn HeyGen MCP. Ví dụ prompt:
```
tạo video 60s avatar HeyGen đọc script "Welcome to Claude Code 2 Days"
```
Claude sẽ gọi `create_video_agent` và trả link `https://app.heygen.com/video-agent/{session_id}` để bạn theo dõi.

---

## 3. Tài liệu (docx / pptx / xlsx / pdf)

| Skill | Khi nào dùng | Ví dụ prompt |
|---|---|---|
| `docx` | Word doc — report, memo, letter, template | `tạo docx báo cáo dự án có TOC, heading, page number` |
| `pptx` | Slide deck PowerPoint | `tạo pptx pitch deck 10 slides về AI startup` |
| `xlsx` | Excel/CSV — đọc, edit, formula, chart | `đọc file revenue.xlsx và thêm cột tăng trưởng % MoM` |
| `pdf` | PDF — read, merge, split, OCR, fill form | `merge 3 file pdf này thành 1, rotate page 5` |
| `skill-creator:html-slides` | Slide HTML 16:9 standalone (không cần PowerPoint) | `tạo slides html về Claude Code hooks` |

---

## 4. Thiết kế & UI

| Skill | Khi nào dùng | Ví dụ prompt |
|---|---|---|
| `ui-ux-pro-max` | UI/UX với 67 styles, 96 palettes, 13 stacks (React/Vue/Svelte/Flutter…) | `design dashboard SaaS theme glassmorphism dark mode` |
| `frontend-design` | Frontend production-grade, tránh AI-generic look | `build landing page React + Tailwind cho AI agency` |
| `canvas-design` | Poster, art tĩnh ra .png/.pdf | `tạo poster A4 quảng cáo workshop AI` |
| `theme-factory` | Apply 10 pre-set themes lên artifact bất kỳ | `apply theme 'midnight' cho slide deck vừa tạo` |
| `brand-guidelines` | Anthropic official brand colors/typography | `style file này theo Anthropic brand guidelines` |
| `algorithmic-art` | p5.js generative art, flow field, particle system | `tạo flow field art seed 42 với 1000 particles` |
| `slack-gif-creator` | GIF animated cho Slack | `tạo GIF rocket bay lên cho Slack` |

---

## 5. Web & App Building

| Skill | Khi nào dùng | Ví dụ prompt |
|---|---|---|
| `web-artifacts-builder` | Artifact phức tạp (React + Tailwind + shadcn/ui + state) | `build dashboard React có routing và shadcn/ui cards` |
| `webapp-testing` | Playwright test/debug local app | `chạy app rồi test golden path login flow, screenshot mỗi step` |

---

## 6. Dev Tools

| Skill | Khi nào dùng | Ví dụ prompt |
|---|---|---|
| `claude-api` | Code dùng Anthropic SDK — caching, thinking, tool use | `migrate code này từ Sonnet 4.5 sang Opus 4.7 + thêm prompt caching` |
| `mcp-builder` | Build MCP server (Python FastMCP / Node TS SDK) | `build MCP server expose API thời tiết với 3 tools` |
| `skill-creator` | Tạo / sửa / eval skill mới | `tạo skill mới giúp viết LinkedIn post theo format X` |
| `update-config` | Sửa settings.json, hooks, permissions | `add hook tự chạy npm test sau mỗi edit file .ts` |
| `keybindings-help` | Customize keyboard shortcut | `rebind ctrl+s sang chord shortcut` |
| `fewer-permission-prompts` | Scan transcript → allowlist Bash/MCP | `giảm permission prompt cho các lệnh git/npm` |
| `simplify` | Review code đã đổi, tìm reuse + fix issue | `simplify file vừa edit` |

---

## 7. Tiện ích khác

| Skill | Khi nào dùng | Ví dụ prompt |
|---|---|---|
| `doc-coauthoring` | Co-author proposal/spec/decision doc qua workflow có cấu trúc | `co-author spec cho feature notification system` |
| `internal-comms` | Status report, leadership update, FAQ, incident report nội bộ | `viết incident report cho deploy fail hôm qua` |
| `youtube-trend-finder` | Fetch video mới từ subscribed channels | `tìm video trending từ kênh đã subscribe trong 24h` |
| `loop` | Chạy prompt theo interval | `/loop 5m check deploy status` |
| `schedule` | Cron job remote agent | `schedule chạy /babysit-prs mỗi sáng 9am` |
| `init` | Khởi tạo CLAUDE.md cho repo mới | `/init` |
| `review` | Review PR | `/review PR#123` |
| `security-review` | Security review branch hiện tại | `/security-review` |
| `skill-creator:viet-fb-actionable-post` | FB post AI/tech tiếng Việt casual | `viết bài fb về 5 cách dùng Claude Code tiết kiệm 10h/tuần` |
| `codex:rescue` | Delegate sang Codex khi Claude bí | `delegate task này cho codex investigate` |

---

## Tips dùng skills hiệu quả

1. **Mô tả rõ goal + audience** thay vì gọi tên skill. Ví dụ thay vì `dùng skill X`, hãy viết `viết reels 60s về Y cho audience là dev junior`.
2. **Dán reference link** khi muốn so sánh/audit (`mkt-kane-gold-comparison-reviewer` cần Gold reference).
3. **Chain nhiều skill** trong 1 prompt — ví dụ `viết script reels jenga + render bằng hyperframes + đọc bằng heygen TTS`.
4. **Chỉnh sửa lock file** [skills-lock.json](skills-lock.json) nếu muốn pin version skill HyperFrames cụ thể từ GitHub.
5. **Tạo skill riêng** — gõ `/skill-creator` nếu format/workflow của bạn lặp đi lặp lại.

---

## Tham khảo nhanh

- Tài liệu Claude Code: https://docs.claude.com/claude-code
- HeyGen app: https://app.heygen.com
- HyperFrames source: `heygen-com/hyperframes` (GitHub)

> Có skill mới muốn thêm? Chạy `/skill-creator` hoặc dán SKILL.md vào `.claude/skills/<tên>/`.

---

## 🌟 Cộng đồng Freedom Builders

Bộ skills này được chia sẻ miễn phí bởi **Tony Hoang** dành cho cộng đồng **Freedom Builders** — nơi quy tụ những người đang dùng AI để build doanh nghiệp tự do, automation, và content tăng tốc.

👉 **Tham gia free club:** [whop.com/freedombuilders/freeclub](https://whop.com/freedombuilders/freeclub?a=hoangtranai)

Trong cộng đồng bạn sẽ nhận được:
- 🛠️ Skills + workflow Claude Code mới mỗi tuần
- 🎬 Template HyperFrames / HeyGen sẵn sàng dùng
- 📈 Playbook content marketing AI (Kane series, viral format)
- 💬 Q&A trực tiếp + feedback từ Tony và builders khác

---

## 📺 Theo dõi Tony Hoang — video kiến thức AI & automation

- 🎥 **YouTube:** [@tony-hoang-ai-automation](https://www.youtube.com/@tony-hoang-ai-automation/videos) — tutorial Claude Code, MCP, AI agent, automation workflow
- 👤 **Facebook:** [facebook.com/tranvanhoangcom](https://www.facebook.com/tranvanhoangcom/) — case study, tips ngắn, behind-the-scenes

> Subscribe + bật chuông để không bỏ lỡ video kiến thức mới.
