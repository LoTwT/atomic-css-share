## 优势

[Tailwind CSS Utility-First Fundamentals](https://tailwindcss.com/docs/utility-first#overview) 里提及的优势:

- 不需要再浪费精力思考无意义的类名。`xxx-wrapper`。
- CSS 文件体积增长可以预期。使用原子化 CSS，一切都可以重用，很少需要编写新的 CSS。只需要承担项目中按需使用到的工具类的成本。
- 让改变更安全。CSS 是全局的，而 HTML 中的工具类是局部的，修改它们不用担心影响到全局。

对比行内样式:

- 在约束下设计。工具类可以选择设计系统中预生成的样式，能够更方便地生成一致的 UI。
- 响应式设计。不用单独写媒体查询，更方便使用。
- Hover、Focus 等状态可以通过 [state variants](https://tailwindcss.com/docs/hover-focus-and-other-states) 直接使用在元素上。

Unocss 在上述优势上提供了更好的开发体验，当你**直觉觉得**某处应该有一个工具类可以使用时，它大概率就可以直接使用。
