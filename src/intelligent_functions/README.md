# VSCode的智能好用之处

## 自动更新import语句

当从已有的一个文件，复制并改名后，VSCode可以自动检测出来，提示是否需要更新import语句

![是否更新已更新文件的import语句](../../assets/img/auto_update_renamed_import.png)

即可自动更新import语句：

![更新后的import语句](../../assets/img/updated_import_code.png)

不过，此处更新后的内容不是我要的，竟然把本来正常的都改错误了，所以还要自己去改回来。以后慎用这个自动修改import的功能。

## 快速跳转文件

`Command + P`后，输入（部分）文件名（支持模糊搜索）：

![command+p后输入文件名](../../assets/img/command_pallet_input_name.png)

选中回车即可跳转文件：

![快速跳转到对应文件](../../assets/img/fast_open_select_file.png)

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

![某个python错误日志文件](../../assets/img/python_log_error_file.png)

可以跳转到对应的文件：

![跳转到log错误对应源码文件](../../assets/img/jump_to_log_related_file_position.png)
