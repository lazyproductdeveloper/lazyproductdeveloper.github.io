# Game Page Creator

根据游戏官网自动创建介绍页面。

## 触发方式

告诉 AI：
> 帮我创建游戏介绍页：example.com

或直接提供域名即可。

## 工作流程

1. **访问网站**
   - 使用浏览器访问提供的域名
   - 了解游戏的类型、玩法、特色

2. **参考现有页面风格**
   - 参考 `/src/pages/example.astro` 的结构
   - 保持简洁风格：标题下一句话描述 + bullet points
   - 使用相同的 Tailwind 样式

3. **创建页面文件**
   - 在 `/src/pages/` 下创建 `{项目名}.astro` 文件
   - 使用 kebab-case 命名

4. **更新首页**
   - 在 `/src/pages/index.astro` 的 `projects` 数组中添加新项目
   - 格式：`{ title, description, href, link }`

## 注意事项

- description 要简洁，不超过一行
- 页面路径格式：`/项目名`
- link 为外部访问链接
