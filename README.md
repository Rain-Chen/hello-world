Hello world Github!!test ����;retest ����;windows��ֻ����notepad������ΪGB2312
OK,Github helloworld��ɣ�˵һ���м�������һЩ���⣺
1.�ս���ֿ������ʾ��git remote add origin git@github.com:Rain-Chen/hello-world.gitʱ������
fatal: remote origin already exists.����git remote rm origin������error: Could not remove config section 'remote.origin'��Ҫ�޸�etc�µ�gitconfig�ļ�C:\Users\Administrator\AppData\Local\GitHub\PortableGit_015aa71ef18c047ce8509ffb2f9e4bb0e3e73f13\etc\config�ļ���[remote "origin"]
	
	fetch = +refs/heads/*:refs/remotes/origin/*
	
	fetch = +refs/pull/*/head:refs/remotes/origin/pr/*ɾ������
2.�����������⣺Log�ύʱʹ������ע�͡�Ŀ¼�����ļ����������ġ������к�������ע��
����취��
��etc\git-completion.bash�ļ�����ӣ�
alias ls='ls --show-control-chars --color=auto'
���ã�ʹ���� Git Bash ������ ls �������������ʾ�����ļ���
�޸�etc\inputrc�ļ��е��������ã�
set output-meta on
set convert-meta off
���ã�ʹ���� Git Shell �п��������������ģ��������ĵ� commit log
��etc\profile�ļ�����ӣ�
export LESSCHARSET= utf-8
��C:Gitetcgitconfig�ļ����޸Ļ�����������ã�
[core]
quotepath = false
���ã�û����һ����$git status������Ļ���ʾΪUNICODE����
������κ�ƽ̨�ϱ�����ļ���Ҫ����UTF-8�ַ�������Ĳ���
