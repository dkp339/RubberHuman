** Git使用指北 **
git add README.md #添加文件到本地仓库
git rm README.md #本地倒库内删除
git commit -m "first commit" #提交到本地库并备注，此时变更仍在本地。
git commit -a  ##自动更新变化的文件，a可以理解为auto
git remote add xxx git@github.com:xxx/xxx.git  #增加一个远程服务器的别名。
git remote rm xxx   ##删除远程版本库的别名
git push -u remotename master #将本地文件提交到Github的remoname版本库中。此时才更新了本地变更到github服务上
