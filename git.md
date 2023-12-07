```
git merge	foo	在当前分支上合并foo分支
git rebase	a b	将b合并到a上,并且当前分支变为b
git rebase c	将当前分支合并到c上
HEAD 指向当前分支最近一次提交记录,大多数的提交修改树的git命令都是从改变HEAD的指向开始的
^~相对引用	(^2第二个父级)
git branch -f main HEAD^	将main分支强制指向HEAD的第三级父级
git reset	通过把分支记录回退几个提交记录来实现撤销改动
git cherry-pick想要一些提交复制到当前所在位置(HEAD)下面
git rebase -i HEAD~4 pick了HEAD前4个,并移动顺序
git commit --amend
git tag tagname C1	创建一个指向C1的标签
get describe C5描述离当前ref最近的标签

```

[详细链接](https://it.cha138.com/php/show-60895.html#2__80)