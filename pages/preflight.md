## 预检 ( Preflight )

[Tailwind CSS Preflight](https://tailwindcss.com/docs/preflight) 是 Tailwind 项目的一组固执己见的基本样式。

它们是在所有其他样式之前应用的，作用时重置不同浏览器中的样式，以确保在浏览器之间获得一致的体验。

```css
@tailwind base; /* Preflight will be injected here */
@tailwind components;
@tailwind utilities;
```

UnoCSS 默认情况下不提供样式重置或预检，但提供了丰富的样式重置预设 [Unocss Browser Style Reset](https://unocss.dev/guide/style-reset#browser-style-reset)。
