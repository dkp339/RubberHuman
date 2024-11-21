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
- `remoname` 为远程版本库的别名，`master` 为主分支。
- 此时才更新了本地变更到 GitHub 服务上。
```bash
git push -u remotename master
```

---

