# Topic Research Workflow

Use this when the user gives a poster topic but no reference links. The goal is to automatically gather public style direction, classify it, then create original 9:16 livestream poster options while preserving the uploaded person's face.

## Inputs

Minimum useful input:
- Topic or livestream theme.
- Person/host photo for final poster generation.

Helpful optional input:
- Audience.
- Industry.
- Platform: Douyin, WeChat Video, Xiaohongshu, Kuaishou, Bilibili, webinar, private community.
- Date/time.
- Brand color or logo.
- QR code image or QR placeholder location.
- Tone: premium, commercial, warm, tech, professional, playful.

## Research Sources

Use public, accessible references. Prefer source diversity:

- Huaban: Chinese poster and livestream template patterns.
- Gaoding / DesignKit / Chuangkit: commercial template category language and layout norms.
- ZCOOL / Behance / Dribbble: higher-polish visual directions.
- Xiaohongshu/Pinterest only when publicly accessible; otherwise use search snippets or ask the user for screenshots/boards.

Do not ask for account passwords. If a source is login-blocked or anti-scraping protected, fall back to public search results, screenshots, or user-provided boards.

## Search Query Pattern

Generate 5-8 focused queries from the topic:

- `<topic> 直播预告 海报 竖版`
- `<topic> 主播 海报 9:16`
- `<industry> 直播海报 二维码`
- `<topic> 课程 讲师 海报`
- `<topic> 发布会 直播预告`
- `<topic> poster livestream announcement`
- `site:huaban.com/pins <topic> 直播预告 海报`
- `site:gaoding.com <topic> 直播预告 海报`

For Chinese business posters, include Chinese keywords first. For global design polish, add English queries.

## Classification

Group collected references into 3-5 style buckets. Default buckets:

1. High-energy conversion/commercial.
2. Premium editorial/magazine.
3. Tech/stage/futuristic.
4. Warm lifestyle/community.
5. Minimal professional/platform card.

Rename buckets if the topic demands it. Examples:

- AI design course: `AI neon keynote`, `premium knowledge lecturer`, `minimal course card`, `creator community warm`, `commercial enrollment`.
- Beauty livestream: `soft peach beauty`, `luxury black-gold`, `commerce deal`, `magazine portrait`, `platform QR card`.
- Finance livestream: `blue professional`, `black-gold authority`, `minimal data card`, `lecturer profile`, `warm trust`.

## Save A Topic Brief

When the research will be reused, save a compact brief under:

`references/topic-<slug>-brief.md`

Include:
- Topic.
- Date.
- Search queries used.
- Reference links.
- Style buckets.
- Layout and typography notes.
- QR placement notes.
- Face-preservation constraints.
- Five prompt seeds for original poster generation.

Do not save bulk downloaded reference images unless the user explicitly owns or licenses them.

## Poster Generation Plan

After topic research:

1. Pick 5 visually distinct style directions.
2. Keep a consistent protected person layer across all versions.
3. Vary background, color, typography, title module, and QR module.
4. Keep all face pixels original; if a tool path would redraw or distort the face, use a protected-layer compositing workflow instead.
5. Use generated/original backgrounds and owned assets only.
6. Deliver options as style drafts; ask the user to pick one for refinement.

## User-Facing Summary

Briefly tell the user:

- Which sources were accessible.
- Which style buckets were found.
- Any access limitations.
- That final posters are original compositions and do not directly copy reference images.
