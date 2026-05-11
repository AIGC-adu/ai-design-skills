# ai-design-skills 使用说明

GitHub 地址：

https://github.com/AIGC-adu/ai-design-skills

这个仓库是多个独立 Codex Skills 的集合。安装时要指定具体 Skill 子目录。

## Skill 列表

```text
skills/mobile-h5-landing-page
skills/live-preview-poster
```

## 安装 H5 落地页 Skill

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo AIGC-adu/ai-design-skills \
  --path skills/mobile-h5-landing-page
```

调用方式：

```text
用 $mobile-h5-landing-page 帮我生成平台内赠课详情页 H5。

课程名称：
【填写课程名称】

课程介绍：
【填写课程介绍】

核心模块：
【填写课程模块】

页面要求：
- 按 750px 手机 H5 宽度设计
- 信息少就分 2 段
- 内容多再分 3 段
- 每段单独出图，方便后期拼合
```

## 安装海报 Skill

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo AIGC-adu/ai-design-skills \
  --path skills/live-preview-poster
```

调用方式：

```text
用 $live-preview-poster 帮我做一张 9:16 直播预告海报。

主题：导演思维五步法，让故事身价翻倍
人物：上传照片
时间：5月7日 19:00
二维码：右下角预留
风格：参考我给的图片，整体更热情、更酷炫
```

默认规则：

- 优先用 image-2 / 图像模型做海报风格探索。
- 多方案时每张单独生成，不做四宫格。
- 能根据主题、参考图、风格词或花瓣画板自动分析风格。
- 选中方向后，再精修中文、二维码和人物一致性。

## 后续新增 Skill 的约定

新增 Skill 时，放在：

```text
skills/<skill-name>/
```

每个 Skill 至少包含：

```text
skills/<skill-name>/
├── SKILL.md
└── agents/
    └── openai.yaml
```

如果需要参考资料，放在该 Skill 自己的 `references/` 目录下。不要把多个 Skill 的规则混写到同一个 `SKILL.md` 里。
