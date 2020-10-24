### 为项目创建远程仓库并创建多分支
+ 关联到某远程仓库
> $ git remote add origin http://github.com/....
+ 将本地的 master 分支推送到远程仓库的 master 分支
> $ git push origin master
+ 创建并切换到本地 dev 分支
> $ git checkout -b dev
+ 将本地的 dev 分支推送到远程仓库的 dev 分支
> $ git push origin dev

### 此时，如果将远程克隆到本地，默认克隆的是 master 分支，如果需要 dev 分支，则需要执行以下命令
+ 将 master 分支克隆到本地 master 分支
> $ git clone http://github.com/....
+ 创建并切换到本地 dev 分支，并且关联到远程 dev 分支，此时本地 dev 就拥有了远程 dev 的内容，不需要额外拉取。
> $ git checkout -b dev origin/dev
+ 当远程 dev 有变化时，需要重新拉取
> $ git pull origin dev