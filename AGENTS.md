# 自定义 Skills

本项目的可复用 skill 放在 `.agents/skills/` 目录。任何 AI 工具都可以直接读取这些文件来获取提示词。

## Game Page Creator

根据游戏官网自动创建介绍页面。

**Skill 文件:** `.agents/skills/game-page-creator.md`

### 使用方法

直接提供域名：

> example.com

AI 会自动：
1. 访问网站了解游戏内容
2. 按现有风格创建 `/src/pages/{项目名}.astro`
3. 更新首页的 projects 列表

### 手动复制

如果 AI 没有读取到这个文件，手动复制以下提示词：

```
你是网站开发助手。根据给定的游戏官网域名：
1. 访问网站了解游戏内容
2. 参考 /src/pages/example.astro 的风格创建介绍页
3. 更新 /src/pages/index.astro 的 projects 数组

页面要求：标题下一句话描述 + bullet points，使用相同 Tailwind 样式
```
