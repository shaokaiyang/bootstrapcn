|布局|标题|组|
| ------------- |:-------------:| -----:|
|docs|导航栏|组件|

导航栏是对将产品商标，导航和其他元素简单放置到一个简洁导航表头的简单包装。它很容易扩展，并且在崩溃插件的帮助下，它可以轻松地集成屏幕外的内容。

# 目录

- 将被 ToC 取代，“Contents” header {:toc} 除外。

# 基础知识

在开始使用导航栏之前，您需要知道以下几点：

- 导航栏需要一个封装的 `.navbar` 和一个配色方案的类（`.navbar-default` 或 `.navbar-inverse`）
- 在导航栏中使用多个组件时，您需要一些[对齐方式类](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#alignment)
- 导航栏和他们的内容默认为流动的。使用[可选的容器](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#containers)来限制他们的水平宽度
- 使用 `.pull-left` 和 `.pull-right` 来快速地对齐子组件
- 通过使用一个 `<nav>` 元素或者，如果使用一个更一般的元素比如 `<div>`,添加一个 `role="navigation"` 到每个导航栏来显示地标识它为用户辅助技术的标志区域

# 支持的内容

导航栏伴随对少数子组件的内置支持而来。根据您的需要从以下几点组合和搭配：

- `.navbar-brand` 为您的公司，产品或项目名称提供支持
- `.navbar-nav` 为一个全高度，轻量级的导航（包括对下拉菜单的支持）提供支持
- `.navbar-form` 为垂直居中，默认大小的输入框和按钮提供支持
- `.navbar-toggler` 为使用我们的崩溃插件和其他导航切换行为提供支持

下面是一个示例，所有的子组件包括在一个默认的，轻量的导航栏中：

{% example html %} 

[Navbar](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [Home (current)](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [Features](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [Pricing](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [About](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)

Search {% endexample %}

# 配色方案

将导航栏主题化从未如此容易，这要归功于一个简单的链接颜色修饰符类和 `background-color` 工具的结合。换句话说，您可以指定亮暗并且应用背景颜色。

下面是一些例子，来展示我们所说的内容：

[Navbar](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [Home (current)](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [Features](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#) 
- [Pricing](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [About](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)

Search [Navbar](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [Home (current)](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [Features](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [Pricing](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [About](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#) 

Search [Navbar](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [Home (current)](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [Features](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#) 
- [Pricing](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [About](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#) 

Search 
{% highlight html %} 

<!-- Navbar content --> 

<!-- Navbar content --> 

<!-- Navbar content --> {% endhighlight %}

# 容器

虽然这不是必须的，但您可以把一个导航栏封装到一个 `.container` 中来将它在一个页面居中或者添加一个仅内容居中的导航栏。

{% example html %}

[Navbar](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)

{% endexample %}

{% example html %} 

[Navbar](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#) 
{% endexample %}

# 布局

导航栏可以静态地放置(默认表现)，或固定到窗口的顶部或底部。

{% example html %}
 
[Fixed top](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#) {% endexample %}

{% example html %}
 
[Fixed bottom](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#) {% endexample %}

# 可折叠内容

我们的崩溃插件允许您使用一个 `<button>` 或 `<a>` 来切换隐藏内容。

{% example html %}

## 折叠的内容

通过导航栏标牌切换

☰ {% endexample %}

对于更复杂的导航栏模式，像在 Bootstrap v3 中所使用的，使用 `.navbar-toggleable-*` 类和 `.navbar-toggler`。这些类重写我们的响应程序来展示导航，仅当内容是为了展示的时候 
。

{% example html %} 

☰

[Responsive navbar](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [Home (current)](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#) 
- [Features](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)
- [Pricing](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#) 
- [About](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/navbar.md#)

{% endexample %}

