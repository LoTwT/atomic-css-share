---
layout: two-cols
---

<img src="/traditional-atomic-css.png" bg-white alt="traditional-atomic-css" />

<br />

1. 开发时预生成的工具类冗余
   - 开发和生产的产物不一致
   - 开发时生成的 CSS 体积过大影响加载速度和调试
1. 开发时无法预知所有可能用到的工具类
1. 生产构建时需要额外剔除冗余工具类

::right::

<img src="/on-demand-atomic-css.png" bg-white alt="on-demand-atomic-css" />

<br />

1. 预先扫描源代码，只生成使用到的工具类 ( 按需 )
1. 可以灵活地实现预生成无法实现的动态需求
1. 节约了额外的计算开销和传输成本
1. 开发和生产的产物一致
1. 方便缓存和增量构建，使得 HMR 更高效
1. 更好的 DX ( 开发体验 )

