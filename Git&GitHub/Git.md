# Git & GitHub

## Git

### 1. 用户配置
```python
git config --global user.name "XXXX" # XXXX为个人用户名
git config --global user.email "youremail@example.com" # 配置个人电子邮件
ssh-keygen -t rsa -C "youremail@example.com" # 配置SSH Key
```

### 2. 创建仓库
```python
git init # 使用当前文件夹作为本地仓库并初始化。
git init first # 创建一个名为“first”的本地仓库
```

### 3. 克隆仓库
```Git
git clone <repo's url>   # 克隆仓库到当前目录
git clone <repo's url> <文件夹名> # 克隆仓库到指定文件夹
```

### 4. 提交与修改
```
git add xxx     # 添加文件到暂存区
git status      # 查看仓库当前的姿态，显示有变更的文件。
git diff        # 比较文件的不同，即暂存区和工作区的差异。
git commit      # 提交暂存区到本地仓库
git reset       # 回退版本。
git rm          # 将文件暂存区和工作区中删除
git mv          # 移动或重命名工作区文件
```