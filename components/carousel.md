---
布局: 文档
标题: 旋转木马
组: 组件
---

一个可以让元素－图片或者文本幻灯片－滚动的组件，就像一个旋转木马一样。**嵌套的旋转木马将不再被支持。**

## 内容

* 将要被 ToC 替换, 除了 "内容" 头部。

## 例子

{% 例子 html %}
<div id="carousel-example-generic" class="carousel slide" data-ride="carousel">
  <ol class="carousel-indicators">
    <li data-target="#carousel-example-generic" data-slide-to="0" class="active"></li>
    <li data-target="#carousel-example-generic" data-slide-to="1"></li>
    <li data-target="#carousel-example-generic" data-slide-to="2"></li>
  </ol>
  <div class="carousel-inner" role="listbox">
    <div class="carousel-item active">
      <img data-src="holder.js/900x500/auto/#777:#555/text:First slide" alt="First slide">
    </div>
    <div class="carousel-item">
      <img data-src="holder.js/900x500/auto/#666:#444/text:Second slide" alt="Second slide">
    </div>
    <div class="carousel-item">
      <img data-src="holder.js/900x500/auto/#555:#333/text:Third slide" alt="Third slide">
    </div>
  </div>
  <a class="left carousel-control" href="#carousel-example-generic" role="button" data-slide="prev">
    <span class="icon-prev" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="right carousel-control" href="#carousel-example-generic" role="button" data-slide="next">
    <span class="icon-next" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>
{% 例子结束 %}

{% 插图编号警告 %}
#### 在 Internet Explorer 9 过渡动画将不再被支持

Bootstrap 专门使用为它的动画使用 CSS3，但是 Internet Explorer 9 并不支持必要的 CSS 属性。因此，当使用这个浏览器的时候将不会再有滑动的过渡动画。我们专门决定不引用基于 jQuery 的兼容动画。
{% 结束插图编号 %}

{% 插图编号警告 %}
#### 需要初始化活跃的元素

`.active` 这个类需要给其中的某一个幻灯片加上，否则，旋转木马将不会被显示。
{% 结束插图编号 %}

### 可选项

在任何 `.carousel-item` 里面你都可以轻松的通过使用 `.carousel-caption` 来给你的幻灯片加上说明文字。在那里面加上任何可选的 HTML，都将自动的对齐和格式化。

<div class="bd-example">
  <div id="carousel-example-captions" class="carousel slide" data-ride="carousel">
    <ol class="carousel-indicators">
      <li data-target="#carousel-example-captions" data-slide-to="0" class="active"></li>
      <li data-target="#carousel-example-captions" data-slide-to="1"></li>
      <li data-target="#carousel-example-captions" data-slide-to="2"></li>
    </ol>
    <div class="carousel-inner" role="listbox">
      <div class="carousel-item active">
        <img data-src="holder.js/900x500/auto/#777:#777" alt="First slide image">
        <div class="carousel-caption">
          <h3>First slide label</h3>
          <p>Nulla vitae elit libero, a pharetra augue mollis interdum.</p>
        </div>
      </div>
      <div class="carousel-item">
        <img data-src="holder.js/900x500/auto/#666:#666" alt="Second slide image">
        <div class="carousel-caption">
          <h3>Second slide label</h3>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
      </div>
      <div class="carousel-item">
        <img data-src="holder.js/900x500/auto/#555:#555" alt="Third slide image">
        <div class="carousel-caption">
          <h3>Third slide label</h3>
          <p>Praesent commodo cursus magna, vel scelerisque nisl consectetur.</p>
        </div>
      </div>
    </div>
    <a class="left carousel-control" href="#carousel-example-captions" role="button" data-slide="prev">
      <span class="icon-prev" aria-hidden="true"></span>
      <span class="sr-only">Previous</span>
    </a>
    <a class="right carousel-control" href="#carousel-example-captions" role="button" data-slide="next">
      <span class="icon-next" aria-hidden="true"></span>
      <span class="sr-only">Next</span>
    </a>
  </div>
</div>

{% 高亮 html %}
<div class="carousel-item">
  <img src="..." alt="...">
  <div class="carousel-caption">
    <h3>...</h3>
    <p>...</p>
  </div>
</div>
{% 结束高亮 %}

{% 插图编号警告 %}
#### 易用性问题

这个旋转木马组件通常与易用性原则不冲突。如果你需要服从，请考虑展示你的内容的其他选择。
{% 结束插图编号 %}

## 用法

### 多个旋转木马

旋转木马需要在最外面的容器上使用一个 `id`（这个 `.carousel` ）来让旋转木马控件正常工作。当新增多个幻灯片的时候，或者当改变转转木马的 `id` 的时候，务必更新与其相关的控件。

### 使用数据属性

使用数据属性来轻松的控制旋转木马的位置。`data-slide` 接受 `prev` 或者 `next` 这两个可以改变幻灯片当前位置的关键字。另外，使用 `data-slide-to` 来给旋转木马的 `data-slide-to="2"` 来传递一个原生的索引，这个可以让幻灯片的处于一个从 `0` 开始的指定的位置。

这个 `data-ride="carousel"` 属性用来标识动画加载一个旋转木马当一个当页面加载的时候。**这不可以与明确的 JavaScript 初始化同一个旋转木马结合使用。**

### 使用 JavaScript

手动调用旋转木马:

{% 高亮 js %}
$('.carousel').carousel()
{% 结束高亮 %}

### 选项

选项可以通过数据属性或者 JavaScript 传递。对于数据属性，在属性名字前面加上 `data-` ，比如 `data-interval=""`。

<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
     <tr>
       <th style="width: 100px;">名称</th>
       <th style="width: 50px;">类型</th>
       <th style="width: 50px;">默认</th>
       <th>描述</th>
     </tr>
    </thead>
    <tbody>
     <tr>
       <td>interval</td>
       <td>number</td>
       <td>5000</td>
       <td>在两个选项卡之间自动旋转的暂停时间。如果为false，那么旋转木马不会自动旋转。</td>
     </tr>
     <tr>
       <td>pause</td>
       <td>string</td>
       <td>"hover"</td>
       <td>当鼠标进入时暂停旋转，当鼠标离开时恢复旋转。</td>
     </tr>
     <tr>
       <td>wrap</td>
       <td>boolean</td>
       <td>true</td>
       <td>旋转木马是否需要持续旋转，或者硬停止。</td>
     </tr>
     <tr>
       <td>keyboard</td>
       <td>boolean</td>
       <td>true</td>
       <td>旋转木马是否需要响应键盘的事件。</td>
     </tr>
    </tbody>
  </table>
</div>

### 方法

#### .carousel(options)

通过使用一个可选的 `object` 参数来初始化一个旋转木马并且开始旋转。

{% highlight js %}
$('.carousel').carousel({
  interval: 2000
})
{% endhighlight %}

#### .carousel('cycle')

从左到右开始旋转。

#### .carousel('pause')

通过选项暂停旋转木马。

#### .carousel(number)

通过一个特定的数字来旋转（从 0 开始，就像一个数组）。

#### .carousel('prev')

旋转到前一个幻灯片。

#### .carousel('next')

旋转到下一个幻灯片。

### 事件

Bootstrap 的旋转木马类提供了 2 个绑定旋转木马功能的事件。这两个事件都有额外的属性：

- `direction`: 这个旋转木马旋转的方向（`"left"` 或者 `"right"`）。
- `relatedTarget`: 旋转到的活跃的 DOM 节点。

所有的旋转木马事件都是由旋转木马本身触发（比如：在 `<div class="carousel">` 里面）。

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
       <td>slide.bs.carousel</td>
       <td>当<code>slide</code> 方法触发的时候这个事件将会被痢疾调用。</td>
     </tr>
     <tr>
       <td>slid.bs.carousel</td>
       <td>当旋转木马完成滑动过渡的时候这个事件将会被触发。</td>
     </tr>
    </tbody>
  </table>
</div>

{% highlight js %}
$('#myCarousel').on('slide.bs.carousel', function () {
  // do something…
})
{% endhighlight %}
