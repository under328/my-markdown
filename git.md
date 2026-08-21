#### Git命令速查表
`master`: 默认开发分支
`origin`: 默认远程版本库

`Head`: 默认开发分支
`Head^`: Head的父提交

`创建版本库`

| 命令 | 功能 | 作用 |
| --- | --- | --- |
| `git clone <url>` | 克隆远程版本库 | |
| `git init` | 初始化本地版本库 | 使当前目录成为一个git仓库 |

`修改和提交`

| 命令 | 功能 | 作用 |
| --- | --- | --- |
| `git status` | 查看状态 | |
| `git diff` | 查看变更内容 | |
| `git add .` | 跟踪所有改动过的文件 | |
| `git add <file>` | 跟踪指定的文件 | |
| `git mv <old> <new>` | 文件改名 | |
| `git rm <file>` | 删除文件 | |
| `git rm --cached <file>` | 停止跟踪文件但不删除 | |
| `git commit -m "commit message"` | 提交所有更新过的文件 | |
| `git commit -amend` | 修改最后一次提交 | |

`查看历史提交`

| 命令 | 功能 | 作用 |
| --- | --- | --- |
| `git log` | 查看提交历史 | |
| `git log -p <file>` | 查看指定文件的提交历史 | |
| `git blame <file>` | 以列表方式查看指定文件的提交历史 | |

`撤销`

| 命令 | 功能 | 作用 |
| --- | --- | --- |
| `git reset --hard HEAD` | 撤销工作目录中所有未提交文件的修改内容 | |
| `git checkout HEAD <file>` | 撤销指定的未提交文件的修改内容 | |
| `git revert <commit>` | 撤销指定的提交 | |

`分支与标签`

| 命令 | 功能 | 作用 |
| --- | --- | --- |
| `git branch` | 显示所有本地分支 | |
| `git checkout <branch/tag>` | 切换到指定分支或标签 | |
| `git branch <new-branch>` | 创建新分支 | |
| `git branch -d <branch>` | 删除本地分支 | |
| `git tag` | 列出所有本地标签 | |
| `git tag <tag name>` | 基于最新提交创建标签 | |
| `git tag -d <tag name>` | 删除标签 | |

`合并与衍合`

| 命令 | 功能 | 作用 |
| --- | --- | --- |
| `git merge <branch>` | 合并指定分支到当前分支 | |
| `git rebase <branch>` | 衍合指定分支到当前分支 | |

`远程操作`

| 命令 | 功能 | 作用 |
| --- | --- | --- |
| `git remote -v` | 查看远程版本库信息 | |
| `git remote show <remote>` | 查看指定远程版本库信息 | |
| `git remote add <remote> <url>` | 添加远程版本库 | |
| `git fetch <remote>` | 从远程库获取代码 | |
| `git pull <remote> <branch>` | 下载代码及快速合并 | |
| `git push <remote> <branch>` | 上传代码及快速合并 | |
| `git push <remote> :<branch/tag-name>` | 删除远程分支或标签 | |
| `git push --tags` | 上传所有标签 | |

#### Git常用命令
- 设置用户签名 ———— git config --global user.name litao
- 设置用户签名 ———— git config --global user.email 964374951@qq.com
- 初始化本地库 ———— git init
- 查看本地库状态 ———— git status
- 添加到暂存区 ———— git add .
- 提交到本地库 ———— git commit -m "feat:日志信息"
- 添加并提交到本地库 ———— git commit -am "feat:日志信息"
- 查看历史记录 ———— git reflog/git log
- 版本穿梭 ———— git reset --hard 版本号
#### 分支操作
- 创建分支 ———— git branch 分支名
- 查看分支 ———— git branch -v（r 远程、a 所有、v 本地）
- 切换分支 ———— git checkout 分支名
- 把指定的分支合并到当前分支上 ———— git merge 需要合并的分支名
- 创建并切换到新分支 ———— git checkout -b new-feature
- 切换到远程分支 ———— git checkout -t origin/feature-branch
- 恢复文件 ———— git checkout HEAD -- file.txt
- 删除分支 ———— git branch -d 分支名
- 重命名分支 ———— git branch -m <old-branch> <new-branch>
#### 从远程库拉取文件
- 初始化 ————  git init
- 链接仓库 ———— git remote add origin https://github.com/under328/hollow-knight-pixel.git
- 拉取项目 ———— git pull origin master
#### 将文件上传到远程库
- 添加到暂存区 ———— git add .
- 提交到本地库 ———— git commit -m "feat：提交代码"
- 创建分支（第一次） ———— git branch -M main
- 链接仓库（第一次） ———— git remote add origin https://github.com/under328/hollow-knight-pixel.git
- 关联并提交代码到分支（第一次） ———— git push -u origin main
- 提交代码 ———— git push
#### 克隆项目
- git clone https://github.com/under328/hollow-knight-pixel.git
#### 日志类型
- feat ： 新功能
- fix ： 修补bug
- docs：文档
- style：格式
- refactor：重构
- test ： 增加测试
- chore：构建过程或辅助工具的变动
