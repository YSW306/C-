## git的一些知识

git的工作区是文件夹。分支与工作区没有关系

工作区、**暂存区**、版本库

1.

git --config user.name ysw

git --config user.email 11XXXX

2.

在gitconfig中查看已经配置好的文件

2.

创建文件夹project，进入文件夹 git init

3.

创建文件readme,txt

4.

git status查看当前仓库状态

红色

绿色：放入暂存区之中

5.

git add 加入暂存区

git add .：将所有待加入暂存区的文件加入暂存区

6.

git commit -m "给自己看的备注信息"：**将暂存区的内容提交到当前分支**

暂存区会清空



**git restore --stage readme.txt**

**将暂存区的文件撤出，但是不会修改文件**



git diff readme.txt

比较的是文件与暂存区的文件的区别



git rm --cached XX  将文件从仓库索引目录中删掉



git log  日志

显示在一行 git log --pretty=oneline



代码回滚 git reset --hard HEAD^^

^:回滚一个版本

^^:回滚2个版本



git reset --hard HEAD^ 或 git reset --hard HEAD~：将代码库回滚到上一个版本
git reset --hard HEAD^^：往上回滚两次，以此类推
git reset --hard HEAD~100：往上回滚100个版本
git reset --hard 版本号：回滚到某一特定版本



git log 打印出来的是初始到回滚的地方的结点（从下往上读）



git reflog 代码回滚的整个路径



tmux的复制黏贴是啥？



工作区：仓库的目录。工作区是独立于各个分支的。

暂存区：数据暂时存放的区域，类似于工作区写入版本库前的缓存区。暂存区是独立于各个分支的。
版本库：存放所有已经提交到本地仓库的代码版本

版本结构：树结构，树中每个节点代表一个代码版本。