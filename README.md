### 1、安装
``` 
[Git官网](https://git-scm.com/downloads
```

### 2、获取SSHKey：
``` 
输入ssh-keygen 然后一直回车输入y即可
```
### 3、查看生成 key
```
输入：cat ~/.ssh/id_rsa.pub
或者：C:\Users\akei\.ssh
```
### 4、将.ssh/id_rsa.pub生成的key添加到远程仓库中
### 5、设置基本信息
```
查看信息：git config --list     进行查看user.name和user.email项

注：邮箱必须和远程仓库绑定的保持一致 即：user.email
git config --global user.name “momo”
git config --global user.email “momo@163.com”
```
#### 6、创建新分支 
```
git branch -d xiaoguo_fix   # -d分支被合并后才允许删除xiaoguo_fix分支(-D强制删除分支) 
git checkout -b xiaoguo_fix  # 先创建一个新分支xiaoguo_fix , 并切换到那个分支上 
git add .             .添加所有到暂存区,加上文件名也可以单独添加
git commit -m "xxxxx"  提交 
git push -u origin xiaoguo_fix    (本地有xiaoguo_fix 分支  远程没有xiaoguo_fix ) 
```


### 远程有仓库本地没有怎么办？
```
参考：https://www.jianshu.com/p/811b07b129e8

1.将某个远程主机的更新，全部取回本地：git fetch 
2.查看远程分支：git branch -a 
3.查看本地分支：git branch 
4.切换分支：git checkout 分支 
```