``sh
git clone repositorio origen

git clone https://github.com/romancete85/AWSProjects.git

 git remote -v

 ``
origin  https://github.com/romancete85/AWSProjects.git (fetch)
origin  https://github.com/romancete85/AWSProjects.git (push)
ubuntu:~/filesystem/AWSProjects$ git branch                
* main
ubuntu:~/filesystem/AWSProjects$ git push origin:main
ssh: Could not resolve hostname origin: Name or service not known
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
ubuntu:~/filesystem/AWSProjects$ git push main:main  
ssh: Could not resolve hostname main: Name or service not known
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
ubuntu:~/filesystem/AWSProjects$ git add .         
warning: adding embedded git repository: springboot-aws-deploy
hint: You've added another git repository inside your current repository.
hint: Clones of the outer repository will not contain the contents of
hint: the embedded repository and will not know how to obtain it.
hint: If you meant to add a submodule, use:
hint: 
hint:   git submodule add <url> springboot-aws-deploy
hint: 
hint: If you added this path by mistake, you can remove it from the
hint: index with:
hint: 
hint:   git rm --cached springboot-aws-deploy
hint: 
hint: See "git help submodule" for more information.
ubuntu:~/filesystem/AWSProjects$ cd springboot-aws-deploy/

``sh
ubuntu:~/filesystem/AWSProjects/springboot-aws-deploy$ git remote -v
origin  https://github.com/kodedge-swapneel/springboot-aws-deploy.git (fetch)
origin  https://github.com/kodedge-swapneel/springboot-aws-deploy.git (push)
ubuntu:~/filesystem/AWSProjects/springboot-aws-deploy$ git remote add 

``
usage: git remote add [<options>] <name> <url>

    -f, --[no-]fetch      fetch the remote branches
    --[no-]tags           import all tags and associated objects when fetching
                          or do not fetch any tag at all (--no-tags)
    -t, --[no-]track <branch>
                          branch(es) to track
    -m, --[no-]master <branch>
                          master branch
    --[no-]mirror[=(push|fetch)]
                          set up remote as a mirror to push to or fetch from

ubuntu:~/filesystem/AWSProjects/springboot-aws-deploy$ git remote add -f
usage: git remote add [<options>] <name> <url>

    -f, --[no-]fetch      fetch the remote branches
    --[no-]tags           import all tags and associated objects when fetching
                          or do not fetch any tag at all (--no-tags)
    -t, --[no-]track <branch>
                          branch(es) to track
    -m, --[no-]master <branch>
                          master branch
    --[no-]mirror[=(push|fetch)]
                          set up remote as a mirror to push to or fetch from
``sh
git remote add roman https://github.com/romancete85/AWSProjects.git
git remote -v
origin  https://github.com/kodedge-swapneel/springboot-aws-deploy.git (fetch)
origin  https://github.com/kodedge-swapneel/springboot-aws-deploy.git (push)
roman   https://github.com/romancete85/AWSProjects.git (fetch)
roman   https://github.com/romancete85/AWSProjects.git (push)
git push roman origin:main
Username for 'https://github.com': romancete85
Password for 'https://romancete85@github.com': 
To https://github.com/romancete85/AWSProjects.git
 ! [rejected]        origin/HEAD -> main (fetch first)
error: failed to push some refs to 'https://github.com/romancete85/AWSProjects.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
``
``sh
git fetch roman
``
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 1.11 KiB | 1.11 MiB/s, done.
From https://github.com/romancete85/AWSProjects
 * [new branch]      main       -> roman/main
``sh
git branch``

* main
``sh
git checkout main
``
Already on 'main'
Your branch is up to date with 'origin/main'.
``sh
git pull roman main
``
From https://github.com/romancete85/AWSProjects
 * branch            main       -> FETCH_HEAD
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint: 
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint: 
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.
``sh
git status
``sh
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
ubuntu:~/filesystem/AWSProjects/springboot-aws-deploy$ cd ..       
``sh
git add springboot-aws-deploy/
git status
``sh
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   springboot-aws-deploy

``sh
git commit -m "awsspring1"
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'root@ubuntu.(none)')
``sh
git config --global user.email "romanfandrich@hotmail.com"
ubuntu:~/filesystem/AWSProjects$ git config --global user.name "romancete85"
ubuntu:~/filesystem/AWSProjects$ git commit -m "awsspring1"
[main e8047c9] awsspring1
 1 file changed, 1 insertion(+)
 create mode 160000 springboot-aws-deploy
ubuntu:~/filesystem/AWSProjects$ git push       
Username for 'https://github.com': romancete85
Password for 'https://romancete85@github.com': 
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 283 bytes | 283.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/romancete85/AWSProjects.git
   f399bd7..e8047c9  main -> main
ubuntu:~/filesystem/AWSProjects$ 
``
