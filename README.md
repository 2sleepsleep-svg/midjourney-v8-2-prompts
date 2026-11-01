# Image Prompt Suite · AI 生图提示词套件

面向 Midjourney、Nano Banana Pro 与 GPT Image 的 agent skill。根据模型选择写法，明确参考图职责，提供可复制提示词和中文逐句对照。

## 一条命令安装

安装环境需有 Node.js 和 Git。通过 [Skills CLI](https://github.com/vercel-labs/skills) 安装到当前环境已检测到的 agent，`-g` 表示跨项目使用：

```sh
npx --yes skills add 2sleepsleep-svg/image-prompt-suite --skill image-prompt-suite -g -y
```

指定某个 agent 时，增加 `-a codex`、`-a claude-code` 或 `-a cursor`。需要多个时可重复 `-a`。不支持符号链接的环境可加 `--copy`。若只希望当前项目使用，去掉 `-g`。

已有同名技能且包含本地修改时，先备份并比较差异，再更新。通过 Skills CLI 管理的安装可执行：

```sh
npx --yes skills update image-prompt-suite -g -y
```

命令行为和运行环境要求以 [Skills CLI 官方安装说明](https://github.com/vercel-labs/skills/blob/main/docs/commands.md) 为准。安装后按目标 agent 的要求重新加载技能。

## 一键下载完整包

- [下载最新版本 ZIP](https://github.com/2sleepsleep-svg/image-prompt-suite/archive/refs/heads/main.zip)
- [浏览技能入口](SKILL.md)

手动安装时解压完整 ZIP，将仓库根目录命名为 `image-prompt-suite`，放入目标 agent 的技能目录。`SKILL.md` 与 `references/` 必须一并保留，不要只下载单个入口文件。

## 用法

> 使用 image-prompt-suite，为一个窗边人物镜头编写 Midjourney 提示词，附中文逐句对照。

> 使用 image-prompt-suite，根据人物和场景参考，为 GPT Image 编写局部替换提示词，明确改动项与保留项。

## 文件导航

- [技能入口与交付规则](SKILL.md)
- [Midjourney 写法](references/midjourney-v8-2.md)
- [Nano Banana Pro 写法](references/nano-banana-pro.md)
- [GPT Image 写法](references/gpt-image-2.md)
- [Midjourney 参数兼容性](references/parameters.md)
- [题材模板](references/templates.md)
- [创建者参考偏好](references/creator-reference-preferences.md)

## 适用边界与版本恢复

本仓库提供提示词方法与参考记录，不自动调用生成服务。模型版本、参数和入口能力可能变化，使用时按实际平台核验；文档检查不等同于模型出图验证。创建者偏好中的具体项目要求只适用于相应项目。

每次更新保留 Git 历史；`backup-before-*` 标签可用于浏览或下载更新前版本。需要恢复时创建恢复提交，不覆盖历史。最新更新日期：2026-11-01。
