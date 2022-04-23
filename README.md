#### 1、安装
>**Git官网下载：** https://git-scm.com/downloads

#### 2、获取SSHKey：
``` 
输入ssh-keygen 然后一直回车输入y即可
```
#### 3、查看生成 key
```
输入：cat ~/.ssh/id_rsa.pub
或者在本机地址：C:\Users\akei\.ssh
```
#### 4、将.ssh/id_rsa.pub生成的key添加到远程仓库中
#### 5、设置基本信息
```
查看信息：git config --list     进行查看user.name和user.email项

注：邮箱必须和远程仓库绑定的保持一致 即：user.email
git config --global user.name “momo”
git config --global user.email “momo@163.com”
```
#### 6、克隆关联远程仓库地址
```
克隆仓库：git clone https://gitee.com/usersname/5345
关联远程仓库：git remote add origin https://gitee.com/usersname/1345345
```
#### 7、git基本使用
| 说明       | 操作命令   | 示例 |
| :--------  | :--------  | :-------|
创建分支,-b并切换到分支上 | git checkout mark | git checkout -b mark|
-d删除分支(-D强制删除分支)|git branch -d fix |git branch -D aa_fix|
| .添加所有到暂存区,也可单独添加文件 | git add . | git add index.html |
拉取代码pull|git pull origin master|
| 提交并备注提交说明 | git commit -m "test测试代码" |
提交代码到远程, -u 远程没有mark分支 |git push origin mark |  git push -u origin mark|

#### 8、合并代码到master
```
合并dev分支到master 
切换到master：git checkout master 
合并dev：git merge dev 
(git add) (git commit)  
合并到master：git push origin master  
```
#### 9、stash缓存
> 说明：暂时保存当前更改,分支临时切换
| 说明       | 操作命令   | 示例 |
| :--------  | :--------  | :-------|
把暂存和非暂存的修改都保存起来,save添加备注 | git stash | git stash save "test-stash"|
恢复暂存,恢复指定的进度到工作区|git stash pop |git stash pop 3|
.添加所有到暂存区,也可单独添加文件 | git add . | git add index.html |
查看现有暂存stash|git stash list|
删除所有缓存stash| git stash clear

#### 10、版本回退



#### 9、远程有仓库本地没有怎么办？
```
参考：https://www.jianshu.com/p/811b07b129e8

1.将某个远程主机的更新，全部取回本地：git fetch 
2.查看远程分支：git branch -a 
3.查看本地分支：git branch 
4.切换分支：git checkout 分支 
```