# 个人经历
* 在进入饥人谷学习之前, 已经接触过前端开发, 感觉自学的方向不明确,不系统,试听了谷里的一些课程, 毅然投入到系统班课程中, 学习中感觉方方老师知识讲的很细致,学习起来比自己摸索快很多.感谢.

# git基本使用
1. git init ; 初始化 创建一个.git目录 当本地仓库
2. git add 文件路径; 选择变化的文件进行提交
3. .gitignore; 描述那些文件是不需要提交的
4. git commit -v; 提交已经添加的文件, 并打开编辑器编写日志; 也可git commit -m 字符串; 在命令行中说明理由并提交, 如果字符串中有空格需要用引号括起来
5. git log; 打印出已经提交的各个版本信息(带有版本号);
6. git reset --hard 版本号(git log查询出来的); 回退到某个版本
7. git reflog; 打印历史变更的所以版本,以及版本号
8. git branch x(分支名称); 基于当前commit创建一个新的分支,我在那个分支提交,代码就在那个分支
9. git checkout x(分支名称); 用于切换分支
10. 合并分支:首先进入要保留的分支; 运行 git merge x(需要合并的名称) 进行合并, 合并完成后删除无用分支 git branch -d x(分支名称)
11. git add . 提交当前目录所以文件
12. git branch; 可显示当前在那个分支
13. git status -sb; 显示冲突文件

# git与github远程仓库配合使用

## 生成ssh key
1. 运行ssh-keygen -t rsa -b 4096 -C 自己的邮箱
2. cat ~/.ssh/id_rsa.pub 获取公钥内容, 并粘贴到github上
3. ssh -T git@github.com 测试是否配对成功
4. git remote add origin git@xxxxxxx; 在本地添加远程地址仓库
5. git push -u origin master; 把本地master分支推送到远程origin的master分支
6. 在本地修改与远程代码无冲突的情况下，优先使用:pull->commit->push
7. 在本地修改与远程代码有冲突的情况下，优先使用：commit->pull->push
8. 出现冲突后,git-status -sb; 显示冲突文件,手动更改冲突文件,更改完成后,git add 冲突文件, git commit

   