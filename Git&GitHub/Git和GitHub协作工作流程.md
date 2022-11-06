# Git和GitHub协作工作流程

## 所需材料
1. github已建立一个空仓库'helloWorld'，且主分支为**main**；
2. 本地电脑已安装完成Git，已配置好个人用户名和电子邮件且SSH Key已上传到GitHub上；

## 流程

### 1. (本地)git,修改默认主分支为 **main**。
`remote git config --global init.defaultBranch main`

### 2. 从GitHub上把HelloWorld，克隆到本地。
`git clone git@github.com:54AllenZhang/helloWorld.git`

### 3. 克隆完成后，进入工作区（本地仓库），且创建一个新的分支。
```C
cd helloWorld // 进入仓库
git checkout -b first // 创建一个first分支
git checkout first // 切换分支
```

### 4. 分支创建完成后，开始修改或创建代码或文件。
```C 
echo '第一次修改' > test1.txt // 创建test1.txt文件并写入内容，也可以使用vscode
```

### 5. 修改完成后查看修改
`git diff`

### 6. 提交到暂存区
```
git add test1.txt
```

### 7. 提交到本地仓库
```
git commit -m "第一次提交"
```

### 8. 提交远程新分支
```
git push origin first
```

### 9. 切换分支
`git checkout `

### 10. 远程仓库main分支同步到本地main分支
`git pull origin main`


### 11.  把我的修改扔到一边，然后，把main最新的修改拿过来，接着在最新的修改基础上，再把我的这个commit给尝试弄回去，在这个过程中有可能会有rebase conflict
```
git rebase main
```

### 12. 合并分支
`git push -f origin first`

### 13. 审核或测试完成后，远程仓库合并，并删除分支:打开GitHub并打开helloWorld，仓库并点击**New pull request** -> **aquash and merge** -> **deleta branch**（多个提交，合并为一个提交，并提交到主分支）

### 14. 删除本地分支
```
git checkout main // 切换到主分支
git branch -D first // 删除first分支
```

### 15. 把最新远程主分支同步到本地
```
git pull origin main
```

到这里，一个完整工作流程。