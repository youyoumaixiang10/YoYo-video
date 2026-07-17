# YoYo Video

把真实的亲子日常、宝宝童言和成长瞬间，制作成固定角色、手绘风格的竖屏故事视频。

本仓库包含可直接安装到 Codex 的 `family-handdrawn-story-video` Skill，以及妈妈、宝宝、爸爸、奶奶的固定角色参考图。

## 主要特点

- **先确认画面脚本，再开始制作**：完整分镜未确认前，不生成图片或视频。
- **无旁白也能看懂**：默认不生成旁白，核心事件、因果和童言通过画面文字完整呈现。
- **相邻画面逻辑连贯**：逐幕检查“起因—行动—回应—结果”，避免情节突然跳转。
- **固定家庭角色**：通过角色圣经和参考图控制年龄、发型、穿搭与人物比例。
- **自然手绘表达**：暖白纸张、手写文字、不规则对话框、克制的彩铅或水彩。
- **可执行的成片验收**：检查文字行数、人物大小、背景接缝、无意义标记、动态变化和媒体规格。

## 适合制作的内容

- 宝宝的童言童语
- 亲子沟通与情绪表达
- 家庭成员观察到的成长变化
- 值得记录的日常小事
- 小红书、视频号、抖音等平台的竖屏故事视频

## 安装

将仓库克隆到 Codex 的 Skills 目录，并使用 Skill 名称作为文件夹名：

```powershell
git clone https://github.com/youyoumaixiang10/YoYo-video.git "$env:USERPROFILE\.codex\skills\family-handdrawn-story-video"
```

也可以下载仓库 ZIP，解压后将文件夹重命名为：

```text
family-handdrawn-story-video
```

再放入 Codex 的 Skills 目录。安装或更新后，建议新开一个 Codex 任务，让 Skill 重新加载。

## 使用方式

在 Codex 中输入：

```text
请调用 family-handdrawn-story-video，把下面这段真实家庭故事整理成画面脚本。
先不要生成图片和视频，等我确认完整画面脚本后再制作。
```

然后提供真实事件、人物、关键对话和结果。信息不足时，Skill 会优先询问一个最关键的问题，不会自行补造情节。

## 工作流程

1. 提供真实家庭故事。
2. 判断是否适合拆成多条内容。
3. 输出完整的 5—7 幕画面脚本。
4. 逐幕修改并重新确认完整版本。
5. 收到“确认画面脚本，可以生成”后开始制作。
6. 检查角色、文字、动效和媒体规格。
7. 导出并验证 9:16 MP4 成片。

旁白默认关闭。只有用户明确提出并确认旁白文本后，才会生成配音。

## 目录结构

```text
.
├─ SKILL.md
├─ agents/
│  └─ openai.yaml
├─ assets/
│  └─ characters/
│     ├─ father.png
│     ├─ grandmother.png
│     └─ mother-and-child.png
└─ references/
   ├─ character-bible.md
   ├─ visual-direction.md
   ├─ storyboard-contract.md
   ├─ production-contract.md
   └─ example-story.md
```

## 核心文件

- `SKILL.md`：状态流程、制作门槛和硬性规则。
- `character-bible.md`：固定家庭角色设定。
- `visual-direction.md`：手绘字体、留白、人物比例、气泡与背景规则。
- `storyboard-contract.md`：事实完整性、无声叙事和分镜格式。
- `production-contract.md`：成片规格、动态要求与验收方法。
- `example-story.md`：七幕故事结构示例，不作为可直接复制的文案。

## 相关能力

正式制作阶段会使用以下 Codex Skills：

- `hyperframes`
- `general-video`
- `media-use`
- `imagegen`

这些能力只会在完整画面脚本获得确认后进入制作流程。

## 素材说明

仓库中的角色图片用于保持系列视频的人物一致性。未经仓库所有者明确授权，请勿将角色图用于其他人物设定、商业项目或二次分发。

本仓库目前未声明开源许可证；如需公开复用、改编或商业使用，请先联系仓库所有者。
