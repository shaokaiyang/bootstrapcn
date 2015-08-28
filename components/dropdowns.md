---
布局: 文档
标题: Dropdowns
组: 组件
---

Dropdowns 是可开关的，可以展示一些链接列表甚至更多。它们可以与内嵌的 Bootstrap 的 JavaScript dropdown 插件使用。它们通过点击触发，而不是通过鼠标滑过；这是 [一个专门的设计决定。](http://markdotto.com/2012/02/27/bootstrap-explained-dropdowns/)

## 内容

* 将要被 ToC 替换, 除了 "内容" 头部。

## 例子

通过使用 `.dropdown` 将 dropdown 的触发器或者 dropdown 菜单包裹，或者一个申明了 `position: relative;` 的元素。然后增加菜单的 HTML。

{% 例子 html %}
<div class="dropdown open">
  <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenu1" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
    Dropdown
  </button>
  <div class="dropdown-menu" aria-labelledby="dropdownMenu1">
    <a class="dropdown-item" href="#">Action</a>
    <a class="dropdown-item" href="#">Another action</a>
    <a class="dropdown-item" href="#">Something else here</a>
  </div>
</div>
{% 结束例子 %}

### 按钮元素

你可以可选的使用 `<button>` 元素在你的 dropdown 里面，而不是 `<a>`。

{% 例子 html %}
<div class="dropdown open">
  <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenu2" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
    Dropdown
  </button>
  <div class="dropdown-menu" aria-labelledby="dropdownMenu2">
    <button class="dropdown-item" type="button">Action</button>
    <button class="dropdown-item" type="button">Another action</button>
    <button class="dropdown-item" type="button">Something else here</button>
  </div>
</div>
{% 结束例子 %}



## 对齐

默认情况下，一个 dropdown 菜单是自动的 100% 位于它的父亲元素的顶部和左侧。给一个  `.dropdown-menu` 增加 `.dropdown-menu-right` 来让这个 dropdown 菜单右对齐。

{% callout info %}
**注意!** Dropdown 只能只用 CSS 来定位，并且可能需要一些额外的样式来对齐。 
{% endcallout %}

{% highlight html %}
<div class="dropdown-menu dropdown-menu-right" aria-labelledby="dLabel">
  ...
</div>
{% endhighlight %}

## 菜单头部

在任何一个 dropdown 菜单里面给 label 部分增加一个头部。

{% example html %}
<div class="dropdown-menu">
  <h6 class="dropdown-header">Dropdown header</h6>
  <a class="dropdown-item" href="#">Action</a>
  <a class="dropdown-item" href="#">Another action</a>
</div>
{% endexample %}

## 菜单分隔线

通过一个分割线来让一组相关的菜单选项分组。

{% 例子 html %}
<div class="dropdown-menu">
  <a class="dropdown-item" href="#">Action</a>
  <a class="dropdown-item" href="#">Another action</a>
  <a class="dropdown-item" href="#">Something else here</a>
  <div class="dropdown-divider"></div>
  <a class="dropdown-item" href="#">Separated link</a>
</div>
{% 结束例子 %}

## 禁用菜单选项

在 dropdown 里面给选项新增 `.disabled` 来 **让它们在样式上不可用**。

{% 例子 html %}
<div class="dropdown-menu">
  <a class="dropdown-item" href="#">Regular link</a>
  <a class="dropdown-item disabled" href="#">Disabled link</a>
  <a class="dropdown-item" href="#">Another link</a>
</div>
{% 结束例子 %}

## 用法

通过数据属性或者 JavaScript，这个 dropdown 插件通过 `.open` 这个类在它的父元素中触发隐藏的内容（dropdown 菜单）。

在移动设备上，通过 `.dropdown-backdrop` 打开一个 dropdown，当在菜单外面点击的时候，给关闭 dropdown 菜单一个作为可点击的区域，这是一个支持 iOS 设备的要求。**这意味着从一个打开的 dropdown 到另外一个不同的 dropdown 菜单需要一个在移动设备上额外的点击。**

注意：这个 `data-toggle="dropdown"` 属性是在应用层作为依靠关闭 dropdown 菜单的，因此使用它总是好的。

### 使用数据属性

给一个链接或者按钮增加 `data-toggle="dropdown"` 来触发一个 dropdown。

{% highlight html %}
<div class="dropdown">
  <button id="dLabel" type="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
    Dropdown trigger
  </button>
  <div class="dropdown-menu" aria-labelledby="dLabel">
    ...
  </div>
</div>
{% endhighlight %}

要让 URLs 与链接按钮交互，使用 `data-target` 属性而不是 `href="#"`。

{% highlight html %}
<div class="dropdown">
  <a id="dLabel" data-target="#" href="http://example.com" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
    Dropdown trigger
  </a>

  <div class="dropdown-menu" aria-labelledby="dLabel">
    ...
  </div>
</div>
{% endhighlight %}

### 使用 JavaScript

通过 JavaScript 来调用 dropdown：

{% highlight js %}
$('.dropdown-toggle').dropdown()
{% endhighlight %}

{% callout info %}
#### 仍然需要 `data-toggle="dropdown"` 

不管你是通过 JavaScript 来调用 dropdown 或者使用 data-api， `data-toggle="dropdown"` 总是需要在被触发的元素上面。
{% endcallout %}

### 选项

*无*

### 方法

| 方法 | 描述 |
| --- | --- |
| `$().dropdown('toggle')` | 给一个指定的 navbar  或者 navigation 触发 dropdown 菜单。|

### 事件

所有的 dropdown 事件都是在 `.dropdown-menu`父亲元素触发的，并且都有一个 `relatedTarget` 属性，对应的值是触发开关的元素。

| Event | Description |
| --- | --- |
| `show.bs.dropdown` | 当显示事件调用的时候这个事件会立即被触发。|
| `shown.bs.dropdown` | 当 dropdown 对用户可见的时候这个事件就会被触发（会等待CSS 过渡完成）。 |
| `hide.bs.dropdown` | 当隐藏方法被调用的时候这个事件将会被触发。|
| `hidden.bs.dropdown`| 当 dropdown 已经对用户隐藏的时候这个事件会触发（会等待CSS 过渡完成）。|

{% highlight js %}
$('#myDropdown').on('show.bs.dropdown', function () {
  // do something…
})
{% endhighlight %}
