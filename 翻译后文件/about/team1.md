<table>
<tbody>
<tr><td><em>layout</em></td><td><em>title</em></td><td><em>group</em></td></tr>
<tr><td>docs</td><td>Translations</td><td>about</td></tr>
</tbody>
</table>
社区成员已将 Bootstrap 的文档翻译成各种语言。但没有得到官方的支持，而且可能不是最新的版本。
  
{% for language in site.data.translations %}   
[{{ language.description }} ({{ language.name }})](https://github.com/bitmoonz/bootstrapcn/blob/master/about/%7B%7B%20language.url%20%7D%7D)   
{% endfor %}  
 
**我们不组织或主持翻译，我们只是链接到它们。**     
 
完成了一个新的或更好的翻译？打开一个请求将它添加到我们的列表中。
