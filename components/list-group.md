list groups 是灵活而且强大的组件，不仅可以用来展示一些简单的元素列表，同样也能展示 那些有自定义内容的复杂元素。

## 内容

- 它将会被 ToC 替代，除“内容”头部之外

## 基本示例

最基本的 list group 仅仅是一个拥有列表项和适当的类的无序列表。在这基础上可以使用下列选项，或者有需要的话也可以是你自己的 CSS。

{% example html %}

- Cras justo odio
- Dapibus ac facilisis in
- Morbi leo risus
- Porta ac consectetur ac
- Vestibulum at eros

{% example html %}

## 标签

给任意 list group 项添加标签来展示一些未读的计数、活动等等。

{% example html %}

- 14 Cras justo odio
- 2 Dapibus ac facilisis in
- 1 Morbi leo risus

{% example html %}

## 链接项

通过使用锚点而非列表项来给 list group 项添加链接（同样也意味着是一个父类的 <div> 而不是 <ul>）。对每个元素周围独立的父类来说没有必要。

{% example html %}

[Cras justo odio](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/list-group.md#) [Dapibus ac facilisis in](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/list-group.md#) [Morbi leo risus](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/list-group.md#) [Porta ac consectetur ac](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/list-group.md#) [Vestibulum at eros](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/list-group.md#)
{% example html %}

## 按钮箱

list group 可能是按钮而不是列表项（同样也意味着是一个父类的 <div> 而不是 <ul>）。
对每个元素周围独立的父类来说没有必要。这里不要使用标准的 .btn 类。

{% example html %}

Cras justo odio Dapibus ac facilisis in Morbi leo risus Porta ac consectetur ac Vestibulum at eros
{% example html %}

## 禁用项

添加 .disabled 到 .list-group-item 来让它显示灰色，呈现出禁用状态。

{% example html %}

[Cras justo odio](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/list-group.md#) [Dapibus ac facilisis in](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/list-group.md#) [Morbi leo risus](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/list-group.md#) [Porta ac consectetur ac](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/list-group.md#) [Vestibulum at eros](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/list-group.md#)
{% example html %}

## 自定义内容

几乎在任何的 HTML 中都有，即使是像下列链接的 list groups。

{% example html %}

### List group 项标题

Donec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius blandit.

### List group 项标题

Donec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius blandit.

### List group 项标题

Donec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius blandit.

{% example html %}

