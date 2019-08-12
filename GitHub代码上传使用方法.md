使用Git上传代码思路：
<br/>
Github账户设置SSH key:<br/>
---
 生成ssh key
-------
首先检查是否已生成密钥 cd ~/.ssh，ls如果有3个文件，则密钥已经生成，id_rsa.pub就是公钥
如果没有生成，那么通过$ ssh-keygen -t rsa -C “邮箱”来生成


1）是路径确认，直接按回车存默认路径即可

2）直接回车键，这里我们不使用密码进行登录, 用密码太麻烦;

3）直接回车键、

生成成功后，去对应目录C:\Users\specter\.ssh里（specter为电脑用户名，每个人不同）用记事本打开id_rsa.pub，得到ssh key公钥

---
为github账号配置ssh key

切换到github，展开个人头像的小三角，点击settings然后打开SSH keys菜单， 点击Add SSH key新增密钥

---
建立本地仓库
---
<br/>
    git init //把这个目录变成Git可以管理的仓库 <br/>
 　 git add README.md //文件添加到仓库<br/>
　　git add . //不但可以跟单一文件，还可以跟通配符，更可以跟目录。一个点就把当前目录下所有未追踪的文件全部add了 <br/>
　　git commit -m "first commit" //把文件提交到仓库<br/>
　　git remote add origin 你的GitHub地址 //关联远程仓库<br/>
　　git push -u origin master //把本地库的所有内容推送到远程库上<br/>

---
实例：<br/>
	cd 盘符：<br/>
	git init <br/>
    git add . <br/>
	git commit -m "提交文件"  <br/>
	到github 仓库复制仓库地址然后执行指令：git remote add origin 你复制的地址<br/>
	git push -u origin master <br/>
	然后敲个yes <br/>
	到此就全部结束了

	

