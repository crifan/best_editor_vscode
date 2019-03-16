# 调试Python

VSCode支持调试Python代码：

之前去试了：

【已解决】VSCode中调试Python代码

[【记录】用VSCode开发和调试Python](http://www.crifan.com/use_vscode_develop_debug_python)

效果很好。

## 设置Python解析器

### 手动设置选择Python版本

调试之前，先要设置Python解析器。

对于python代码中：

```python
#!/usr/bin/python
# -*- coding: utf-8 -*-
```

其可以自动检测出当前的第一行的解析器，然后显示出`Set as interpreter`，如果点击了：

![检测并提示Set as interpreter](../../assets/img/detect_show_set_as_interpreter.png)

则就可以从当前的解析器：

![选择Python 2.7.10](../../assets/img/choose_python_2_7_10.png)

换成代码中设置的解析器了：

![换成所选Python版本](../../assets/img/changed_to_selected_python.png)

### 选择虚拟环境的Python版本

在用

```bash
pipenv install
```

安装了虚拟环境的python项目后，重新用VSCode打开该项目，会提示你

> You have selected the macOS system install of Python, which is not not recommended for use with the Python extension. Some functionality will be limited, please select a different interpreter.

![selected python not recommended](../../assets/img/selected_python_not_recommended.png)

然后点击`Select Python Interpreter`，去选择刚装好的虚拟环境中的python：

![选择用pipenv安装后的python虚拟环境](../../assets/img/choose_installed_pipenv_python.png)

选择后，左下角就可以显示出当前所选Python了：

![显示当前Python是刚所选虚拟环境](../../assets/img/showing_python_selected_virtualenv.png)

## 鼠标移动上去可以查看变量值

后来又多次使用VSCode去调试Python：

![用VSCode调试Python的效果](../../assets/img/vscode_debug_python_view.png)

鼠标移动到变量（类）的属性上，支持（直接）显示变量的属性的值：

比如datetime

![鼠标移动到datetime](../../assets/img/mouse_move_to_datatime.png)

的microsecond：

![移动到microsecond看到值](../../assets/img/move_to_microsecond_see_value.png)

而这类功能，之前只有比较高级的IDE，比如`Visual Studio`，`PyCharm`等才支持。

## 支持异常信息的显示

当调试代码时发生异常，则可以方便快速的显示异常堆栈错误信息：

![VSCode显示Python异常信息](../../assets/img/show_python_exception_stack_info.png)

且可以点击左下角的 调用堆栈，调转到对应代码位置：

![从异常堆栈中快速定位文件](../../assets/img/click_stack_file_to_locate.png)

## 注意事项

偶尔出现小问题，可参考：

### 调试适配器进程意外终止

[【已解决】VSCode调试Python出错：调试适配器进程意外终止Cannot read property 'style' of undefined](http://www.crifan.com/vscode_python_debugger_process_stopped_exceptionally_cannot_read_property_style_of_undefined)

### 文件内容改动后断点错位

有时候会遇到：当前面新增行后，后面的断点位置都移动了，错位了。

比如此处，前面新增了2行，导致后面的，之前设置的断点，都错位了，无效了：

![代码改动后断点错乱](../../assets/img/code_changed_breakpoint_messy.png)

只能再：去掉之前断点，重新打断点：

![重新给Python添加断点](../../assets/img/re_add_breakpoint_for_python.png)

所以还是有点点麻烦的

-》而PyCharm就可以很好的支持：当代码改动（不多）的时候，可以自动保持原有的断点的位置。

-》不过后来也发现，此问题只是偶尔发生的。有时候代码改动后，断点还正常的。