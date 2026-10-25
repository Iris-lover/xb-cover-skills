# XB Cover Skills

用你自己的照片和喜欢的风格创建封面。开始时，Skill 会先索要你的个人照片与期望风格，再逐步确认标题和构图。适用于 AI 工具、设计教程、工作流、推荐与测评。

[中文](#中文) · [English](#english)

## 中文

### 包含的 Skill

| Skill | 用途 | 建议画幅 |
| --- | --- | --- |
| [xb-blibili-cover](xb-blibili-cover/SKILL.md) | B 站横版封面；支持截图对比、流程、Logo，以及从小红书封面重排 | 16:9，1920×1080；4:3，1440×1080 |
| [xb-xhs-cover](xb-xhs-cover/SKILL.md) | 小红书封面；先收集用户照片与风格，再确认标题、信息结构与可选卡通分身 | 3:4，1080×1440 |

以上尺寸是设计建议，并非平台强制规格。`xb-blibili-cover` 的名称保留原拼写。

### 视觉风格

风格由你决定，可提供文字描述或参考图。下方手绘贴纸风仅作可选方向，不强制套用。卡通分身为可选项，仅依据你本人的照片创建。不会调用作者的真人或卡通形象。

奶油暖白底、深棕粗标题、局部暖黄高亮、鼠尾草绿手绘线与简洁纸贴信息卡。真人照片承担人物身份，截图和 Logo 提供内容证据。两种封面均仅在你选择时加入基于你本人照片的卡通分身。

### 安装

需要一个支持本地 `SKILL.md` 的 AI 助手，以及可用的图片生成或编辑工具。本仓库提供工作流与提示词，不包含图片生成 API、模型或密钥，也不会自动安装相关工具。

```bash
git clone https://github.com/Iris-lover/xb-cover-skills.git
mkdir -p ~/.claude/skills
cp -R xb-cover-skills/xb-blibili-cover ~/.claude/skills/
cp -R xb-cover-skills/xb-xhs-cover ~/.claude/skills/
```

如果已经安装同名 Skill，请先备份并手动合并规则，避免直接覆盖。如果 Codex 的 `~/.codex/skills` 已映射到 `~/.claude/skills`，无需重复复制；其他环境请放入对应的 Skill 发现目录。

### 使用示例

```text
使用 xb-xhs-cover，为这篇 AI 工具教程制作封面。
标题：把重复工作交给 AI
请先向我索要个人照片与想要的风格，再逐步确认构图。
```

```text
使用 xb-blibili-cover，把已确认的小红书封面重排为 16:9 B 站封面。
保留标题和素材身份，双截图对比，真人在右侧。
```

建议提供：主题或脚本、准确标题、真人照片，以及需要使用的截图或 Logo。缺少输入时 Skill 会继续确认。横竖版转换需要重新排版，不能只裁切或补边。

### 素材与隐私

- 仓库不包含私人照片、照片索引、使用记录或含真人的测试图片。
- 开始时先提供自己的照片及想要的风格；不会自动读取作者或相邻 Skill 的照片库。
- 照片默认仅用于当前任务，不自动收录、保存索引或使用历史。长期保存需你明确要求并指定位置。
- 仅使用你有权使用的照片、截图和 Logo。生成式工具可能改变脸、手或界面细节；要求像素保真时，应使用原图合成能力并核验结果。

### 目录

```text
xb-blibili-cover/
  SKILL.md
  references/       # 横版案例规则与提示词（原始图片不分发）
xb-xhs-cover/
  SKILL.md
  agents/openai.yaml
  references/       # 卡通图标、贴纸与密度规范
```

参考案例使用占位内容，不含作者的外貌、服装或角色设定，也不预填效果百分比。

## English

### Included skills

| Skill | Purpose | Suggested canvas |
| --- | --- | --- |
| [xb-blibili-cover](xb-blibili-cover/SKILL.md) | Bilibili covers with screenshot comparisons, workflows, logos, and layouts adapted from Xiaohongshu covers | 16:9 at 1920×1080; 4:3 at 1440×1080 |
| [xb-xhs-cover](xb-xhs-cover/SKILL.md) | Xiaohongshu covers starting with your portrait and desired style, followed by layout decisions and an optional personal avatar | 3:4 at 1080×1440 |

These dimensions are design recommendations, not mandatory platform requirements. The original spelling `xb-blibili-cover` is intentional. Skill instructions and reference prompts are written in Chinese; this README provides English onboarding.

### Visual style

Start by providing your own portrait and desired style, using a description or reference image. Your style takes priority; the sticker collage below is optional. A cartoon avatar is also optional and must be based only on your portrait. The author’s portrait and cartoon character are never used.

Warm cream backgrounds, bold dark-brown titles, selective yellow highlights, sage-green hand-drawn lines, and clean paper-sticker cards. Real photographs establish identity; screenshots and logos supply evidence. Both skills include a cartoon avatar only if you choose one, based on your own portrait.

### Installation

You need an AI assistant that discovers local `SKILL.md` files and an available image generation or editing tool. This repository contains workflows and prompts, not an image API, model, or API key. It does not install image tools automatically.

```bash
git clone https://github.com/Iris-lover/xb-cover-skills.git
mkdir -p ~/.claude/skills
cp -R xb-cover-skills/xb-blibili-cover ~/.claude/skills/
cp -R xb-cover-skills/xb-xhs-cover ~/.claude/skills/
```

Back up and merge any existing skills with the same names before copying. If Codex’s `~/.codex/skills` already points to `~/.claude/skills`, no second copy is needed. For other assistants, use their configured skill discovery directory.

### Examples

```text
Use xb-xhs-cover to design a cover for this AI tutorial.
Title: 把重复工作交给 AI
First ask me for my own portrait and desired style, then confirm the layout step by step.
```

```text
Use xb-blibili-cover to adapt the approved Xiaohongshu cover into a 16:9 Bilibili cover.
Keep the exact title and source identities. Place the portrait on the right with two comparison screenshots.
```

Provide a topic or script, an exact title, a portrait, and any required screenshots or logos. The skills ask for missing inputs. Changing aspect ratios requires a new layout rather than cropping or adding borders.

### Assets and privacy

- Private portraits, photo catalogs, usage history, and portrait-containing test images are excluded.
- Start with your own portrait and desired style. Neither skill automatically reads the author’s or neighboring skills’ photo libraries.
- Photos are used for the current task without automatic cataloging or usage-history storage. Persistent storage requires your explicit request and a chosen location.
- Use only photos, screenshots, and logos you have permission to use. Generative tools may change faces, hands, or interface details. Use source-image compositing and verify the output when pixel fidelity is required.

### Repository structure

```text
xb-blibili-cover/
  SKILL.md
  references/       # Landscape case notes and prompt; source images excluded
xb-xhs-cover/
  SKILL.md
  agents/openai.yaml
  references/       # Cartoon icons, stickers, and density rules
```

Reference examples use placeholders without the author’s appearance, clothing, or character design, and without preset performance percentages.
