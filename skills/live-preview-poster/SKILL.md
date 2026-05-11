---
name: live-preview-poster
description: Use this skill when creating vertical 9:16 livestream preview posters for hosts, anchors, creators, course launches, events, or sales livestreams from a real person photo, especially when the user requires the face/person identity to remain unchanged and needs QR-code reserved space. Trigger on Chinese or English requests like 主播直播预告海报, 真人照片不改脸, 9:16海报, 二维码预留位, live preview poster, livestream announcement poster.
---

# Live Preview Poster

## Purpose

Create high-quality 9:16 vertical livestream preview posters from a real host photo. Default to image-model generation for style exploration and polished poster key visuals, then refine text/QR/person consistency as needed. The poster should have a strong, topic-appropriate visual style; style work should come from background, lighting, layout, typography, color, promotional modules, reference-derived visual elements, and owned/generated assets.

## Non-Negotiables

- Treat face preservation and poster style quality as dual requirements. Do not frame this as "sacrifice style to keep the face" or "change the face to achieve style"; choose a workflow that preserves both.
- Do not promise absolute facial consistency if the workflow redraws the face with a generative model.
- For any request like "不能改脸", "人物一致", or "真人不变", preserve the original face/person pixels: cut out the person, compose them into the poster, and design around them.
- Do not use prompts that ask the model to recreate the person from scratch.
- Do not alter facial geometry, eyes, nose, mouth, jawline, skin texture, age, gender presentation, expression, hairstyle, or body proportions unless the user explicitly asks.
- When the user prioritizes visual exploration or says identity can be relaxed, use the image model directly and prioritize beautiful commercial poster design.
- Keep a QR-code placeholder visible, usually near the lower right or lower center, with enough quiet margin and contrast.
- Default canvas is vertical 9:16. Use 1080x1920 or 1440x2560 unless the user requests another size.

## Input Handling

If no person photo is provided, ask the user to upload the photo before generating final poster images. You may still propose style directions, but do not claim final posters were generated.

If the user provides reference websites or Huaban boards, gather visual direction first. Read `references/reference-sourcing.md` for the preferred workflow, copyright boundaries, and what to save. If available, use `references/categorized-reference-catalog.md`, `references/huaban-person-poster-brief.md`, and `references/user-huaban-boards-catalog.md` as the baseline style map.

If the user provides a topic but no references, automatically research public reference directions for that topic before generating final posters. Read `references/topic-research-workflow.md`.

For actual image-model poster generation, read `references/image-model-generation.md`. It captures the working rules from prior iterations: generate one poster per call, avoid four-up collages, infer style from the user's theme/references, and avoid hardcoding fixed style lists unless the user asks for them.

Ask only for missing essentials:
- Host/person photo.
- Live title, date/time, platform, CTA, or brand colors if the user expects accurate poster text.
- QR code image if it should be embedded now; otherwise reserve a labeled placeholder.

When text details are missing, use tasteful placeholders such as:
- `直播预告`
- `今晚 20:00`
- `扫码预约`
- `主题待定`

## Face-Preservation Workflow

1. Inspect the photo and decide whether the person should be full-body, half-body, or bust based on crop quality.
2. Segment/cut out the person while keeping original face pixels untouched.
3. Build or generate the poster background separately.
4. Composite the original person layer into the layout.
5. Apply only global, low-risk visual harmonization to the person layer: exposure, color balance, soft shadow, rim light, edge cleanup. Avoid face retouching.
6. Add typography, live details, decorative elements, and QR placeholder on separate layers or in non-face regions.
7. Verify the face is not warped, over-smoothed, or replaced.

If using an image-editing tool that may regenerate pixels, mask out the face and avoid editing inside that mask. If masking is not available, choose a compositing approach over generative editing. If a chosen style cannot be achieved without changing the face, keep the face layer protected and rebuild the style around it.

## Image-Model First Workflow

Use this by default when the user asks to see styles, asks for more options, or explicitly requests image-2/image model output. Generate each candidate as a separate single 9:16 poster, not a collage or four-grid. After a promising visual direction is selected, fix exact Chinese text, QR code, and any identity-sensitive person layer issues in a refinement pass.

## Five-Style Exploration

When the user asks for multiple options, default to five distinct directions:

1. **High-Energy Commerce**: bold red/pink accents, strong price/event hierarchy, dynamic diagonal shapes, high contrast, suitable for sales livestreams.
2. **Premium Magazine**: clean editorial typography, dark or neutral luxury background, refined lighting, large portrait presence, suitable for expert or beauty/fashion hosts.
3. **Tech Neon Stage**: deep background, cyan/magenta neon, light beams, glass panels, suitable for AI, digital products, gadgets, and knowledge streams.
4. **Warm Lifestyle**: soft warm gradients or real interior texture, friendly typography, approachable CTA, suitable for personal brands, education, wellness, or community streams.
5. **Minimal Platform Card**: modern app-like grid, clear schedule block, restrained color, high readability, suitable for recurring show announcements.

Each option should preserve the same person crop and face; vary background, color, typography, layout, and decorative language.

If topic research produced stronger topic-specific categories, adapt these five directions while keeping them visually distinct and keeping at least one conservative high-readability option.

## Layout Rules

- Keep the person as the first visual priority. Common placements: lower center, lower left, or right-side vertical portrait.
- Reserve QR placeholder at 14-20% of canvas width. Keep it away from the face and key text.
- Leave a quiet zone around the QR placeholder. Use a white or very light container if the background is busy.
- Poster hierarchy should usually be:
  1. Host/person
  2. Main live title
  3. Time/date
  4. Hook or benefit
  5. QR/CTA
- Avoid placing small text over the face, hands, or hair detail.
- Ensure all text remains legible on mobile preview.

## Text Guidance

Use concise Chinese poster copy unless the user provides exact copy. Prefer short punchy lines:

- `今晚 20:00 直播见`
- `限时直播`
- `新课首发`
- `扫码预约`
- `干货专场`
- `新品发布`

Do not invent factual claims such as discounts, credentials, dates, or platform names unless supplied by the user.

## Quality Check

Before final response or delivery, check:

- The poster is 9:16.
- The original face identity is preserved.
- The poster still has a clear, polished, topic-appropriate visual style.
- The face is not covered by text, QR code, glare, or decorations.
- QR placeholder is obvious and scannable once replaced with a real QR code.
- Title/date/CTA are readable at mobile size.
- The five options are meaningfully different, not just recolors.

## User-Facing Language

When discussing consistency, be precise:

- Good: "我可以用不重画人脸的合成流程来最大化保证一致性。"
- Good: "如果用纯生成式重绘，我不能保证 100% 不变；所以这类海报应保留原图人物图层。"
- Avoid: "我保证模型生成出来脸完全一样。"
