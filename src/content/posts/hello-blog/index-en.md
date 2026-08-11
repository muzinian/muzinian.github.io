---
title: The blog is ready
published: 2026-08-11
description: A small post that verifies bilingual content, KaTeX, Shiki, and local images.
tags: [Astro, Retypeset]
lang: en
abbrlink: hello-blog
---

This is the first post on `muzinian.github.io` and a minimal test of the content stack.

## Mathematics

Inline math $e^{i\pi}+1=0$ and display math are rendered with KaTeX:

$$
\int_{-\infty}^{\infty} e^{-x^2}\,dx = \sqrt{\pi}
$$

## Syntax highlighting

```ts
interface Post {
  title: string
  published: Date
}

const latest = (posts: Post[]) =>
  posts.toSorted((a, b) => b.published.getTime() - a.published.getTime())[0]
```

## Local images

![The post and its images are versioned together in Git](./images/local-image.svg)

The image uses a standard relative Markdown path, so it can later be migrated to R2, Cloudinary, or OSS with a script.
