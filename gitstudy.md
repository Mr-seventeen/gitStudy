
###non-fast-forward
    qixiujuan@QIXIUJUAN MINGW64 /e/git (branch-copy)
    $ git pull origin test_branch:branch-copy
    From https://github.com/Mr-seventeen/gitStudy
    ! [rejected]        test_branch -> branch-copy  (non-fast-forward)


###`git pull`
再分支上执行`git pull`如下，git返回的提示很清楚，是由于当前分支与远程分支没有关联造成的，如果想要执行`git pull`提示了两种方法，一个是指定pull的远程分支，这样操作后，在该本地分支会有远程指定分支的内容，但与指定的远程分支没有关联关系；另一个就是建立和远程分支的关系

    $ git pull
    There is no tracking information for the current branch.
    Please specify which branch you want to merge with.
    See git-pull(1) for details.

        git pull <remote> <branch>

    If you wish to set tracking information for this branch you can do so with:

        git branch --set-upstream-to=origin/<branch> branch-copy

下图是执行`git pull <remote> <branch>`后分支的关联关系
![](/img/git-pull-1.1.png)   
![](/img/git-pull-1.2.png)   
下图是执行` git branch --set-upstream-to=origin/<branch> branch-copy`后分支的关联关系
![](/img/git-pull-1.3.png)   
![](/img/git-pull-1.4.png)   


    //有远程关联分支的切换，切换后显示
    qixiujuan@QIXIUJUAN MINGW64 /e/git (branch-copy)
    $ git checkout master
    Switched to branch 'master'
    Your branch is up to date with 'origin/master'.
    //无远程关联分支的切换
    qixiujuan@QIXIUJUAN MINGW64 /e/git (master)
    $ git checkout branch-copy
    Switched to branch 'branch-copy'