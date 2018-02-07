
#### GIT TAG 大全

##### 列出现有标签

```bash
    git tag
```

##### 列出特定条件标签

```bash
    git tag -l 'v1.1.*'
```

##### 创建标签含备注

```bash
    git tag -a v1.1.0 -m'tag message'
    git tag v1.1.0
```


##### 补充某次提交标签含备注

```bash
    git tag -a v1.1.0 46b3024(commit id） -m'tag message'
    git tag v1.1.0
```

##### 查看某个标签

```bash
    git show v1.1.0
```

##### 推送到远程

```bash
    git push origin v1.1.0
```

##### 一次推送所有tag到远程

```bash
    git push origin --tags
```

##### 回滚Tag

##### 查看某个tag 快照 获取 commit id 3b192c7

```bash
    git tag
    git show v.1.1.0
```

##### 版本回退

```bash
    git reset --hard 3b192c7
```

##### 拉取分支

```bash
    git checkout -b bugfix
    git branch
```

##### 主干分支立即回到原来的位置

```bash
    git checkout master
    git reflog // 最近一次提交commit id 296827f
    git reset --hard 296827f
```

##### 切换到bugfix分支，修改bug

```bash
    git checkout bugfix
    git add .
    git commit -m"修复bug"
    git tag v1.1.1
```

##### 合并到主干上

```bash
    git checkout master
    git merge bugfix //有冲突解决冲突
```

##### 推送标签到远程

```bash
    git push origin --tags
```
