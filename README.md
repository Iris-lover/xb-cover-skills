# XB Cover Skills

真人实拍 × 手绘贴纸拼贴的封面设计 Skill，适用于 AI 工具、设计教程、工作流、推荐与测评。

[中文](#中文) · [English](#english)

## 中文

### 包含的 Skill

| Skill | 用途 | 建议画幅 |
| --- | --- | --- |
| [xb-blibili-cover](xb-blibili-cover/SKILL.md) | B 站横版封面；支持截图对比、流程、Logo，以及从小红书封面重排 | 16:9，1920×1080；4:3，1440×1080 |
| [xb-xhs-cover](xb-xhs-cover/SKILL.md) | 小红书封面；逐步确认标题、真人、信息结构和同源 Q 版小人物 | 3:4，1080×1440 |

以上尺寸是设计建议，并非平台强制规格。`xb-blibili-cover` 的名称保留原拼写。

### 视觉风格

奶油暖白底、深棕粗标题、局部暖黄高亮、鼠尾草绿手绘线与简洁纸贴信息卡。真人照片承担人物身份，截图和 Logo 提供内容证据。小红书封面配合一个与真人同源的 Q 版小人物；B 站封面默认不添加。

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
我会提供真人照片和产品截图，请先逐步确认构图。
```

```text
使用 xb-blibili-cover，把已确认的小红书封面重排为 16:9 B 站封面。
保留标题和素材身份，双截图对比，真人在右侧。
```

建议提供：主题或脚本、准确标题、真人照片，以及需要使用的截图或 Logo。缺少输入时 Skill 会继续确认。横竖版转换需要重新排版，不能只裁切或补边。

### 素材与隐私

- 仓库不包含私人照片、照片索引、使用记录或含真人的测试图片。
- 首次使用请提供自己的照片。可选择仅在本地维护 `xb-xhs-cover/assets/photos/catalog.json`；照片条目应提供相对索引目录的路径，并在使用前查看原图。无需建立照片库也能使用。
- B 站 Skill 可以读取相邻小红书 Skill 的本地照片库。照片目录已被 Git 忽略，请勿使用强制添加上传私人素材。
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

参考案例中的标题和“还原度 98%”只属于该案例；该数字来自用户表述，不代表测量结果或效果保证。

## English

### Included skills

| Skill | Purpose | Suggested canvas |
| --- | --- | --- |
| [xb-blibili-cover](xb-blibili-cover/SKILL.md) | Bilibili covers with screenshot comparisons, workflows, logos, and layouts adapted from Xiaohongshu covers | 16:9 at 1920×1080; 4:3 at 1440×1080 |
| [xb-xhs-cover](xb-xhs-cover/SKILL.md) | Xiaohongshu covers with step-by-step decisions about titles, portraits, content structure, and a matching cartoon character | 3:4 at 1080×1440 |

These dimensions are design recommendations, not mandatory platform requirements. The original spelling `xb-blibili-cover` is intentional. Skill instructions and reference prompts are written in Chinese; this README provides English onboarding.

### Visual style

Warm cream backgrounds, bold dark-brown titles, selective yellow highlights, sage-green hand-drawn lines, and clean paper-sticker cards. Real photographs establish identity; screenshots and logos supply evidence. Xiaohongshu covers include one small cartoon character based on the portrait. Bilibili covers omit it by default.

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
I will provide a portrait and product screenshots. Confirm the layout step by step first.
```

```text
Use xb-blibili-cover to adapt the approved Xiaohongshu cover into a 16:9 Bilibili cover.
Keep the exact title and source identities. Place the portrait on the right with two comparison screenshots.
```

Provide a topic or script, an exact title, a portrait, and any required screenshots or logos. The skills ask for missing inputs. Changing aspect ratios requires a new layout rather than cropping or adding borders.

### Assets and privacy

- Private portraits, photo catalogs, usage history, and portrait-containing test images are excluded.
- Supply your own portrait on first use. Optionally keep a local catalog at `xb-xhs-cover/assets/photos/catalog.json`, using image paths relative to that catalog and inspecting source photos before selection. A photo library is optional.
- The Bilibili skill can read the neighboring Xiaohongshu skill’s local photo library. Photo directories are ignored by Git; do not force-add private assets.
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

The sample titles and “98% fidelity” tag apply only to the reference case. That percentage was supplied by the user; it is not a measured result or a performance guarantee.
