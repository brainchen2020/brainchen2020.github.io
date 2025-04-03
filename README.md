# brainchen2020.github.io

1.部署到github pages里作为个人博客使用。
2.界面扩展。比如主页，显示个人简介，仓库地址等等信息。
3.列表自动识别指定目录，作为分类路由，相当于本地文件目录访问。列表显示归类。分页？
4.限制可读状态，导出页面Push到git pages。【不需要，其实就是本地编辑，然后push到git pages，网页只读。】

HTML+JS请求github仓库读取配置表。
再过滤一些数据，HTML不显示。按一个一个目录来就行。
主页编辑也就完成了。对的。就像一个一个文件打开一样。没啥的。


那index.html使用js，就不是Nash编辑的这怎么办？
index不经常改，可以长期使用。不需要多操作。

可以就这样。


修改界面，index.html，是一个简单的计算vlog界面。左边是界面占1/4，中间2/4，右边留白。
1.左边面显示个人简介。一段文本描述。
2.左下面是联系方式。email，微信，github。
3.中间是仓库列表，通过API动态渲染在前端HTML里。显示全部的HTML。如果是有目录的，按树目录递归显示。
在目录的情况下，按仓库里文件更新时间降序。
比如：基础/GitHub部署页面.html
渲染成。
基础：
    GitHub部署页面.html
    GitHub常规操作.html

// GitHub API URL，注意分支名称（此处默认 main）
    const apiUrl = 'https://api.github.com/repos/brainchen2020/brainchen2020.github.io/git/trees/main?recursive=1';

