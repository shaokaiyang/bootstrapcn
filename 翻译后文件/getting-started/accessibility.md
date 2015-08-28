<table data-table-type="yaml-metadata">
  <thead>
  <tr>
  <th>布局</th>

  <th>标题</th>

  <th>分组</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div>文档</div></td>

  <td><div>辅助功能</div></td>

  <td><div>入门教程</div></td>
  </tr>
  </tbody>
</table>

Bootstrap 遵循普通的 web 标准和 — — 用最少的额外付出 — — 可以用来创建那些使用 AT 访问的网站。

# 组件要求 #

一些常见的 HTML 元素都需要支持通过角色和 Aria 特性来实现基本辅助功能增强。下面是列出了一些最常用的。

{%callout info %}**当心！**当我们检查阿尔法的时候，我们就会在这里移动更多的带有从文档的其他区域链接到特定区域的辅助功能备注。{%endcallout %}

# 按钮组 #

为了使辅助技术 — — 如屏幕阅读器 — — 传达一系列按钮已经被分组了，需要提供适当的 role 属性。对于按钮组，这将是 `role="group"`，而工具栏应该有一个 `role="toolbar".`。

此外，组和工具栏应该被给予明确的标签，因为尽管存在正确的 `role` 属性，但是大多数辅助技术不会申明它们。在此处提供的示例中，我们使用 `aria-label` 标签，但也可以使用替代品如 `aria-labelledby` 。

# Skip 导航 #

如果您的导航包含很多链接，并且需要在 DOM 中的主要内容之前显示，在导航之前添加一个 `Skip 链接`(一个简单的解释，请参阅本文 [A11Y 项目上 skip 导航链接](http://a11yproject.com/posts/skip-nav-links/))。使用 `.sr-only` 类会从视觉上隐藏 `skip` 链接，然后 `.sr-only-focusable` 类将确保链接变得可见当获取焦点的时候。 (针对视力正常的键盘用户)。

由于 Chrome 和 Internet Explorer 长期存在的一些错误和问题（请分别参见 [Chromium bug 追踪器中的问题 262171](https://code.google.com/p/chromium/issues/detail?id=262171) 和这篇文章关于在页面的[链接和焦点顺序的部分](http://accessibleculture.org/articles/2010/05/in-page-links/)），您将需要确保您的 skip 链接的目标至少是以编程方式通过添加 tabindex ="-1"来设置焦点的。

此外，您可能想要显式地压制在带有 `#content:focus { outline: none; }`的目标上的可见焦点指示 （特别是 Chrome 在单击鼠标时，目前也会让 `tabindex ="-1"` 来在元素上设置焦点。）。

请注意，此 bug 也会影响任何其他您的网站可能使用的页面链接，对键盘用户而言，就会使他们变得无用。你可能会考虑将类似的权宜之计修复程序添加到所有其他名为 anchors / fragment  的作为链接目标的标识符中。{%endcallout %}。

{% highlight html %} [跳转到主要内容](https://github.com/yangxuanxc/bootstrapcn/blob/master/getting-started/accessibility.md#content) ...

<!-- The main page content -->
{% endhighlight %}

# 嵌套的标题 #

当嵌套标题为 (`<h1>` - `<h6>`)，您文档的主要标题应该是`<h1>`。随后的标题应该逻辑利用`<h2>`-`<h6>`，这样屏幕阅读器可以为您的网页内容构建一个表。

了解更多关于 [HTML CodeSniffer](http://squizlabs.github.io/HTML_CodeSniffer/Standards/Section508/) 和[宾夕法尼亚州立大学](http://accessibility.psu.edu/headings)的内容请点击。

# 更多的资源 #

- ["HTML Codesniffer"书签用于标识辅助功能问题
](https://github.com/squizlabs/HTML_CodeSniffer)
- [A11Y 项目](http://a11yproject.com/)
- [MDN 辅助功能文档](https://developer.mozilla.org/en-US/docs/Accessibility)
