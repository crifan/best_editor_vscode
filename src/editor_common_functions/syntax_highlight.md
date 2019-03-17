# 语法高亮

设置文件和代码的语法高亮：

对于未保存的文件时，需要设置文件类型-〉才能使得语法高亮生效

比如新建文件，粘贴html代码，此时代码无法自动高亮

![新拷贝的html代码不能高亮](../assets/img/newly_copy_html_no_highlight.png)

点击右下角的`纯文本`，在弹出的语言列表中选择`HTML`：

![切换语言为HTML](../assets/img/pure_text_change_to_html.png)

即可看到HTML代码高亮的效果了：

![HTML代码高亮的效果](../assets/img/html_highlight_effect.png)

## 支持log类型的语法高亮

无意间发现，VSCode连log格式，都可以支持，都可以语法高亮：

![log日志文件语法高亮效果](../assets/img/log_file_highlight_effect.png)

很是方便查看内容。

另外一个截图：

![另外一个log日志文件语法高亮效果](../assets/img/another_log_highlight.png)

-》后来不知道为何突然log文件丢失语法高亮了

所以又去找了个插件：

[Output Colorizer](https://marketplace.visualstudio.com/items?itemName=IBM.output-colorizer)

![已安装Output Colorizer](../assets/img/plugin_output_colorizer.png)

安装后，效果也很不错：

![log日志效果很不错](../assets/img/log_highlight_effect_good.png)
