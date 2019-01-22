# 上传本地代码到github

**第一步：建立git仓库** 
在你想上传的文件夹下面，鼠标右键点击git bash here.

执行Git命令：git init

**第二步：将项目的所有文件添加到仓库中**

执行“git add .” 。

**如果想添加某个特定的文件，只需把“.”换成特定的文件名即可。**

 

**第三步：将add的文件commit到仓库**

执行“git commit -m "文件名"。

### 第四步：去github上创建自己的Repository,拿到创建的仓库的https地址

### 第五步：重点来了，将本地的仓库关联到github上

 git remote add origin https://github.com/handsomeboyck/angular6.git

后面的https链接地址换成你自己的仓库url地址

**第六步：上传github之前，要先pull一下，执行如下命令：**

git pull origin master

**第七步，也就是最后一步，上传代码到github远程仓库**

//git pull origin master --allow-unrelated-histories

git push -u origin master