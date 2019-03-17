# VSCode的智能好用之处

## 自动更新import语句

当从已有的一个文件，复制并改名后，VSCode可以自动检测出来，提示是否需要更新import语句

![是否更新已更新文件的import语句](../assets/img/auto_update_renamed_import.png)

即可自动更新import语句：

![更新后的import语句](../assets/img/updated_import_code.png)

不过，此处更新后的内容不是我要的，竟然把本来正常的都改错误了，所以还要自己去改回来。以后慎用这个自动修改import的功能。

## 快速跳转文件

`Command + P`后，输入（部分）文件名（支持模糊搜索）：

![command+p后输入文件名](../assets/img/command_pallet_input_name.png)

选中回车即可跳转文件：

![快速跳转到对应文件](../assets/img/fast_open_select_file.png)

## log日志中点击文件路径可以跳转到该文件

比如调试期间出错了，点击对应log错误日志中的文件路径：

```python
File "/usr/local/lib/python3.6/site-packages/rest_framework/views.py", line 483, in dispatch
response = self.handle_exception(exc)
File "/usr/local/lib/python3.6/site-packages/rest_framework/views.py", line 443, in handle_exception
self.raise_uncaught_exception(exc)
File "/usr/local/lib/python3.6/site-packages/rest_framework/views.py", line 480, in dispatch
response = handler(request, *args, **kwargs)
File "/Users/crifan/dev/dev_root/company/naturling/projects/xxx/server/xxx/apps/script/views.py", line 136, in create
if i['type'] == '0':
TypeError: string indices must be integers
```

![某个python错误日志文件](../assets/img/python_log_error_file.png)

可以跳转到对应的文件：

![跳转到log错误对应源码文件](../assets/img/jump_to_log_related_file_position.png)

方便调试。

## 提示安装支持相应文件的插件

首次打开`.env`，则提示是否要安装.env的插件，点击 搜索商店：

![提示安装env插件](../assets/img/env_file_notice_install_plugin.png)

然后点击安装插件：

![安装DotEnv插件](../assets/img/install_dotenv_plugin.png)

安装后，重启加载：

![已安装好DotEnv插件](../assets/img/installed_dotenv_plugin_reload.png)

然后.env就可以语法高亮了：

![env文件语法高亮](../assets/img/env_file_highlight.png)

另外类似的情况还有：

首次打开vue提示安装对应的插件：

![vue建议安装插件Vetur](../assets/img/recommend_vue_plugin_vetur.png)

![安装Vetur插件](../assets/img/install_vetur_plugin.png)

## 根据路径动态提示文件

刚新建个文件夹，加入了几个js文件后，然后再去html中输入路径后，即可动态匹配路径和文件：

![动态匹配出文件夹](../assets/img/file_path_hint_folder.png)

![智能匹配列出文件名](../assets/img/auto_list_match_file.png)

很是智能和贴心。

## 显示大纲

VSCode 1.24版本支持支持`大纲`=`Outline`=`目录`：

> Preview: Outline view - Symbol tree outline and navigation for your projects.

右键项目条，选中 大纲：

![右键显示大纲](../assets/img/project_right_show_outline.png)

点击大纲中的某行后，可以跳转到对应位置，比如：

* Markdown：
  * ![Markdown中大纲点击跳转效果](../assets/img/outline_jump_markdown.png)
* Html
  * ![HTML中大纲点击跳转效果](../assets/img/outline_jump_html.png)

## 未使用变量检测

VSCode 1.24版本支持支持自动检测未使用的变量的提示：

> Unused variable detection - Unused variables are greyed-out in your JavaScript/TypeScript files
