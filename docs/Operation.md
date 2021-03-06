# 本地版本库操作

* 文件新修改：
``` bash
$ git add <fileName>  # 添加指定文件到版本库
$ git add .           # 添加所有文件到版本库
```

* 删除add的文件
``` base
$ git rm <fileName>
```

* 回退文件修改(新添/删除/修改)
``` base
$ git checkout -- <fileName>
```
场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。

* 回退add文件新添/修改
``` base
$ git reset HEAD <fileName>
```
场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD file，就回到了场景1，第二步按场景1操作

* 回退commit文件新添/修改
``` base
$ git reset --hard commit_id    # 回退到指定版本
$ git reset --hard HEAD^^       # 回退到上一版本
```
场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交

* 更新本地版本库
``` base
$ git commit -m "message"
```

* 提交至线上版本库
``` base
$ git push origin <master|name>
```