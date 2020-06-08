push to origin/master was rejected错误解决方案

idea中，发布项目到OSChina的Git中，当时按照这样的流程添加Git，然后push，提示：push to origin/master war rejected"。

解决方案如下：

1.切换到自己项目所在的目录，右键选择GIT BASH Here

2.在terminl窗口中依次输入命令：

git pull

git pull origin master

git pull origin master --allow-unrelated-histories

3.在idea中重新push自己的项目，成功！！！



chenzeming@chenzeming-thinkpad-t420:~/Documents/Java/PopularFramework/Git/git-test-project$ git pullThere is no tracking information for the current branch.
Please specify which branch you want to rebase against.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> master

chenzeming@chenzeming-thinkpad-t420:~/Documents/Java/PopularFramework/Git/git-test-project$ git pull origin master
fatal: couldn't find remote ref master
chenzeming@chenzeming-thinkpad-t420:~/Documents/Java/PopularFramework/Git/git-test-project$ git pull origin master --allow-unrelated-histories
fatal: couldn't find remote ref master
chenzeming@chenzeming-thinkpad-t420:~/Documents/Java/PopularFramework/Git/git-test-project$ git pushfatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin master

chenzeming@chenzeming-thinkpad-t420:~/Documents/Java/PopularFramework/Git/git-test-project$ git push origin master
Username for 'https://github.com': goldman99999
Password for 'https://goldman99999@github.com': 
Enumerating objects: 36, done.
Counting objects: 100% (36/36), done.
Delta compression using up to 4 threads
Compressing objects: 100% (15/15), done.
Writing objects: 100% (36/36), 2.65 KiB | 903.00 KiB/s, done.
Total 36 (delta 6), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (6/6), done.

******************************************************************************************************************************************
####################   idea push master to origin/master was rejected by remote
******************************************************************************************************************************************
remote: error: GH007: Your push would publish a private email address.
remote: You can make your email public or disable this protection by visiting:
remote: http://github.com/settings/emails
******************************************************************************************************************************************

To https://github.com/goldman99999/git-test.git
 ! [remote rejected] master -> master (push declined due to email privacy restrictions)
error: failed to push some refs to 'https://github.com/goldman99999/git-test.git'
chenzeming@chenzeming-thinkpad-t420:~/Documents/Java/PopularFramework/Git/git-test-project$ git push origin master
Username for 'https://github.com': goldman99999
Password for 'https://goldman99999@github.com': 
Enumerating objects: 36, done.
Counting objects: 100% (36/36), done.
Delta compression using up to 4 threads
Compressing objects: 100% (15/15), done.
Writing objects: 100% (36/36), 2.65 KiB | 542.00 KiB/s, done.
Total 36 (delta 6), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (6/6), done.
To https://github.com/goldman99999/git-test.git
 * [new branch]      master -> master
=====================================================================

