---
布局: 文档
标题: 滚动监听
组: 组件
---

## 目录

* 将会被 ToC 替代，除“目录”头部之外
{:toc}

## 导航条中的实例

滚动监听插件是用来根据滚动条位置自动的更新导航项的。滚动导航条下面的区域并观察 active 类的变化。下拉菜单中的条目也会高亮显示。

<div class="bd-example">
  <nav id="navbar-example2" class="navbar navbar-default" role="navigation">
    <h3 class="navbar-brand">Project Name</h3>
    <ul class="nav nav-pills">
      <li class="nav-item"><a class="nav-link" href="#fat">@fat</a></li>
      <li class="nav-item"><a class="nav-link" href="#mdo">@mdo</a></li>
      <li class="nav-item dropdown">
        <a class="nav-link dropdown-toggle" data-toggle="dropdown" href="#" role="button" aria-haspopup="true" aria-expanded="false">Dropdown</a>
        <div class="dropdown-menu">
          <a class="dropdown-item" href="#one">one</a>
          <a class="dropdown-item" href="#two">two</a>
          <div role="separator" class="dropdown-divider"></div>
          <a class="dropdown-item" href="#three">three</a>
        </div>
      </li>
    </ul>
  </nav>
  <div data-spy="scroll" data-target="#navbar-example2" data-offset="0" class="scrollspy-example">
    <h4 id="fat">@fat</h4>
    <p>Ad leggings keytar, brunch id art party dolor labore. Pitchfork yr enim lo-fi before they sold out qui. Tumblr farm-to-table bicycle rights whatever. Anim keffiyeh carles cardigan. Velit seitan mcsweeney's photo booth 3 wolf moon irure. Cosby sweater lomo jean shorts, williamsburg hoodie minim qui you probably haven't heard of them et cardigan trust fund culpa biodiesel wes anderson aesthetic. Nihil tattooed accusamus, cred irony biodiesel keffiyeh artisan ullamco consequat.</p>
    <h4 id="mdo">@mdo</h4>
    <p>Veniam marfa mustache skateboard, adipisicing fugiat velit pitchfork beard. Freegan beard aliqua cupidatat mcsweeney's vero. Cupidatat four loko nisi, ea helvetica nulla carles. Tattooed cosby sweater food truck, mcsweeney's quis non freegan vinyl. Lo-fi wes anderson +1 sartorial. Carles non aesthetic exercitation quis gentrify. Brooklyn adipisicing craft beer vice keytar deserunt.</p>
    <h4 id="one">one</h4>
    <p>Occaecat commodo aliqua delectus. Fap craft beer deserunt skateboard ea. Lomo bicycle rights adipisicing banh mi, velit ea sunt next level locavore single-origin coffee in magna veniam. High life id vinyl, echo park consequat quis aliquip banh mi pitchfork. Vero VHS est adipisicing. Consectetur nisi DIY minim messenger bag. Cred ex in, sustainable delectus consectetur fanny pack iphone.</p>
    <h4 id="two">two</h4>
    <p>In incididunt echo park, officia deserunt mcsweeney's proident master cleanse thundercats sapiente veniam. Excepteur VHS elit, proident shoreditch +1 biodiesel laborum craft beer. Single-origin coffee wayfarers irure four loko, cupidatat terry richardson master cleanse. Assumenda you probably haven't heard of them art party fanny pack, tattooed nulla cardigan tempor ad. Proident wolf nesciunt sartorial keffiyeh eu banh mi sustainable. Elit wolf voluptate, lo-fi ea portland before they sold out four loko. Locavore enim nostrud mlkshk brooklyn nesciunt.</p>
    <h4 id="three">three</h4>
    <p>Ad leggings keytar, brunch id art party dolor labore. Pitchfork yr enim lo-fi before they sold out qui. Tumblr farm-to-table bicycle rights whatever. Anim keffiyeh carles cardigan. Velit seitan mcsweeney's photo booth 3 wolf moon irure. Cosby sweater lomo jean shorts, williamsburg hoodie minim qui you probably haven't heard of them et cardigan trust fund culpa biodiesel wes anderson aesthetic. Nihil tattooed accusamus, cred irony biodiesel keffiyeh artisan ullamco consequat.</p>
    <p>Keytar twee blog, culpa messenger bag marfa whatever delectus food truck. Sapiente synth id assumenda. Locavore sed helvetica cliche irony, thundercats you probably haven't heard of them consequat hoodie gluten-free lo-fi fap aliquip. Labore elit placeat before they sold out, terry richardson proident brunch nesciunt quis cosby sweater pariatur keffiyeh ut helvetica artisan. Cardigan craft beer seitan readymade velit. VHS chambray laboris tempor veniam. Anim mollit minim commodo ullamco thundercats.
    </p>
  </div>
</div>


## 用法

### 需要 Bootstrap 导航组件

滚动监听当前需要使用 [Bootstrap 导航组件]({{ site.baseurl }}/components/nav/)来适当的高亮显示激活的链接。

### 需要相对位置

无论何种实现方式，滚动监听都需要在你监视的元素上使用 `position: relative;`。大多数时候，被监听元素都是 `<body>`。当监听除了 `<body>` 以外的元素时，确保有一个 `height` 设置和一个 `overflow-y: scroll;` 应用。

### 通过 data 属性

想要方便地添加顶栏导航，添加 `data-spy="scroll"` 到你想要监视的元素（最典型的就是 `<body>`）上。然后在任意 Bootstrap `.nav` 组件的父元素的 ID 或者类上添加 `data-target` 属性。

{% highlight css %}
body {
  position: relative;
}
{% endhighlight %}

{% highlight html %}
<body data-spy="scroll" data-target="#navbar-example">
  ...
  <div id="navbar-example">
    <ul class="nav nav-tabs" role="tablist">
      ...
    </ul>
  </div>
  ...
</body>
{% endhighlight %}

### 通过 JavaScript

在你的 CSS 里添加 `position: relative;` 之后，通过 JavaScript 调用滚动监听：

{% highlight js %}
$('body').scrollspy({ target: '#navbar-example' })
{% endhighlight %}

{% callout danger %}
#### 可解析的 ID 目标需求

导航栏链接必须有可解析的 ID 目标。例如，一个 `<a href="#home">home</a>` 必须对应着 DOM 中的像是 `<div id="home"></div>` 的东西。
{% endcallout %}

{% callout info %}
#### 非 `:visible` 目标元素忽略

[根据 jQuery 不是 `:visible`](http://api.jquery.com/visible-selector/) 的目标会被忽略，并且它们对应的导航项将不会被高亮显示。
{% endcallout %}

### 方法

#### .scrollspy('refresh')

当同时使用滚动监听从 DOM 中添加或删除元素后，你需要像下面这样调用刷新方法：

{% highlight js %}
$('[data-spy="scroll"]').each(function () {
  var $spy = $(this).scrollspy('refresh')
})
{% endhighlight %}


### 参数

参数可以通过 data 属性或 JavaScript 传递。对于 data 属性，在 `data-` 上附加参数名称，例如 `data-offset=""`。

<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
     <tr>
       <th style="width: 100px;">名称</th>
       <th style="width: 100px;">类型</th>
       <th style="width: 50px;">默认值</th>
       <th>描述</th>
     </tr>
    </thead>
    <tbody>
     <tr>
       <td>offset</td>
       <td>number</td>
       <td>10</td>
       <td>计算滚动位置时相对于顶部的位移（offset）像素。</td>
     </tr>
    </tbody>
  </table>
</div>

### 事件

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
       <td>activate.bs.scrollspy</td>
       <td>当一个新的项目被滚动监听激活时触发这个事件。</td>
    </tr>
    </tbody>
  </table>
</div>
{% highlight js %}
$('#myScrollspy').on('activate.bs.scrollspy', function () {
  // do something…
})
{% endhighlight %}
