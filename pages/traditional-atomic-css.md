---
layout: two-cols-header
title: 传统的原子化 CSS
---

# 传统的原子化 CSS

### 提供**所有**可能会用到的 CSS 工具类

<img src="/traditional-atomic-css.png" bg-white alt="traditional atomic css" w-160 />

::left::

例如使用预处理器 SCSS 生成代码:

```scss
@for $i from 1 through 10 {
  .m-#{$i} {
    margin: $i / 4 rem;
  }
}
```

::right::

编译结果如下:

```css
.m-1 { margin: 0.25 rem; }
.m-2 { margin: 0.5 rem; }
/* ... */
.m-10 { margin: 2.5 rem; }
```

