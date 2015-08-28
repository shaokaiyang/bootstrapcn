<table>
<tbody>
<tr><td><em>类别</em></td><td><em>标题</em></td><td><em>群组</em></td></tr>
<tr><td>说明文档</td><td>警报</td><td>组件</td></tr>
</tbody>
</table>

为一些用户的典型操作中出现的可用的和灵活的警报消息提供上下文相关的反馈信息。

## 内容

* 将被替换为 ToC,不包括标题“内容”  
{:toc}

## 示例

警报可供任何长度的文本以及可选的撤回按钮使用。为了适当的格式，使用上下文类中四个**required**之一(例如，'.alert-success ')。对于内联撤回，使用 [alerts jQuery plugin](#dismissing)。

{% example html %}
<div class="alert alert-success" role="alert">
  <strong>Well done!</strong> You successfully read this important alert message.
</div>
<div class="alert alert-info" role="alert">
  <strong>Heads up!</strong> This alert needs your attention, but it's not super important.
</div>
<div class="alert alert-warning" role="alert">
  <strong>Warning!</strong> Better check yourself, you're not looking too good.
</div>
<div class="alert alert-danger" role="alert">
  <strong>Oh snap!</strong> Change a few things up and try submitting again.
</div>
{% endexample %}

### 链接颜色

在任何警报信息之中，使用 `.alert-link` 实用程序类来快速匹配链接的颜色。

{% example html %}
<div class="alert alert-success" role="alert">
  <strong>Well done!</strong> You successfully read <a href="#" class="alert-link">this important alert message</a>.
</div>
<div class="alert alert-info" role="alert">
  <strong>Heads up!</strong> This <a href="#" class="alert-link">alert needs your attention</a>, but it's not super important.
</div>
<div class="alert alert-warning" role="alert">
  <strong>Warning!</strong> Better check yourself, you're <a href="#" class="alert-link">not looking too good</a>.
</div>
<div class="alert alert-danger" role="alert">
  <strong>Oh snap!</strong> <a href="#" class="alert-link">Change a few things up</a> and try submitting again.
</div>
{% endexample %}

### 撤回

使用警报的 JavaScript 插件，就有可能撤回任何内联警报。这里就是操作步骤：

-确保你已经加载警报插件或已编译的引导 JavaScript。
-添加撤回按钮和 `.alert-dismissible` 类，该类添加额外填充右侧的警报，并置于  `.close`  按钮。
-在撤回按钮上，添加 `data-dismiss="alert"` 属性，触发 JavaScript 功能。一定要在所有设备上用适当的方式使用 `<button>` 元素。
-当撤回他们时，进行动画警报，一定要添加的 `.fade` 和 `.in` 类。

你可以看到这些在现场操作演示中：

{% example html %}
<div class="alert alert-warning alert-dismissible fade in" role="alert">
  <button type="button" class="close" data-dismiss="alert" aria-label="Close">
    <span aria-hidden="true">&times;</span>
    <span class="sr-only">Close</span>
  </button>
  <strong>Holy guacamole!</strong> You should check in on some of those fields below.
</div>
{% endexample %}

## JavaScript 行为

### 触发器

通过 JavaScript 来撤回一个警告：

{% highlight js %}
$(".alert").alert()
{% endhighlight %}

或用 `data` 按钮上的属性 **within the alert**, 如上所述：

{% highlight html %}
<button type="button" class="close" data-dismiss="alert" aria-label="Close">
  <span aria-hidden="true">&times;</span>
  <span class="sr-only">Close</span>
</button>
{% endhighlight %}

请注意，关闭警报将会从 DOM 中移除。

### 方法
| 方法 | 描述 |
| --- | --- |
| `$().alert()` | 设置一个单击事件警报用于对含有 `data-dismiss="alert"` 属性的子代元素的侦听，(不需要使用数据 data-api's 自动初始化时)。|
| `$().alert('close')` | 关闭警报通过从 DOM 中移除它，如果 `.fade` 和 `.in` 类在元素上有所体现，警报将会淡出在它被移除之前。 |

{% highlight js %}$(".alert").alert('close'){% endhighlight %}

### 事件

当连接警报功能时，引导的警报插件会暴露一些事件。

| 事件 | 描述 |
| --- | --- |
| `close.bs.alert` | 当 <code>close</code> 中的实例方法被调用，这个事件立即被触发。 |
| `closed.bs.alert` | 当警报已经被关闭，这个事件立即被触发 (将会等待 CSS 转换完成). |

{% highlight js %}
$('#myAlert').on('closed.bs.alert', function () {
  // do something…
})
{% endhighlight %}
