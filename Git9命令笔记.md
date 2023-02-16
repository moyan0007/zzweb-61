# Git命令

## 1.仓库初始化

```shell
git init
```

## 2.追踪文件

```shell
git add 文件名
```

## 3.查看状态

```shell
git status
git status -s #精简显示
```

## 4.提交到仓库

```shell
git commit -m '描述内容'
```

## 5.跳过暂存区

```shell
git  commit -a -m '描述内容'
```

## 6.一次性添加到暂存区

```shell
git add .
```

## 7.撤销对文件的修改

```shell
git checkout -- 文件名
```

## 8.移除暂存文件

```shell
git reset HEAD 文件名
git reset HEAD . #移除全部文件
```

## 9.删除文件

```shell
# 从 Git仓库和工作区中同时移除 index.js 文件
git rm -f index.js
# 只从 Git 仓库中移除 index.css，但保留工作区中的 index.css 文件
git rm --cached index.css
```

## 10.查看历史记录

```shell
# 按时间先后顺序列出所有的提交历史，最近的提交在最上面
git log
# 只展示最新的两条提交历史，数字可以按需进行填写
git log -2
# 在一行上展示最近两条提交历史的信息
git log -2 --pretty=oneline
# 在一行上展示最近两条提交历史信息，并自定义输出的格式
# &h 提交的简写哈希值 %an 作者名字 %ar 作者修订日志 %s 提交说明
git log -2 --pretty=format:"%h | %an | %ar | %s"
```

## 11.**回退到指定的版本** 

```css
# 在一行上展示所有的提交历史
git log --pretty=oneline
# 使用 git reset --hard 命令，根据指定的提交 ID 回退到指定版本
git reset --hard 
# 在旧版本中使用 git reflog --pretty=oneline 命令，查看命令操作的历史
git reflog 
# 再次根据最新的提交 ID，跳转到最新的版本
git reset --hard 
```

