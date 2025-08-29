#这是项目的readme文件，暂时编辑一下

[学习markdown语法][def]

1.项目最开始的目的是搭建一个博客系统，然后保存学习的内容。
2.在网上看了下别人的内容后，选择了mkdocs-material来搭建
3.发现mkdocs-material后，把文件上传了到了github，现在的进度就是在研究怎么使用github同步项目。
具体内容可以去看github.md

更新的方法，本地先修改文件，然后保存
运行
`mkdocs build`
生成文件
`git add .
git commit -m "更新" #更新修改成你的更改内容


这里碰到一个warning：warning: in the working copy of 'site/404.html', LF will be replaced by CRLF the next time Git touches it
解决方法：git.md

## 推送到远程仓库的 main 分支（或其他分支）
git push -u origin main

本项目使用python版本的mkdocs-material搭建
使用python3
使用pip的python包管理器来安装

使用Visual Studion Code来开发

然后把页面发布到github上面

首先,我们先给项目建立一个文件夹,这里使用tfpdc-mkdocs,在 文件夹的菜单栏输入cmd进去终端,在终端中输入code .,打开vscode,
在vscode中打开终端
建立一个python虚拟空间
`python -m venav tfpdc-mkdocs
 python -m venv tfpdc-docs
使用ls检查有没有同名文件夹生成,
 .\tfpdc-docs\Scripts\activate打开虚拟环境
pip install mkdocs-material 安装依赖

现在我们把项目文件下载到本地

启动git bash,(进去当前目录,右键点击 open git bash here)

git clone https://github.com/tfpdc/tfpdc-mkdocs.git
把远程文件下载到本地.

更新文件后把本地文件打包 mkdocs build







[def]: https://markdown.com.cn/

