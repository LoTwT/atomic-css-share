## 预检 ( Preflight )

[Tailwind CSS Preflight](https://tailwindcss.com/docs/preflight) 是 Tailwind 项目的一组固执己见的基本样式。

它们是在所有其他样式之前应用的，作用时重置不同浏览器中的样式，以确保在浏览器之间获得一致的体验。

Preflight 也会预生成一些 CSS 变量以便 utilities 能够符合 CSS 工作原理从而正常生效。

```css
@tailwind base; /* Preflight will be injected here */
@tailwind components;
@tailwind utilities;
```

UnoCSS 默认情况下不提供样式重置或预检，但提供了丰富的样式重置预设 [Unocss Browser Style Reset](https://unocss.dev/guide/style-reset#browser-style-reset)。

UnoCSS 预生成的 Preflight Variables 是由 `preset-mini` 提供的，可以在 `preset-uno` 中配置 `presetUno({ preflight: false })` 关闭。

`Tailwind Preflight` = `Unocss Preflight` + `Unocss Style Reset`
