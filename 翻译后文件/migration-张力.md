<table>
    <tr>
        <th>布局</th>
        <th>标题</th>
        <th>分组</th>
    </tr>
    <tr>
        <td>docs</td>
        <td>Migrating to v4</td>
        <td>migration</td>
    </tr>
</table>

Bootstrap 4  几乎是对整个项目进行了重写。其中最显著的变化都概括到了下面的内容，与以前相比，拥有了更多的具体的类以及把一些有关的部分变成了相关的组件。

{%标注信息 %}**当心！**它在 flux 中工作的时候和在 v4 alphas 进程中工作是一致的。只有当它在不完整的情况下，我们才会推送来帮助它保持在最新的状态。{%标注信息结束%}

# 总结 #

如下便是从 v3 升级到 v4 的时候你最应该注意的地方。

## 支持的浏览器 ##

- v4 现在放弃了对 IE8 以及 iOS 6 的支持，现在仅仅支持 IE9 以上 以及 iOS 7 以上版本的浏览器。如果对于其中需要用到以前的浏览器，那么请使用 v3.
- 添加了对 Android v5.0 Lollipop 浏览器和 web 视图的官方支持。早期版本的 Android 浏览器和 web 视图仍然只有非官方支持。

## 全局变化 ##

- 对于 CSS 文件，从 LESS 切换到了 SCSS.
- 对于主要的 CSS 单元，从 `px` 切换到了 `rem`.
- 媒体查询现在是在 `ems` 中而不是 `pxs`  中。
- 全局字体大小从 `14px` 增加到了 `16px`。
- 为 `~ 480px` 及其以下添加了一个新的网格层。
- 通过 SCSS 变量，可以使用可配置的选项来替换单独的可选主题 (例如，`$enable-gradients: true`)。

## 组件 ##

- 对于该包罗万象的新的组件，丢弃了面板，缩略图以及wells。
- 丢弃了 Glyphicons 图标字体。
- 丢弃了 Affix jQuery 插件。相反，我们推荐使用 `position: sticky`。如果想要查看 [HTML5](http://html5please.com/#sticky)，请点击该这里，查看详细具体的填充代码建议。
- 重构几乎所有的组件来使用更多的 unnested 的类而不是子选择器。

## Misc ##

- Bootstrap 不再支持非响应的用法。
- 丢弃了在线定制器功能，支持更广泛的安装文件以及自定义的工程。

# 组件上的差别 #

## 重启 ##

对于 Bootstrap 4 有一个新的部分------重启，即一个新的样式表，基于标准化的基础上再添加上我们自定义的重置样式。当使用 Element 对象的时候我们才会用到选择器------在这里没有类。它使用更模块化的方法将我们重置的样式和组件样式进行分离。它们包括了一些最重要重置比如一些`边框尺寸`，`边界`的变化，许多元素从 `rem` 移动到 `em` 单元，链接样式，还有许多 element 对象中的变化。

## 版式 ##

- 将所有的 `.text- utilities` 移动到了 `_utilities.scss` 文件。
- 完全删除了 `.page-header` 类。
- `.dl-horizontal` 现在需要网格类，增加了列宽的灵活性。
- 将自定义的<blockquote>样式移动到了类------`.blockquote` 和 `.blockquote-reverse` 修饰符中。

## 表 ##

- 几乎所有实例的 > 符号都被删除了，意味着嵌套的表格现在将自动继承他们的父母的样式。这大大简化了我们的选择器和潜在的自定义设置。
- 响应表不再需要包装元素。相反，仅仅只需要把 `.table-responsive` 放在 `<table>` 即可。
- 考虑一致性，将 `.table-condensed` 重命名为 `.table-sm`。
- 添加了一个新的 `.table-inverse` 选项。
- 添加了一个新的 `.table-reflow` 选项。
- 添加了表头修饰符：`.thead-default` 和 `.thead-inverse`。

## 表单 ##

- 将重置元素移动到了 `_reboot.scss` 文件夹。
- 分别将 `.input-lg` 和 `.input-sm` 重命名为 `.form-control-lg` 和 `.form-control-sm`。
- 为了简单起见，现在删除了 `.form-group-*` 类，现在使用 `.form-control-*`  类。
- 水平表单的检修：
 - 取消了 `.form-horizontal` 类的要求。
 - .form-group 类现在不再和 `.row `混合，所以它现在需要网格布局。
 - 将一个新的 `.form-control-label` 类添加到了带有 `.form-controls` 的垂直中心标签中。
 
## 网格系统 ##

添加了新的 `~ 480px` 网格断点，意味着现在有五个总层。

## 按钮 ##

- 完全删除了 `.btn-xs` 类。

## 按钮组 ##

- 完全删除了 `.btn-group-xs` 类。

## Navs ##

- 删除了几乎所有的 `>` 符号，通过使用非嵌套类来实现更简单的样式。
- 我们现在直接使用单独的  `.navs,` `.nav-items`, 和 `.nav-links` 类而不是像 `.nav > li > a` 这样的 `HTML` 特定的符号。

## Pager ##

- 分别将 `.previous` 和 `.next` 重命名为 `.pager-prev` 和 `.pager-next`.

## Panels, thumbnails, 和 wells ##

对于新的 card 组件，他们几乎全部被删除了。

### Panels ###

.panel 改为 .card
将 .panel-default 删除并且不进行替换
.panel-heading 改为 .card-header
.panel-title 改为 .card-title
.panel-body 改为 .card-block
.panel-footer 改为 .card-footer
.panel-primary 改为 .card-primary 以及 .card-inverse
.panel-success 改为 .card-success 以及 .card-inverse
.panel-info 改为 .card-info 以及 .card-inverse
.panel-warning 改为 .card-warning 以及 .card-inverse
.panel-danger 改为 .card-danger 以及 .card-inverse

## Carousel ##

将 .item 更名为 .carousel-item.

# 文档 #

我们对文档也进行了升级，如下所示：

- 我们还是使用 Jekyll，但我们在组合中配置了自定义插件:
 - example.rb 是默认插件 highlight.rb 的拷贝，它允许更容易的处理示例代码。
 - callout.rb  也是该插件类似的拷贝，但是它是为我特殊的文档标注所设计。
- 为了更加轻松的编辑，所有文档内容都已经在 Markdown (而不是 HTML) 中被重写。
- 为了让内容更简单，层次结构更清晰，所有页面被进行了重组。
- 我们从普通的 CSS 改成了 SCSS，为了更好的利用 Bootstrap 的变量，mixins 极其更多内容。

# 新的部分 #

我们已经添加了以及改变了一些现有的组件。如下是新的或更新的样式。

<table><thead>
<tr>
<th>组件</th>
<th>描述</th>
</tr>
</thead><tbody>
<tr>
<td>Cards</td>
<td>一个新的、 更灵活的组件，它用来来取代 v3 中的的panels, thumbnails, 和 wells。</td>
</tr>
<tr>
<td>新导航栏</td>
<td>用一个新的、 更简单的组件替换以前的导航栏。</td>
</tr>
<tr>
<td>新进度栏</td>
<td>用现在的 <code>&lt;progress&gt;</code> 元素替换旧的 <code>.progress</code> <code>&lt; div &gt;</code>。</td>
</tr>
<tr>
<td>新的变形的表</td>
<td>添加 <code>.table-inverse</code>, 表头选项, 用 <code>.table-sm</code>, and <code>.table-reflow</code> 替换 <code>.table-condensed</code> .</td>
</tr>
<tr>
<td>新的实用程序类</td>
<td></td>
</tr>
</tbody></table>

TODO: 审计了 v3 中不存在的新类。

# 移除 # 的部分。

下述组件在 v4.0.0 中被移除了。

<table><thead>
<tr>
<th>组件</th>
<th>从 3.x.x 中移除</th>
<th>在 4.0.0 中相当于</th>
</tr>
</thead><tbody>
<tr>
<td>Panels</td>
<td></td>
<td>Cards</td>
</tr>
<tr>
<td>Thumbnails</td>
<td></td>
<td>Cards</td>
</tr>
<tr>
<td>Wells</td>
<td></td>
<td>Cards</td>
</tr>
<tr>
<td>Justified navs</td>
<td></td>
<td></td>
</tr>
</tbody></table>

TODO:  v3 中的审计类在 v4 中不存在。

# 响应程序 #

下述已弃用的变量在 V4.0.0 被移除了:

- `@screen-phone`、 `@screen-tablet`、 `@screen-desktop`、 `@screen-lg-desktop`。相反的，使用更多抽象的 `$screen-{xs、 sm、 md、 lg、 xl}-*` 变量。
- `@screen-sm`，`@screen-md`，`@screen-lg.`相反，使用更明确地命名的变量 `$screen-{xs，sm，md，lg，xl}-min` 。
- `@screen-xs`，`@screen-xs-min`。这些额外的小断点有没有下限，因此，这些变量在逻辑上是荒谬的。根据 `$screen-xs-max`  改写你的表达式。

响应实用程序类也已经进行了彻底翻新。

- 这些类（`.hidden-xs` .`hidden-sm` `.hidden-md` `.hidden-lg` `.visible-xs-block` `.visible-xs-inline` `.visible-xs-inline-block` `.visible-sm-block` `.visible-sm-inline` `.visible-sm-inline-block` `.visible-md-block` `.visible-md-inline` `.visible-md-inline-block` `.visible-lg-block` `.visible-lg-inline` `.visible-lg-inline-block`）都被删除了。
- 它们被 `.hidden-xs-up` `.hidden-xs-down` `.hidden-sm-up` `.hidden-sm-down` `.hidden-md-up` `.hidden-md-down` `.hidden-lg-up` `.hidden-lg-down` 进行了替换。

当视区是在给定的断点或更大的范围内 `.hidden-*-up` 类将隐藏元素 (例如`.hidden-md-up` 会隐藏中型、 大型，和特大型设备上的元素)。

当视区是在给定的断点或更小的范围内 `.hidden-*-down` 类将隐藏元素 (例如`.hidden-md-down` 会隐藏超小尺寸、 中小型，和小型设备上的元素)。

当你想要让一个元素可见，你仅仅需要不把它隐藏在这样的屏幕尺寸下，而不是使用显示的 `.visible-*` 类。你可以结合一个 `.hidden-*-up` 类和一个 `.hidden-*-down` 类来在给定的时间间隔的屏幕尺寸上显示元素(如`.hidden-sm-down` `.hidden-xl-up` 仅在中型和大型的设备上显示元素)。

请注意，在 v4 中对网格断点进行更改意味着你需要让一个断点更大来实现相同的结果 (例如 和 `.hidden-md-down` 相比 `.hidden-lg-down` 和 `hidden-md` 更相似)。在一些不常见情况下，比如在元素的可见性不能表示为一个单一的连续范围的视区大小的时候，新的响应实用程序类不要试图去容纳它；相反的，您需要在这种情况下使用自定义的 CSS。

# 使用 Misc 来确定优先级 #

为视网膜显示器媒体查询删除 `min--moz-device-pixel-ratio` 黑客错误。
删除了 `.hidden` 和 `.show`，因为它在 `jQuery` 的 `$(...).hide()`拥有接口.
因为 IE 9 + 支持 `:disabled`，所以将 `[disabled]` 按钮改成了 `:disabled `。然而 `fieldset[disabled]` 仍然是必要的，因为[本机禁用字段在 IE11 中仍然会存在问题](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset#Browser_compatibility)。

TODO:  v3 中的事物审核列表被标记为已弃用。

# 附加说明 #

- 删除了对样式嵌套表格的支持 （当前）
