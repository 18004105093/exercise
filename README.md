# Git 基本使用
### 1.git clone 
将远程文件克隆到本地仓库
### 2.git fetch
同步远程仓库到本地仓库
### 3.git checkout
只需要知道它是用来切换分支即可
### 4.git pull
将远程仓库中的更改合并到当前分支中
### 5.git add
主要实现将工作区修改的内容提交到暂存区，交由git管理。
### 6.git commit
主要实现将暂存区的内容提交到本地仓库，并使得当前分支的HEAD向后移动一个提交点。
### 7.git status
查看文件变更状态
### 8.git rebase and git merge 
>(1)现在我们有这样的两个分支,test和master，提交如下：</br>
>              D---E test</br>
>             /</br>
>        A---B---C---F master复制代码</br>
>(2)在master执行git merge test,然后会得到如下结果：</br>
>            D--------E</br>
>           /          \</br>
>      A---B---C---F----G   test, master复制代码</br>
>(3)在master执行git rebase test，然后得到如下结果：</br>
>    A---B---D---E---C'---F'   test, master复制代码</br>

so:如果你想要一个干净的，没有merge commit的线性历史树，那么你应该选择git rebase</br>
   如果你想保留完整的历史记录，并且想要避免重写commit history的风险，你应该选择使用git merge</br>
(内心os:你开心就好，一般自己的项目咋写开心咋写，多人开发的项目为了能取到更多有效信息还是推荐rebase)</br>
### 9.git revert and git reset
git revert是用一次新的commit来回滚之前的commit
git reset是直接删除指定的commit
[详细内容参照](http://yijiebuyi.com/blog/8f985d539566d0bf3b804df6be4e0c90.html "git reset revert")
### 10.git push
上传本地仓库分支到远程仓库分支，实现同步。
# Git 需要熟悉的概念
- conflict
[如何解决冲突](https://gitbook.tw/chapters/branch/fix-conflict.html "解决冲突")
- PR
- fork（了解）

[一篇文章，教你学会Git](https://www.jianshu.com/p/9685a56bdf7a "git基本使用")
