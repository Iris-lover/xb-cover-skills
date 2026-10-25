# xb-xhs-bilibili-cover

用你自己的照片和喜欢的风格创建小红书 / Bilibili 封面。一个 Skill，支持两种平台。

[中文](#中文) · [English](#english)

## 中文

### 功能与流程

1. 开始先索要用户本人的照片和期望风格，可用文字或参考图说明。
2. 确认平台、主题、准确标题及截图 / 流程 / Logo 等素材。
3. 逐步确认人物位置与构图，使用可用图片工具制作封面。
4. 卡通分身为可选项，仅根据当前用户的照片创建。

| 平台 | 建议画幅 | 说明 |
| --- | --- | --- |
| 小红书 | 3:4，1080×1440 | 竖版人物、截图、流程或 Logo 布局 |
| Bilibili / B 站 | 16:9，1920×1080；4:3，1440×1080 | 横版构图、截图对比及跨平台改版 |

尺寸是设计建议，不是平台强制要求。跨尺寸分别重排，不只裁切或补边。用户选择的风格优先；奶油纸底、深棕标题与手绘贴纸仅为可选方向。

### 安装

需要支持本地 `SKILL.md` 的 AI 助手和可用的图片生成或编辑工具。本仓库提供规则与提示词，不包含模型、API 密钥或图片工具自动安装程序。

```bash
git clone https://github.com/Iris-lover/xb-cover-skills.git
mkdir -p ~/.claude/skills
cp -R xb-cover-skills/xb-xhs-bilibili-cover ~/.claude/skills/
```

已有同名 Skill 时先备份并手动合并。若 `~/.codex/skills` 已映射至 `~/.claude/skills`，无需重复复制；其他助手使用其 Skill 发现目录。

原来的 `xb-xhs-cover` 和 `xb-blibili-cover` 已合并为 **`xb-xhs-bilibili-cover`**。升级后使用新名称调用；旧安装如需停用，请先备份私人素材，再手动移出 Skill 发现目录。

### 使用示例

```text
使用 $xb-xhs-bilibili-cover，帮我制作小红书封面。
请先索要我的个人照片和想要的风格，再逐步确认构图。
```

```text
使用 $xb-xhs-bilibili-cover，把刚确认的封面改为 B 站 16:9。
保留准确标题、我的照片与风格，重新排版。
```

### 素材与隐私

不包含或调用作者的真人照片、照片库或专属卡通形象。仅使用当前用户提供或明确指定的照片，不自动收录照片、索引或使用历史；长期保存需用户明确要求并指定位置。

请使用你有权使用的照片、截图和 Logo。生成式工具可能改变人物或界面细节；要求像素保真时需采用原图合成并检查结果，不把 AI 重绘称作无损合成。

### 目录

```text
xb-xhs-bilibili-cover/
  SKILL.md
  agents/openai.yaml
  references/
    xiaohongshu.md
    bilibili.md
    visual-system.md
    design-system-test.md
    design-system-test-prompt.txt
```

通用案例使用占位内容，不含作者的外貌、服装或角色设定，不预填效果百分比。Skill 正文与参考提示词为中文。

## English

Create Xiaohongshu and Bilibili covers with your own portrait and preferred style through one skill: **`xb-xhs-bilibili-cover`**.

### Workflow

1. Start by asking for your own portrait and desired style, described in words or reference images.
2. Confirm the platform, topic, exact title, and any screenshots, workflows, or logos.
3. Confirm the portrait placement and layout step by step, then use an available image tool.
4. Include a cartoon avatar only if requested, based solely on your own portrait.

| Platform | Suggested canvas | Layout |
| --- | --- | --- |
| Xiaohongshu | 3:4 at 1080×1440 | Portrait layouts with screenshots, steps, or logos |
| Bilibili | 16:9 at 1920×1080; 4:3 at 1440×1080 | Landscape layouts, screenshot comparisons, and platform adaptations |

Dimensions are recommendations, not mandatory platform requirements. Each aspect ratio requires a new layout rather than cropping or adding borders. Your chosen style takes priority; cream paper backgrounds and hand-drawn stickers are optional.

### Installation

You need an assistant that discovers local `SKILL.md` files and an available image generation or editing tool. This repository supplies workflows and prompts, not models, API keys, or automatic image-tool installation.

```bash
git clone https://github.com/Iris-lover/xb-cover-skills.git
mkdir -p ~/.claude/skills
cp -R xb-cover-skills/xb-xhs-bilibili-cover ~/.claude/skills/
```

Back up and merge any existing installation with the same name. If `~/.codex/skills` already points to `~/.claude/skills`, no second copy is needed. Other assistants should use their configured skill discovery directory.

The former `xb-xhs-cover` and `xb-blibili-cover` have been merged into **`xb-xhs-bilibili-cover`**. Use the new name after upgrading. To disable old installations, back up private assets before manually moving those folders out of the discovery directory.

### Examples

```text
Use $xb-xhs-bilibili-cover to create a Xiaohongshu cover.
First ask me for my own portrait and desired style, then confirm the layout step by step.
```

```text
Use $xb-xhs-bilibili-cover to adapt the approved cover to 16:9 for Bilibili.
Keep my exact title, portrait, and chosen style. Create a new layout.
```

### Assets and privacy

The skill does not include or use the author’s portraits, photo library, or personal cartoon character. It uses only photos provided or explicitly selected by the current user. Photos, catalogs, and usage history are not stored automatically; persistent storage requires an explicit request and a chosen location.

Use photos, screenshots, and logos you have permission to use. Generative tools may alter people or interface details. Use source-image compositing and verify the output when pixel fidelity is required; do not describe AI-redrawn material as lossless compositing.

### Structure

```text
xb-xhs-bilibili-cover/
  SKILL.md
  agents/openai.yaml
  references/
    xiaohongshu.md
    bilibili.md
    visual-system.md
    design-system-test.md
    design-system-test-prompt.txt
```

Reference cases use placeholders without the author’s appearance, clothing, or character design, and without preset performance percentages. Skill instructions and reference prompts are written in Chinese.
