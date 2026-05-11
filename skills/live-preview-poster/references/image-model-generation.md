# Image Model Generation

Use this reference when generating livestream preview poster candidates with an image model such as image-2. This workflow is for visual exploration and polished key-visual output.

## Default Behavior

- Use the image model for first-pass poster style exploration.
- Generate one finished 9:16 poster per image generation call.
- Do not ask for "4 posters in one image", "four variations", "grid", "collage", or "moodboard" unless the user explicitly wants a comparison sheet.
- For 4 options, make 4 separate generation calls with 4 distinct prompts.
- Use references as taste signals, not rigid constraints. Analyze the user's theme, reference image, board, or described style and mimic the underlying visual language without copying exact assets.

## Prompt Skeleton

Use a prompt like:

```text
Create ONE single finished vertical 9:16 Chinese livestream preview poster, not a collage, not a grid, not multiple designs.
Theme title: "<main title>".
Subtitle: "<subtitle>".
Time: "<date/time>".
Include a tasteful bottom-right QR-code placeholder labeled "扫码预约".
Style: <specific style direction>.
Use a stylish teacher/host/director figure as the hero.
Prioritize beautiful commercial poster design, strong visual hierarchy, large readable Chinese typography, high-end social media course launch polish.
9:16 vertical composition only.
```

If exact identity matters, add:

```text
Use the uploaded portrait as the identity reference. Preserve the face, facial geometry, glasses, hairstyle, expression, age, and body proportions as closely as possible. Do not turn the person into someone else.
```

If the user says face identity is not important, do not over-constrain identity; focus on visual quality.

## Chinese Text Reality

Image models may distort Chinese, especially small text. Use image output for key visual exploration. For final delivery:

- Recompose or overlay exact Chinese text locally if accuracy matters.
- Place the real QR code or a clean placeholder locally if the generated QR area is wrong.
- Keep model-generated text limited to large title blocks when possible.

## Style Intelligence

Do not hardcode a fixed style list into the Skill. Instead, infer style from the current request.

For any provided style phrase, reference board, or image, extract:

- Color system: dominant colors, accent colors, contrast level.
- Composition: person size, person placement, negative space, text zones, QR area.
- Material language: photo-real, 3D, illustration, collage, paper, glass, metallic, grain, ink, etc.
- Lighting: soft, dramatic, neon, stage, natural, sunset, high-key, low-key.
- Typography mood: bold, editorial, playful, premium, tech, handwritten, poster-like.
- Energy level: calm, premium, warm, enthusiastic, cool, surreal, commercial.
- Motifs: camera, film strip, storyboard, abstract geometry, product shapes, seasonal objects, etc.

Then translate those attributes into an original image-model prompt. The Skill should be able to follow styles such as `虚实结合`, `热情活泼`, `高级`, `酷炫`, `杂志感`, `综艺感`, `电影感`, or any user-provided image/board without needing the style to be prelisted.

If the style phrase is vague:

- Generate 3-5 plausible visual interpretations.
- Make each interpretation visibly different.
- Ask the user which direction feels closest after showing samples.

If the reference is too restrictive or makes outputs ugly/template-like:

- Keep the reference's useful design DNA.
- Loosen exact layout, colors, and decorative details.
- Prioritize a beautiful, commercially usable poster.

Always keep a strong hierarchy: hero person, main title, subtitle/time, QR.

## Multi-Option Generation Pattern

When the user asks "再给我 4 张" or similar:

1. Generate 4 separate images.
2. Keep the same topic and time.
3. Change only the style direction and visual language.
4. Do not repeat previous styles unless the user asks for more of one direction.
5. Briefly summarize which one is most promising and why.

For each option, describe the inferred style direction in one sentence, based on the user's current theme/references.

## Refinement Pattern

After the user chooses a direction:

- Preserve the selected visual style.
- Fix exact text and date.
- Make QR placeholder clean, or insert the user's real QR code.
- If identity matters, bring back the user's original portrait through a protected-layer compositing pass or masked edit.
- If identity does not matter, refine purely inside image model.
