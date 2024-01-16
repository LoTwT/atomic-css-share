---
layout: two-cols-header
---

# 使用

以 Unocss 为例。如何配置请查阅 [Unocss Integrations](https://unocss.dev/integrations/)

::left::

## 基本使用

```html
<div class="text-lg font-bold underline">Some Text</div>
```

编译结果:

```css
.text-lg,
[text-lg=""] {
  font-size: 1.125rem;
  line-height: 1.75rem;
}
.underline,
[underline=""] {
  text-decoration-line: underline;
}
.bg-red,
/* for presetAttributify */
[bg-red=""] {
  --un-bg-opacity: 1;
  background-color: rgb(248 113 113 / var(--un-bg-opacity));
}
```

::right::

## `@apply` 复用

配置 [Directives Transformer](https://unocss.dev/transformers/directives)，使用 `@apply` 指令，别名 `--at-apply`、`--uno-apply`、`--uno`。

```css
.reuse-with-apply {
  @apply text-lg font-bold underline;
  /* same in Unocss */
  /* --at-apply: text-lg font-bold underline; */
}
```
