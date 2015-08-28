<table>
<tbody>
<tr><td><em>类别</em></td><td><em>标题</em></td><td><em>群组</em></td></tr>
<tr><td>说明文档</td><td>导航控件</td><td>组件</td></tr>
</tbody>
</table>

在导航层次之中，指示当前页面的位置。

通过 CSS 自动添加分隔符
[`::before`](https://developer.mozilla.org/en-US/docs/Web/CSS/::before) 和 [`content`](https://developer.mozilla.org/en-US/docs/Web/CSS/content).

{% example html %}
<ol class="breadcrumb">
  <li class="active">Home</li>
</ol>
<ol class="breadcrumb">
  <li><a href="#">Home</a></li>
  <li class="active">Library</li>
</ol>
<ol class="breadcrumb" style="margin-bottom: 5px;">
  <li><a href="#">Home</a></li>
  <li><a href="#">Library</a></li>
  <li class="active">Data</li>
</ol>
{% endexample %}
