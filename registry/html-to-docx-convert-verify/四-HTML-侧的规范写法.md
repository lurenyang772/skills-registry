## 四、HTML 侧的规范写法

```html
<section role="cover" class="report-cover"> ... </section>
<section role="body" data-page-restart="1">
  <nav class="doc-toc" aria-label="文档目录">
    <p class="toc-title">目录</p>
    <ol>
      <li><a href="#sec1">一、结论先行</a></li>
      <li><a href="#sec2">二、对手方画像</a></li>
      <!-- 编号写进链接文本：列表渲染不会自动编号 -->
    </ol>
  </nav>
  ...
  <h2 id="sec1">一、结论先行</h2>
</section>
```

- 页脚/封面抑制靠 CSS Paged Media：
  ```css
  @page { @bottom-center { content: counter(page); } }
  @page cover { @bottom-center { content: none; } }
  section[role="cover"] { page: cover; }
  ```
  这套写法**只有在分节成功时才有意义**（见上文契约 2）。
- 间距一律走 `var(--spacing-*)`，别写裸值（设计令牌门禁会拦）。

