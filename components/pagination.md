|布局|标题|分组|
| ------------- |:-------------:| -----:|
|docs|分页|组件|

通过多页分页组件或简单的可选择的 Pager 为您的网站或应用程序提供分页链接

# 内容

将被 ToC 取代，"Contents" header {:toc} 除外。

# 默认分页

Rdio 提倡的简单分页，极大程度上是为了应用和搜索结果。大的块不容易被丢失，易于扩展，并且提供大的点击区域。

{% example html %}

- [« Previous](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [1](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [2](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [3](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [4](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [5](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [» Next](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)

{% endexample %}

# 禁用的和活动的状态

对不同的环境，链接是自定义的。对取消选中的链接使用 `.disabled`，`.active` 指示当前页。

{% example html %}
 
- [« Previous](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [1 (current)](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#) 
- [2](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [3](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [4](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [5](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [» Next](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)

{% endexample %}

您可以为 <span> 选择交换出活动或禁用的锚点，或者就 prev/next 箭头而言省略锚点，以此来删除单机功能同时保留样式。

{% highlight html %}

- « Previous 
- 1 (current)

{% endhighlight %}

# 分级

想要更大或更小的分页吗？为附加规格添加 `.pagination-lg`或 `.pagination-sm` 吧。

{% example html %}

- [« Previous](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [1](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [2](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [3](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [» Next](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
  
{% endexample %}

{% example html %}
 
- [« Previous](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [1](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [2](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [3](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [» Next](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
 
{% endexample %}

#  Pager 

简单分页的快速的上一个和下一个链接实现了光标记和样式。这对简单的像博客或杂志的网站来说很棒。

# 默认实例

默认情况下，Pager 会将链接居中。

{% example html %}
 
- [Previous](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [Next](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)

{% endexample %}

# 对齐的链接

或者，您可以将链接设置为左或右对齐：

{% example html %}
 
- [Older](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [Newer](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)

{% endexample %}

# 可选禁用状态

Pager 链接也使用 `.disabled` 类。

{% example html %}

- [Older](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)
- [Newer](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/pagination.md#)

{% endexample %}
