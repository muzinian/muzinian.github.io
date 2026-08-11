# muzinian.github.io

基于 [Astro](https://astro.build/) 和 [Retypeset](https://github.com/radishzzz/astro-theme-retypeset) 的静态博客，通过 GitHub Actions 发布到 GitHub Pages。

## 本地开发

```bash
pnpm install
pnpm dev
```

常用命令：

```bash
pnpm new-post       # 创建文章
pnpm lint           # 代码检查
pnpm build          # 类型检查并生成静态站点
pnpm preview        # 预览构建结果
pnpm update-theme   # 同步 Retypeset 更新
```

## 内容结构

```text
src/content/
├── about/
│   ├── about-zh.md
│   └── about-en.md
└── posts/
    └── hello-blog/
        ├── index-zh.md
        ├── index-en.md
        └── images/
            └── local-image.svg
```

中英文翻译使用相同的 `abbrlink`，并分别设置 `lang: zh` 和 `lang: en`。图片与文章放在同一目录中，使用标准 Markdown 相对路径引用。

## 发布

推送 `main` 分支后，`.github/workflows/deploy.yml` 会构建并发布站点。首次使用时，在 GitHub 仓库的 **Settings → Pages → Build and deployment** 中将 Source 设为 **GitHub Actions**。

## 许可证

本项目基于 MIT 许可的 Retypeset 主题构建，详见 [LICENSE](./LICENSE)。
