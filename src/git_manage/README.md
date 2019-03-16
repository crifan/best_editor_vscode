# Git代码管理

## 查看文件历史版本和改动差异

如果需要对比之前某次的文件代码和当前最新代码有何改动，可以通过`File History`文件历史，得到我们要的效果：

比如想要对此这段代码和之前的写法有何不同：

![想要查看某段代码的改动历史](../../assets/img/some_code_to_know_history.png)

则可以：文件中右键选择 `Git: View File History`

![右击选择Git: View File History](../../assets/img/right_click_git_view_file_history.png)

或Tab页中右键选择：

![文件顶部右键选择Git: View File History](../../assets/img/file_top_choose_file_hisotry.png)

然后就可以看到各个历史版本了：

![查看文件的历史](../../assets/img/show_git_file_history.png)

点击其中一个版本可以查看提交详情：

![点击某文件查看历史改动](../../assets/img/click_some_file_show_history.png)

点击某次提交中的某个文件：

![点击某次提交中的某文件](../../assets/img/click_some_file_in_some_commit.png)

选择：Compare against workspace file

![选择：Compare against workspace file](../../assets/img/choose_compare_against_workspace_file.png)

即可去该版本和当前最新文件，去对比内容差异：

![显示文件对比试图看差异](../../assets/img/some_file_compare_view_diff.png)

其中左边是最新内容，右边是之前该版本的内容。

另外，如果需要还可以在查看历史版本时，根据不同条件筛选，比如根据作者：

![根据作者筛选文件](../../assets/img/show_file_diff_by_author.png)

即可只查看某人的提交的代码：

![只显示某人提交的代码](../../assets/img/only_show_some_author_commits.png)
