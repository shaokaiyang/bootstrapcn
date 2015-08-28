<table>
<tbody>
<tr><td><em>layout</em></td><td><em>title</em></td><td><em>group</em></td></tr>
<tr><td>docs</td><td>Team</td><td>about</td></tr>
</tbody>
</table>

{% for member in site.data.core-team %}  
[{{ member.name }} @{{ member.user }}](https://github.com/%7B%7B%20member.user%20%7D%7D)    
{% endfor %}    
通过[提出一个问题](https://github.com/twbs/bootstrap/issues/new)或[提交一个请求](https://github.com/twbs/bootstrap/blob/master/CONTRIBUTING.md)，参与 Bootstrap 程序开发。阅读关于我们如何发展的贡献引导。
