Modals are streamlined, but flexible, dialog prompts with the minimum required functionality and smart defaults.

## 内容

- 它将会被 ToC 替代，除“内容”头部之外

由于 HTML5 定义语意的方式，[autofocus HTML 属性](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-autofocus)在 Bootstrap modals 中没有任何影响。为了达到同样的效果，使用一些自定义的 javascript。

{% highlight js %} $('#myModal').on('shown.bs.modal', function () { $('#myInput').focus() }) {% endhighlight %}

{% callout warning %}

### 不支持打开多个 modal

记住当一个 modal 仍然可见的时候不要去打开另外一个。同时打开多个 modal 需要自定义代码。

{% callout warning %}

### modal 标记位置

在你的文档中尽量始终保持将 modal 的 HTML 代码置于一个高等级的位置上，这样可以避免其他的组件影响到 modal 的外观和/或功能。{% endcallout %}

{% callout warning %}

### 移动设备警告

这里有一些有关在移动设备上使用 modal 的警告。详情浏览[我们的浏览器支持文档](https://github.com/yangxuanxc/bootstrapcn/blob/master/components/%7B%7B%20site.baseurl%20%7D%7D/getting-started/browsers-devices/#modals-navbars-and-virtual-keyboards)。{% endcallout %}

### 静态例子

A rendered modal with header, body, and set of actions in the footer.

× 关闭

### modal 标题

一个好的 body

关闭保存更改
{% highlight html %}

× 关闭

### modal 标题

一个好的 body

关闭保存更改
{% endhighlight %} ### 通过点击下面的按钮使用 JavaScript 来触发一个 modal 的例子。它会从页面顶部滑下并慢慢淡入。
× Close

### modal 标题

### modal 中的文本

Duis mollis, est non commodo luctus, nisi erat porttitor ligula.

### modal 中的 popover

这个[按钮]( )在点击的时候可以触发 popover

### modal 中的工具提示

[这个链接]( )和[这个链接]( )在鼠标悬停的时候会有工具提示。


----------

### 溢出文本来显示滚动行为

ras mattis consectetur purus sit amet fermentum. Cras justo odio, dapibus ac facilisis in, egestas eget quam. Morbi leo risus, porta ac consectetur ac, vestibulum at eros.

Praesent commodo cursus magna, vel scelerisque nisl consectetur et. Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor.

Aenean lacinia bibendum nulla sed consectetur. Praesent commodo cursus magna, vel scelerisque nisl consectetur et. Donec sed odio dui. Donec ullamcorper nulla non metus auctor fringilla.

Cras mattis consectetur purus sit amet fermentum. Cras justo odio, dapibus ac facilisis in, egestas eget quam. Morbi leo risus, porta ac consectetur ac, vestibulum at eros.

Praesent commodo cursus magna, vel scelerisque nisl consectetur et. Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor.

Aenean lacinia bibendum nulla sed consectetur. Praesent commodo cursus magna, vel scelerisque nisl consectetur et. Donec sed odio dui. Donec ullamcorper nulla non metus auctor fringilla.

Cras mattis consectetur purus sit amet fermentum. Cras justo odio, dapibus ac facilisis in, egestas eget quam. Morbi leo risus, porta ac consectetur ac, vestibulum at eros.

Praesent commodo cursus magna, vel scelerisque nisl consectetur et. Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor.

Aenean lacinia bibendum nulla sed consectetur. Praesent commodo cursus magna, vel scelerisque nisl consectetur et. Donec sed odio dui. Donec ullamcorper nulla non metus auctor fringilla.

关闭保存更改
启动演示 modal
{% highlight html %}

启动演示 modal

× Close

### modal 标题

...
关闭保存更改
{% endhighlight %}

{% callout warning %}

### 使得 modals 可以访问

考虑到 modal 标题，将 `role="dialog"` 和 `aria-labelledby="..."` 添加到 `.modal，`将 `role="document"` 添加到 `.modal-dialog` 中去。

另外，你可以通过 `aria-describedby` 和 `.modal` 给你的 modal 对话框加个描述。{% endcallout %}

{% callout info %}

### 植入 YouTube 视频

在 modals 中植入 YouTube 视频需要使用到 Boostrap 中没有的 JavaScript 来实现自动停止重播或者其他的要求。看看这个很有帮助的 [Stack Overflow post](http://stackoverflow.com/questions/18622508/bootstrap-3-and-youtube-in-modal) 来了解更多信息。{% endcallout %}

## 可选大小

modals 有两种可选大小，通过将修饰符类放置在 `.modal-dialog` 上即可用、

大的 modal 小的 modal
{% highlight html %}

大的 modal

...
小的 modal

...
{% endhighlight %}

× Close

### 大的modal

...
× Close

### 小的modal

...

## 移除动画

对于那些只需要简单的出现而不是渐渐淡入计入视图中的 modals，可以从你的 modal 标记中移除 `.fade` 类。

{% highlight html %}

...
{% highlight html %}

## 使用栅格系统

为了在 modal 中使用 Bootstrap 的栅格系统，只需要将 `.container-fluid` 嵌套在 `.modal-body` 中，然后在这个容器中使用普通的栅格系统类。

{% example html %}

×

### modal 标题

.col-md-4
.col-md-4 .col-md-offset-4
.col-md-3 .col-md-offset-3
.col-md-2 .col-md-offset-4
.col-md-6 .col-md-offset-3
Level 1: .col-sm-9
Level 2: .col-xs-8 .col-sm-6
Level 2: .col-xs-4 .col-sm-6
关闭保存更改
启动启动演示 modal
{% endexample %}

## 基于触发按钮变化的 modal 内容

有一堆按钮触发相同的 modal，只是内容有一点不同？使用 `event.relatedTarget` 和 `HTML data-*` 属性（可能是通过 jQuery）根据被点击的按钮来改变 modal 的内容。
查看在 `relatedTarget` 上的 Modal Events 文档了解更多。

{% example html %}

打开模型 @mdo 打开模型 @fat 打开模型 @getbootstrap
× Close

### 新信息

收件人：
信息：
关闭发送信息
{% endexample %}

{% highlight js %} $('#exampleModal').on('show.bs.modal', function (event) { var button = $(event.relatedTarget) // Button that triggered the modal var recipient = button.data('whatever') // Extract info from data-* attributes // If necessary, you could initiate an AJAX request here (and then do the updating in a callback). // Update the modal's content. We'll use jQuery here, but you could use a data binding library or other methods instead. var modal = $(this) modal.find('.modal-title').text('New message to ' + recipient) modal.find('.modal-body input').val(recipient) }) {% endhighlight %}

## 不同高度的 modal

如果一个 modal 的高度在打开的时候发生了改变，你需要调用 `$('#myModal').data('bs.modal').handleUpdate()` 来重新调整滚动条出现的时候 modal 的位置。

## 使用

modal 插件可以触发要求的隐藏内容，通过数据属性或者 JavaScript。点击 modal 外的区域时，同样将 `.modal-open` 添加到 <body> 中来重写默认的滚动行为，并产生 `.modal-backdrop` 提供一个点击区域来取消显示的 modal。

### 通过数据属性

无须通过 JavaScript 便可激活 modal。在控制元素中设置 `data-toggle="modal"`，就像按钮一样，同样的还有 `data-target="#foo"` 或者 `href="#foo"` 确定一个指定的 modal 来触发。

{% highlight html %} 启动 modal {% endhighlight %}

### 通过 JavaScript

通过 id myModal 和一行 JavaScript 来调用 modal：

{% highlight js %}$('#myModal').modal(options){% endhighlight %}

## 选项

选项可以通过数据属性或者 JavaScript 来传递。对于数据属性，将选项名称添加到 `data-` 中去，就像在 `data-backdrop=""` 一样。
    <table>
    <tbody>
    <tr><td><b>名字</b></td><td><b>类型</b></td><td><b>默认</b></td><td><b>描述</b></td></tr>
    <tr><td>backdrop</td><td>布尔类型或<br>者静态字符串</td><td>true</td><td>包含一个 modal-backdrop 元素。<br/>另外，明确 backdrop 的静态，在<br>单击时 backdrop 不会关闭 modal</td></tr>
    <tr><td>keyboard</td><td>布尔类型</td><td>true</td><td>退出键按下时关闭 modal</td></tr>
    <tr><td>show</td><td>布尔类型</td><td>true</td><td>初始化时显示 modal</td></tr>
    </tbody>
    </table>

## 方法

### .modal(options)

像 modal 一样激活你的内容。可以考虑一个可选的选择 object。

{% highlight js %} $('#myModal').modal({ keyboard: false }) {% endhighlight %}

### .modal('toggle')

手动触发一个 modal。在 modal 被实际显示或者隐藏之前回到调用者那里（这就是说在 `shown.bs.modal` 或者 `hidden.bs.modal` 事件发生之前）。

{% highlight js %}$('#myModal').modal('toggle'){% endhighlight %}

### .modal('show')

手动打开一个 modal。在 modal 实际显示之前回到调用者那里（也就是说 `shown.bs.modal` 事件发生之前）

{% highlight js %}$('#myModal').modal('show'){% endhighlight %}

### .modal('hide')

手动隐藏一个 modal 在 modal 被实际隐藏之前回到调用者那里（也就是说 `hidden.bs.modal` 事件发生之前）

{% highlight js %}$('#myModal').modal('hide'){% endhighlight %}

##事件

Bootstrap 的 modal 类提供了几个事件能与 modal 功能相关联起来。所有的 modal 事件都是针对 modal 本身（也就是说在 `<div class="modal">` 中）。
    <table>
    <tbody>
    <tr><td><b>事件类型</b></td><td><b>描述</b></td></tr>
    <tr><td>show.bs.modal</td><td>这个事件在 show 实例方法被调用时立即发生。如果是被单击事件造成的，那么被单击的元素需要像事件中的 relatedTarget 属性一样可用。</td></tr>
    <tr><td>shown.bs.modal	</td><td>这个世界在 modal 对用户可见时立即发生（需要等待 CSS 过渡来完成）。如果是被单击事件造成的，那么被单击的元素需要像事件中的 relatedTarget 属性一样可用。</td></tr>
    <tr><td>hide.bs.modal</td><td>这个事件在 hide 实例方法被调用时立即发生。</td></tr>    
	<tr><td>hidden.bs.modal	</td><td>这个事件在 modal 完成向用户隐藏之后发生（需要等待 CSS 过渡来完成）。</td></tr>    
	<tr><td>loaded.bs.modal</td><td>这个事件在 modal 加载了使用 remote 选项的内容时发生。</td></tr>
    </tbody>
    </table>

{% highlight js %} $('#myModal').on('hidden.bs.modal', function (e) { // do something... }) {% endhighlight %}
