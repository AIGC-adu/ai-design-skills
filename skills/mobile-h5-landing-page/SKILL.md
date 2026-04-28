---
name: mobile-h5-landing-page
description: Use when the user wants to design, generate, or edit a mobile H5 landing page image, long-form mobile poster, campaign signup page, course detail page, event registration page, livestream reservation page, competition submission page, or product introduction page. This skill is especially for AI image generation prompts, H5 long-image structure, mobile conversion copy, KV extension, and design execution guidance.
---

# Mobile H5 Landing Page

Use this skill when the user asks for mobile H5 page design, H5 long images, landing-page posters, course sales pages, competition recruitment pages, event signup pages, livestream reservation pages, product intro pages, or AI-generated H5 design images.

The goal is to turn minimal user information into a mobile-first conversion page that is easy to understand, visually unified, and ready for AI image generation, design execution, or frontend implementation.

## Core Judgment

Always first identify:

1. Page type: competition, course, event, livestream, product, or other.
2. Conversion goal: signup, submission, reservation, lead capture, purchase, consultation, or trial.
3. Whether the user provided an existing KV, reference image, brand style, or visual direction.
4. Whether the content should be one image or split into 2-3 long-image segments.
5. Whether the user wants a plan, a prompt, an actual generated image, or an editable implementation.

## Mobile H5 Principles

Mobile H5 is not a shrunken PC webpage. It should feel like a vertical mobile long image or swipeable mobile landing page.

Required:

- Single-column vertical structure.
- One key idea per screen.
- Clear reading path from attraction to conversion.
- Large headings, short copy, strong spacing.
- Obvious CTA in the first screen and bottom section.
- Visual language inherited from the KV when provided.
- Low information density and strong mobile readability.

Avoid:

- PC-style multi-column layout.
- Dense tables or long paragraphs.
- Stacked UI-card grids.
- Tiny text.
- Complex navigation.
- Too many decorative elements competing with content.

## Page Path

Use this default path:

```text
First-screen hook -> Value -> Content -> Trust -> Conversion
```

For longer pages:

```text
Part 1: First screen + core value
Part 2: Content + rules/details
Part 3: Trust + CTA conversion
```

## Size Guidance

- First-screen poster: 9:16.
- Short H5 preview: 1:2.
- Full mobile H5 preview: 9:20 or 1000 x 2000.
- Complex pages: split into 2-3 segments instead of forcing all content into one image.

Each generated segment should carry at most 3-4 core modules.

## Structure By Page Type

### Competition

Use:

```text
1. First-screen banner
2. Competition highlights
3. Track introduction
4. Submission requirements
5. Awards
6. Timeline
7. Judging criteria
8. Judges or trust module
9. Submission CTA
```

Keep highlights to 3 points. Make submission requirements icon-like and short.

### Course

Use the conversion path:

```text
Pain point -> Course solution -> Learning modules -> Results -> Teacher trust -> Student work -> Signup CTA
```

Answer:

```text
Why should I learn?
Can I learn it?
What can I do after learning?
Who teaches it?
Are there cases or proof?
How do I sign up now?
```

### Event Or Livestream

Use:

```text
1. First-screen banner
2. Event highlights
3. Guest introduction
4. Agenda
5. What you will gain
6. Suitable audience
7. Participation method
8. Reservation CTA
```

### Product

Use:

```text
1. First-screen banner
2. User pain points
3. Product value
4. Core features
5. Use cases
6. Case proof
7. Service assurance
8. Trial or consultation CTA
```

## KV Extension Rules

If the user provides a KV or reference image:

- First screen: keep the strongest KV identity.
- Middle sections: weaken the KV, preserve atmosphere, color, motifs, texture, and icon style.
- Bottom: strengthen CTA and visually close the page.

Inherit:

- Main color system.
- Title style.
- Background atmosphere.
- Mascot/IP/hero object if present.
- Core visual symbols.
- Button and CTA style.

Avoid repeating the full KV in every section.

## Copy Rules

- Prefer keywords and short phrases over paragraphs.
- Each module should usually stay within 3 lines of core information.
- Value points should be concrete and result-oriented.
- CTA should be direct: "立即报名", "扫码投稿", "立即预约", "领取资料", "申请试用".
- Avoid weak CTA copy such as "了解更多", "查看更多", "点击这里".

## Output When User Wants A Plan

Return:

1. Page structure table.
2. Detailed section-by-section content.
3. Visual direction.
4. CTA advice.
5. Whether to split the image.
6. AI image-generation prompt.

Use this table shape:

```markdown
| Screen | Module | Purpose | Content | Visual Focus | CTA |
|---|---|---|---|---|---|
| 01 | First-screen banner | Hook | Main title / subtitle / CTA | KV hero visual | 立即报名 |
```

## Output When User Wants An Image

Use the image-generation tool after forming a complete prompt. Do not stop at giving a prompt unless the user specifically asks for prompt only.

The prompt must include:

```text
Image type:
Aspect ratio:
Overall style:
Page type:
Module order:
Exact visible copy:
Visual focus:
Layout requirements:
Avoid:
```

Important image prompt requirements:

- Ask for a polished mobile H5 long-page preview.
- Use single-column vertical composition.
- Use strong top hero area, readable middle modules, and clear bottom CTA.
- Keep text sparse and large enough to read.
- Do not request dense tiny Chinese text.
- If many details are needed, generate segmented images instead of one overcrowded image.

## Quality Check

Before finalizing, check:

- Can the first screen be understood in 3 seconds?
- Does every section have only one focus?
- Is the page vertical and mobile-first?
- Is the CTA obvious?
- Is the page too card-heavy?
- Is there enough side padding and breathing room?
- Does it inherit the KV when one exists?
- Does it look like a formal H5 page instead of a PC webpage screenshot?

## One-Sentence Rule

Mobile H5 is not about putting all information on the page; it is about using clear rhythm to move the user toward action.
