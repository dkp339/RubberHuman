# Git使用指北

## 基本命令说明

### 添加文件到本地仓库
```bash
git add README.md
```

### 从本地仓库中删除文件
```bash
git rm README.md
```

### 提交到本地库并备注（变更仍在本地）
```bash
git commit -m "first commit"
```

### 自动更新变化的文件
- `-a` 可以理解为 `auto`，即自动将所有已跟踪文件的改动提交。
```bash
git commit -a
```

### 增加一个远程服务器的别名
```bash
git remote add xxx git@github.com:xxx/xxx.git
```

### 删除远程版本库的别名
```bash
git remote rm xxx
```

### 提交本地文件到 GitHub 的远程版本库
- `remotename` 为远程版本库的别名，`master` 为主分支。
- `-u` 是 `--set-upstream` 的简写。它的作用是将当前分支与远程仓库的某个分支关联起来，并且在以后的 `git push` 和 `git pull` 操作中，不需要再指定远程分支的名称。通过这种方式，Git 会记住远程分支的信息，方便后续操作。
- 此时才更新了本地变更到 GitHub 服务上。
```bash
git push -u remotename master
```

## 下载方式
### 以 git readonly 方式克隆到本地（只读）
```bash
git clone git://github.com:xxxx/test.git
```

### 以 SSH 方式克隆到本地（读写）
```bash
git clone git@github.com:xxx/test.git
```

### 以 HTTPS 方式克隆到本地（读写）
```bash
git clone https://github.com/xxx/test.git
```

### 获取内容到本地但不合并
```bash
git fetch git@github.com:xxx/xxx.git
```

### 获取并合并内容到本地
```bash
git pull git@github.com:xxx/xxx.git
```

## 分支操作

### 创建分支
```bash
git branch          # 显示当前分支是 master
git branch new_bra  # 创建分支命名为 new_bra
git checkout new_bra  # 切换到新分支
git add branch.txt
git commit -m "added branch.txt"
git push readme_test new_bra  # 提交分支到远程服务器
```

### 合并分支
```bash
git checkout master         # 切换到主干
git merge new_bra           # 合并 new_bra 分支到主干
git branch                  # 显示当前分支是 master
git push readme_test master # 提交主干更新到远程
```

---

## 其他命令

### 更新远程分支列表
```bash
git remote update 别名 --prune
```

### 查看所有分支
```bash
git branch -a
```

### 删除远程分支
```bash
git push 别名 --delete 分支名
```

### 删除本地分支
```bash
git branch -d 分支名
```
