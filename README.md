Hello world Github!!test 中文;retest 中文;windows下只能用notepad但不能为GB2312
OK,Github helloworld完成，说一下中间遇到的一些问题：
1.刚建玩仓库后按照提示做git remote add origin git@github.com:Rain-Chen/hello-world.git时出现了
fatal: remote origin already exists.输入git remote rm origin还报错error: Could not remove config section 'remote.origin'需要修改etc下的gitconfig文件C:\Users\Administrator\AppData\Local\GitHub\PortableGit_015aa71ef18c047ce8509ffb2f9e4bb0e3e73f13\etc\config文件把[remote "origin"]
	
	fetch = +refs/heads/*:refs/remotes/origin/*
	
	fetch = +refs/pull/*/head:refs/remotes/origin/pr/*删除即可
2.中文乱码问题：Log提交时使用中文注释、目录或者文件名含有中文、代码中含有中文注释
解决办法：
在etc\git-completion.bash文件中添加：
alias ls='ls --show-control-chars --color=auto'
作用：使得在 Git Bash 中输入 ls 命令，可以正常显示中文文件名
修改etc\inputrc文件中的两项配置：
set output-meta on
set convert-meta off
作用：使得在 Git Shell 中可以正常输入中文，比如中文的 commit log
在etc\profile文件中添加：
export LESSCHARSET= utf-8
在C:Gitetcgitconfig文件中修改或添加如下配置：
[core]
quotepath = false
作用：没有这一条，$git status输出中文会显示为UNICODE编码
最后在任何平台上保存的文件都要是以UTF-8字符集保存的才行
