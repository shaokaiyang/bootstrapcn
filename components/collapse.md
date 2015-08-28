---
布局: 文档
标题: 折叠板
组: 组件
---

Bootstrap 折叠插件允许你在你的页面上使用少量 JavaScript 和一些类来打开或者关闭内容。一个利用少量类的可以具有开关功能的灵活的插件 (来自 **必要的 [过渡插件]({{ site.baseurl }}/components/transitions/)**)。

## 内容

* 将要被 ToC 替换, 除了 "内容" 头部。

## 例子

点击下面的按钮通过改变类来展示和隐藏其他元素。

- `.collapse` 隐藏内容
- `.collapsing` 在过渡的时候用到
- `.collapse.in` 展示内容

你可以使用 `href` 这个属性来使用链接，或者使用 `data-target` 属性来使用按钮。在这两个类里面，都需要 `data-toggle="collapse"` 这个类。

{% 例子 html %}
<p>
  <a class="btn btn-primary" data-toggle="collapse" href="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
    Link with href
  </a>
  <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
    Button with data-target
  </button>
</p>
<div class="collapse" id="collapseExample">
  <div class="card card-block">
    Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident.
  </div>
</div>
{% 结束例子 %}

## 手风琴例子

通过扩展默认的的折叠行为来创建一个手风琴。

{% 例子 html %}
<div id="accordion" role="tablist" aria-multiselectable="true">
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingOne">
      <h4 class="panel-title">
        <a data-toggle="collapse" data-parent="#accordion" href="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
          Collapsible Group Item #1
        </a>
      </h4>
    </div>
    <div id="collapseOne" class="panel-collapse collapse in" role="tabpanel" aria-labelledby="headingOne">
      Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.
    </div>
  </div>
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingTwo">
      <h4 class="panel-title">
        <a class="collapsed" data-toggle="collapse" data-parent="#accordion" href="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
          Collapsible Group Item #2
        </a>
      </h4>
    </div>
    <div id="collapseTwo" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwo">
      Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.
    </div>
  </div>
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingThree">
      <h4 class="panel-title">
        <a class="collapsed" data-toggle="collapse" data-parent="#accordion" href="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
          Collapsible Group Item #3
        </a>
      </h4>
    </div>
    <div id="collapseThree" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingThree">
      Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod. Brunch 3 wolf moon tempor, sunt aliqua put a bird on it squid single-origin coffee nulla assumenda shoreditch et. Nihil anim keffiyeh helvetica, craft beer labore wes anderson cred nesciunt sapiente ea proident. Ad vegan excepteur butcher vice lomo. Leggings occaecat craft beer farm-to-table, raw denim aesthetic synth nesciunt you probably haven't heard of them accusamus labore sustainable VHS.
    </div>
  </div>
</div>
{% 结束例子 %}

## 易用性

请务必给控件元素增加 `aria-expanded` 这个类。这个属性给现代屏幕阅读器或者类似的辅助技术明确的定义了折叠元素当前的状态。如果这个折叠元素是默认关闭的，那么它将会有一个 `aria-expanded="false"` 属性。如果你想这个折叠元素默认情况下是打开的，那么在控件上设置 `aria-expanded="true"` 即可。不管这个折叠的元素是打开还是关闭的，这个插件将会自动的开关。

此外，如果你的控件只是想简单的要一个开关效果－比如这个 `data-target` 属性与一个 `id` 选择器绑定，那么只需要将这个 `id` 包含在折叠元素里面。现代屏幕阅读器或者类似的辅助技术充分利用这个属性来给用户提供额外的直接在导航的折叠元素之间导航的捷径。

## 用法

这个折叠插件使用了一些类来处理折叠行为：

- `.collapse` 隐藏内容
- `.collapse.in` 展示内容
- `.collapsing` 当过渡开始的时候被加上，当过渡结束的时候被移除

这些类可以在 `_animation.scss` 找到。

### 通过数据属性

只需要增加 `data-toggle="collapse"` 并且一个 `data-target` 就可以自动的让这个元素成为可折叠元素。这个 `data-target` 属性接受一个 CSS 选择器来执行这个折叠。务必给这个折叠的元素增加 `collapse` 这个类。如果你想默认情况下是开着的，那么只需要额外的增加 `in` 这个类。

给一个可折叠控件增加一个类似手风琴的效果，只需要增加 `data-parent="#selector"`这个属性。可以参考在这个实践中的例子。

### 通过 JavaScript

手动开启:

{% highlight js %}
$('.collapse').collapse()
{% endhighlight %}

### 选项

选项可以通过数据属性或者 JavaScript 来传递。对于数据属性，在选项名前面加上 `data-`，比如 `data-parent=""`。

<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
     <tr>
       <th style="width: 100px;">名称</th>
       <th style="width: 50px;">类型</th>
       <th style="width: 50px;">默认值</th>
       <th>描述</th>
     </tr>
    </thead>
    <tbody>
     <tr>
       <td>parent</td>
       <td>selector</td>
       <td>false</td>
       <td>如果提供了一个选择器，那么当可折叠元素打开的时候，在特定的父元素里面所有可以折叠的元素都将会被关闭。（有一点像传统的手风琴行为－这个由 <code>panel</code> 来决定）</td>
     </tr>
     <tr>
       <td>toggle</td>
       <td>boolean</td>
       <td>true</td>
       <td>调用的时候触发可折叠元素</td>
     </tr>
    </tbody>
  </table>
</div>

### 方法

#### .collapse(options)

将你的元素激活为一个可折叠元素。接收一个可选的参数 `object`。

{% highlight js %}
$('#myCollapsible').collapse({
  toggle: false
})
{% endhighlight %}

#### .collapse('toggle')

触发一个可折叠元素打开或者关闭。

#### .collapse('show')

展示一个可折叠元素。

#### .collapse('hide')

隐藏一个可折叠元素。

### 事件

Bootstrap 的给绑定折叠功能提供了一些事件。

<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
     <tr>
       <th style="width: 150px;">事件类型</th>
       <th>描述</th>
     </tr>
    </thead>
    <tbody>
     <tr>
       <td>show.bs.collapse</td>
       <td>当 <code>show</code> 方法被调用的时候这个事件将会触发。</td>
     </tr>
     <tr>
       <td>shown.bs.collapse</td>
       <td>当可折叠元素对用户可见的时候这个事件将会触发（将会等待 CSS 过渡完成）。</td>
     </tr>
     <tr>
       <td>hide.bs.collapse</td>
       <td>当 <code>hide</code> 事件被调用的时候这个事件将会被立即触发。       </td>
     </tr>
     <tr>
       <td>hidden.bs.collapse</td>
       <td>当一个可折叠元素对读者隐藏的时候这个事件就会触发（将会等待 CSS 过渡完成）。</td>
     </tr>
    </tbody>
  </table>
</div>

{% highlight js %}
$('#myCollapsible').on('hidden.bs.collapse', function () {
  // do something…
})
{% endhighlight %}
