![](RackMultipart20220317-4-129bvi1_html_f3e31080746ea320.png)

=============

**GitHub For Dummies**

tpreddy@tpreddy MINGW64 /d/Labs/github-for-dummies (master)

$ git --version

git version 2.26.1.windows.1

tpreddy@tpreddy MINGW64 /d/Labs/github-for-dummies

$ git init

Initialized empty Git repository in D:/Labs/github-for-dummies/.git/

tpreddy@tpreddy MINGW64 /d/Labs/github-for-dummies (master)

$

==============

**The Git &amp; Github Bootcamp**

**Configuring Git Name and Email**

#Configure name that git will associate the work

tpreddy@tpreddy MINGW64 ~

$ git config --global user.name &quot;way2aws&quot;

#Show name that git is associating the work

tpreddy@tpreddy MINGW64 ~

$ git config user.name

Way2aws

#Configure name that git will associate the work

tpreddy@tpreddy MINGW64 ~

$ git config --global user.email &quot;way2aws0621@gmail.com&quot;

#Show name that git is associating the work

tpreddy@tpreddy MINGW64 ~

$ git config user.emial

way2aws0621@gmial.com

**Git init and status**

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel

$ git status

fatal: not a git repository (or any of the parent directories): .git

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel

$ git init

Initialized empty Git repository in D:/Labs/gitBootcamp/MyFirstNovel/.git/

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

No commits yet

nothing to commit (create/copy files and use &quot;git add&quot; to track)

![Picture 1](RackMultipart20220317-4-129bvi1_html_397327dd0634a7e3.gif)

By default files will be in Working directory

Git add moves the files to staging area (logically marked)

Git commit moves all files in staging area to repository.

![](RackMultipart20220317-4-129bvi1_html_9d95127eda941687.png)

**Git Add :** Used to add specific files to staging area.

# git add file1 file2

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ touch characters.txt outline.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ ls -l

total 0

-rw-r--r-- 1 tpreddy 197121 0 Mar 8 16:01 characters.txt

-rw-r--r-- 1 tpreddy 197121 0 Mar 8 16:01 outline.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

No commits yet

Untracked files:

(use &quot;git add \&lt;file\&gt;...&quot; to include in what will be committed)

characters.txt

outline.txt

nothing added to commit but untracked files present (use &quot;git add&quot; to track)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git add outline.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

No commits yet

Changes to be committed:

(use &quot;git rm --cached \&lt;file\&gt;...&quot; to unstage)

new file: outline.txt

Untracked files:

(use &quot;git add \&lt;file\&gt;...&quot; to include in what will be committed)

characters.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

No commits yet

Changes to be committed:

(use &quot;git rm --cached \&lt;file\&gt;...&quot; to unstage)

new file: characters.txt

new file: outline.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$

**Git Commit:** Used to commit changes from staging area.

# git commit -m &quot;message&quot;

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git commit -m &quot;Started working on outline and characters&quot;

[master (root-commit) d800750] Started working on outline and characters

2 files changed, 0 insertions(+), 0 deletions(-)

create mode 100644 characters.txt

create mode 100644 outline.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

**nothing to commit** , working tree clean

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master) # created new file

$ touch chapter1.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ cat outline.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master) # modified file content.

$ echo &quot;Line 1&quot; \&gt; outline.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

Changes not staged for commit:

(use &quot;git add \&lt;file\&gt;...&quot; to update what will be committed)

(use &quot;git restore \&lt;file\&gt;...&quot; to discard changes in working directory)

modified: outline.txt

Untracked files:

(use &quot;git add \&lt;file\&gt;...&quot; to include in what will be committed)

chapter1.txt

no changes added to commit (use &quot;git add&quot; and/or &quot;git commit -a&quot;)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git add chapter1.txt outline.txt

warning: LF will be replaced by CRLF in outline.txt.

The file will have its original line endings in your working directory

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

Changes to be committed:

(use &quot;git restore --staged \&lt;file\&gt;...&quot; to unstage)

new file: chapter1.txt

modified: outline.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git commit -m &quot;Started working on chapter1.txt&quot;

[master a532534] Started working on chapter1.txt

2 files changed, 1 insertion(+)

create mode 100644 chapter1.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

nothing to commit, working tree clean

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git log

commit a532534afcd3c68433626b0cef31466847c89276 (HEAD -\&gt; master)

Author: pavannav \&lt;pavan.nav@gmail.com\&gt;

Date: Tue Mar 8 17:23:28 2022 -0600

Started working on chapter1.txt

commit d800750734d05892b049278d08903208b8ceecb7

Author: pavannav \&lt;pavan.nav@gmail.com\&gt;

Date: Tue Mar 8 17:10:15 2022 -0600

Started working on outline and characters

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ echo &quot;Line 2 in outline&quot; \&gt;\&gt; outline.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ touch chapter2.txt ; echo &quot;Line one in chapter2&quot; \&gt; chapter2.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ ls -l

total 2

-rw-r--r-- 1 tpreddy 197121 0 Mar 8 17:19 chapter1.txt

-rw-r--r-- 1 tpreddy 197121 21 Mar 9 09:55 chapter2.txt

-rw-r--r-- 1 tpreddy 197121 0 Mar 8 16:01 characters.txt

-rw-r--r-- 1 tpreddy 197121 25 Mar 9 09:54 outline.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

Changes not staged for commit:

(use &quot;git add \&lt;file\&gt;...&quot; to update what will be committed)

(use &quot;git restore \&lt;file\&gt;...&quot; to discard changes in working directory)

modified: outline.txt

Untracked files:

(use &quot;git add \&lt;file\&gt;...&quot; to include in what will be committed)

chapter2.txt

no changes added to commit (use &quot;git add&quot; and/or &quot;git commit -a&quot;)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git add .

warning: LF will be replaced by CRLF in outline.txt.

The file will have its original line endings in your working directory

warning: LF will be replaced by CRLF in chapter2.txt.

The file will have its original line endings in your working directory

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

Changes to be committed:

(use &quot;git restore --staged \&lt;file\&gt;...&quot; to unstage)

new file: chapter2.txt

modified: outline.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git commit -m &quot;edited outline and added new file chapter2&quot;

[master f0e325d] edited outline and added new file chapter2

2 files changed, 2 insertions(+)

create mode 100644 chapter2.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

nothing to commit, working tree clean

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

**Exercise:**

[https://www.notion.so/Committing-Basics-Exercise-3dc1ef1873ce45e68cedd2265710d7d8](https://www.notion.so/Committing-Basics-Exercise-3dc1ef1873ce45e68cedd2265710d7d8)

![Picture 3](RackMultipart20220317-4-129bvi1_html_23653fada11a5be2.gif)

It is recommended officially to write commit messages in present tense like &quot;make abc to xyz&quot; instead of &quot;made abc to xyz&quot;. However it is better to follow organization guidelines. There is a big debate on this.

Ideally we use 1 line commit messages, how ever if we want to write multiple lines we just say git commit and this will open an editor to write the comments.

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git commit

This will open default editor, vi in this case. We have to enter the message in it and save it.

$ git log --oneline

**Amending Commits:**

$ git commit -m &#39;commit message&#39;

$ git add forgotten\_file

$ git commit --amend

**Git ignore**

[https://www.toptal.com/developers/gitignore](https://www.toptal.com/developers/gitignore)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ touch secrets.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

Untracked files:

(use &quot;git add \&lt;file\&gt;...&quot; to include in what will be committed)

secrets.txt

nothing added to commit but untracked files present (use &quot;git add&quot; to track)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ touch .gitignore

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ echo &quot;secrets.txt&quot; \&gt;\&gt; .gitignore

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ cat .gitignore

secrets.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

Untracked files:

(use &quot;git add \&lt;file\&gt;...&quot; to include in what will be committed)

.gitignore

nothing added to commit but untracked files present (use &quot;git add&quot; to track)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git add .

warning: LF will be replaced by CRLF in .gitignore.

The file will have its original line endings in your working directory

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git status

On branch master

Changes to be committed:

(use &quot;git restore --staged \&lt;file\&gt;...&quot; to unstage)

new file: .gitignore

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/MyFirstNovel (master)

$ git commit -m &quot; add gitignore file&quot;

[master 4b601b2] add gitignore file

1 file changed, 1 insertion(+)

create mode 100644 .gitignore

**Branching**

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp

$ mkdir Roadtrip

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp

$ cd Roadtrip/

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip

$ git init

Initialized empty Git repository in D:/Labs/gitBootcamp/Roadtrip/.git/

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ touch playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ echo &quot;SONG - ARTIST&quot; \&gt;\&gt; playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ echo &quot;=========&quot; \&gt;\&gt; playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git status

On branch master

No commits yet

Untracked files:

(use &quot;git add \&lt;file\&gt;...&quot; to include in what will be committed)

playlist.txt

nothing added to commit but untracked files present (use &quot;git add&quot; to track)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git add .

warning: LF will be replaced by CRLF in playlist.txt.

The file will have its original line endings in your working directory

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git log

fatal: your current branch &#39;master&#39; does not have any commits yet

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git commit -m &quot; add playlist.txt&quot;

[master (root-commit) d8c4f4e] add playlist.txt

1 file changed, 2 insertions(+)

create mode 100644 playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git log

commit d8c4f4e6e956c854af0ed4a84887268ac720b693 (HEAD -\&gt; master)

Author: pavannav \&lt;pavan.nav@gmail.com\&gt;

Date: Wed Mar 9 16:34:48 2022 -0600

add playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ echo &quot;sos - abba&quot; \&gt;\&gt; playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ echo &quot;one of us - abba&quot; \&gt;\&gt; playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git status

On branch master

Changes not staged for commit:

(use &quot;git add \&lt;file\&gt;...&quot; to update what will be committed)

(use &quot;git restore \&lt;file\&gt;...&quot; to discard changes in working directory)

modified: playlist.txt

no changes added to commit (use &quot;git add&quot; and/or &quot;git commit -a&quot;)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git add .

warning: LF will be replaced by CRLF in playlist.txt.

The file will have its original line endings in your working directory

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git commit -m &quot;added 2 songs&quot;

[master 031c30c] added 2 songs

1 file changed, 2 insertions(+)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git status

On branch master

nothing to commit, working tree clean

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git log

commit 031c30cebee10647d0b41a711106122afda9d0d4 (HEAD -\&gt; master)

Author: pavannav \&lt;pavan.nav@gmail.com\&gt;

Date: Wed Mar 9 16:39:05 2022 -0600

added 2 songs

commit d8c4f4e6e956c854af0ed4a84887268ac720b693

Author: pavannav \&lt;pavan.nav@gmail.com\&gt;

Date: Wed Mar 9 16:34:48 2022 -0600

add playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git branch

\* master

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git branch oldies

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git branch

\* master

oldies

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git log

commit 031c30cebee10647d0b41a711106122afda9d0d4 ( **HEAD -\&gt;**  **master**** , **** oldies**)

Author: pavannav \&lt;pavan.nav@gmail.com\&gt;

Date: Wed Mar 9 16:39:05 2022 -0600

added 2 songs

commit d8c4f4e6e956c854af0ed4a84887268ac720b693

Author: pavannav \&lt;pavan.nav@gmail.com\&gt;

Date: Wed Mar 9 16:34:48 2022 -0600

add playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git switch oldies

Switched to branch &#39;oldies&#39;

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git status

On branch oldies

nothing to commit, working tree clean

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ echo &quot;song 3&quot; \&gt; playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ echo &quot;song 4&quot; \&gt; playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git status

On branch oldies

Changes not staged for commit:

(use &quot;git add \&lt;file\&gt;...&quot; to update what will be committed)

(use &quot;git restore \&lt;file\&gt;...&quot; to discard changes in working directory)

modified: playlist.txt

no changes added to commit (use &quot;git add&quot; and/or &quot;git commit -a&quot;)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git add playlist.txt

warning: LF will be replaced by CRLF in playlist.txt.

The file will have its original line endings in your working directory

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git commit -m &quot; add song3 and song 4&quot;

[oldies 76ff347] add song3 and song 4

1 file changed, 1 insertion(+), 4 deletions(-)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git log

commit 76ff3472109357bf3addbf90b0134b75112d4de3 (HEAD -\&gt; oldies)

Author: pavannav \&lt;pavan.nav@gmail.com\&gt;

Date: Wed Mar 9 16:43:56 2022 -0600

add song3 and song 4

commit 031c30cebee10647d0b41a711106122afda9d0d4 (master)

Author: pavannav \&lt;pavan.nav@gmail.com\&gt;

Date: Wed Mar 9 16:39:05 2022 -0600

added 2 songs

commit d8c4f4e6e956c854af0ed4a84887268ac720b693

Author: pavannav \&lt;pavan.nav@gmail.com\&gt;

Date: Wed Mar 9 16:34:48 2022 -0600

add playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ cat playlist.txt

song 4

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git switch master

Switched to branch &#39;master&#39;

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ cat playlist.txt

SONG - ARTIST

=========

sos - abba

one of us - abba

- Repeat 7. More practice with Branch.

**Switching Branches with Unstaged Changes**

If we make changes to current commit and try to switch branch without committing, it will throw error

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ echo &quot;song 5&quot; \&gt;\&gt; playlist.txt

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ switch branch master

bash: switch: command not found

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git switch master

error: Your local changes to the following files would be overwritten by checkout:

playlist.txt

**Please commit your changes or stash them before you switch branches.**

**Aborting**

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git commit -a -m &quot;add song 5 to playlist&quot;

warning: LF will be replaced by CRLF in playlist.txt.

The file will have its original line endings in your working directory

[oldies 3d23057] add song 5 to playlist

1 file changed, 1 insertion(+)

However if we create a new file ( which is not tracked), it will carry that file to which ever branch we switch

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git switch -c newsongs

Switched to a new branch &#39;newsongs&#39;

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (newsongs)

$ cat \&gt; newsongs.txt

newsong 1

newsong 2

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (newsongs)

$ git status

On branch newsongs

Untracked files:

(use &quot;git add \&lt;file\&gt;...&quot; to include in what will be committed)

newsongs.txt

nothing added to commit but untracked files present (use &quot;git add&quot; to track)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (newsongs)

$ git switch oldies

Switched to branch &#39;oldies&#39;

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git status

On branch oldies

Untracked files:

(use &quot;git add \&lt;file\&gt;...&quot; to include in what will be committed)

newsongs.txt

nothing added to commit but untracked files present (use &quot;git add&quot; to track)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git switch master

Switched to branch &#39;master&#39;

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git status

On branch master

Untracked files:

(use &quot;git add \&lt;file\&gt;...&quot; to include in what will be committed)

newsongs.txt

nothing added to commit but untracked files present (use &quot;git add&quot; to track)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ cat \&gt; newsongs2.txt

new

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git status

On branch master

Untracked files:

(use &quot;git add \&lt;file\&gt;...&quot; to include in what will be committed)

newsongs.txt

newsongs2.txt

nothing added to commit but untracked files present (use &quot;git add&quot; to track)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (master)

$ git switch oldies

Switched to branch &#39;oldies&#39;

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git status

On branch oldies

Untracked files:

(use &quot;git add \&lt;file\&gt;...&quot; to include in what will be committed)

newsongs.txt

newsongs2.txt

nothing added to commit but untracked files present (use &quot;git add&quot; to track)

tpreddy@tpreddy MINGW64 /d/Labs/gitBootcamp/Roadtrip (oldies)

$ git switch newsongs

Switched to branch &#39;newsongs&#39;

NOTE: While switching branch, If there are un-staged changes, some times it will carry those changes or it wont let us switch the branch.

**Deleting and renaming branches:**

To Delete you should not be on the branch. To rename you should be on branch.

Exercise:

https://www.notion.so/Branching-Exercise-b5460c881d56400cb046357d9a430bf8

$ git checkout  this is older version of switch.

$ git switch -c \&lt;name\&gt;  creates a new branch and switches to it.

$ git commit -a -m  add all files and commit, instead of git add and git commit

===== Skipped all till GitHub

**Merging Branches**

**Comparing Changes With Git Diff**

=====

**Github The Basics**

$ git remote -v # lists remote repository

$ git remote add \&lt;name\&gt; \&lt;url\&gt;

$ git remote add origin \&lt;url\&gt; # ideally name origin is used but it is not mandate

**Scripting**

in scripting and in one liner&#39;s also **set -xe**

x = Debug mode

e = Exit at step it encounters error

**read -s -p**

-s = secret. Input is not displayed

-p = Prompt

$ curl [https://helloacm.com/api/random/?n=10](https://helloacm.com/api/random/?n=10) # this will get a random 10 digit password.

In script we can use it as

PASSWORD=$( curl -sL [https://helloacm.com/api/random/?n=10](https://helloacm.com/api/random/?n=10))

|
#!/bin/bash#set -x -e # -x = debug. -e = Exit if script encounters any error at any step.


 |
| --- |

**Git**

Latest commit is called Head.

**Terraform**

Backend S3 copies state file to s3.

To use backend s3 in terraform main file without credentials in it, host should be configured with &#39;aws configure&#39; or role should be assigned to ec2 instance from where terraform is run.

When using workspaces, the main code will be same. We use different tfvars file for each workspace. The disadvantage here is if we make changes to main code it affects other workspaces also. This is useful if we want to create an exact setup multiple times (Dev/Text/Prod).

Search: Workspace Pros and cons

S3 backend Locking.

Data Sources.

**Docker**

Installing Docker on CentOs manually.

Download these packages and install.

containerd

yum install ./docker-ce-cli-20.10.6-3.el7.x86\_64.rpm

yum install ./docker-ce-20.10.6-3.el7.x86\_64.rpm

systemctl status/start docker

Registry vs Repository: Registry has Repositories. Repositories have Images.

Image size

[root@localhost tpr]# docker pull nginx # By default it will assign

Using default tag: latest # tag Latest

latest: Pulling from library/nginx

69692152171a: Pull complete

30afc0b18f67: Pull complete

596b1d696923: Pull complete

febe5bd23e98: Pull complete

8283eee92e2f: Pull complete

351ad75a6cfa: Pull complete

Digest: sha256:6d75c99af15565a301e48297fa2d121e15d80ad526f8369c526324f0f7ccb750

Status: Downloaded newer image for nginx:latest

docker.io/library/nginx:latest

[root@localhost tpr]# docker images

REPOSITORY TAG IMAGE ID CREATED SIZE

nginx latest d1a364dc548d 7 hours ago 133MB

hello-world latest d1165f221234 2 months ago 13.3kB

# docker ps

# docker ps -a

[root@localhost tpr]# docker run -it nginx bash  i – Interactive, t - terminal

root@694109fd4ccc:/#

root@694109fd4ccc:/# exit  Exit will stop the container.

exit

[root@localhost tpr]#

[root@localhost tpr]# docker start 694109fd4ccc  to start stopped container 694109fd4ccc

[root@localhost tpr]# docker exec -it adoring\_hofstadter  to log into container

&quot;docker exec&quot; requires at least 2 arguments.

root@694109fd4ccc:/# read escape sequence Ctrl + p + q  to exit out of container

[root@localhost tpr]# docker run -d -i -t nginx  d – Detached mode

2bdb76d833fae4aafc22cc5253fed19323e88a432ed605219b25c99990b20636

[root@localhost tpr]# docker run -it --name nginxserver2 --hostname nginxserver2 nginx:latest bash

root@nginxserver2:/#

[root@localhost tpr]# docker stop 2bdb76d833fa 694109fd4ccc

[root@localhost tpr]# docker rm 6ef80063063a afbe77cb5601 2bdb76d833fa 694109fd4ccc c6b14405b576

6

[root@localhost tpr]# docker ps -aq

ee5b015f653d

0a41bfa1a187

b0b23842617f

570652be65c5

[root@localhost tpr]# docker stop $(docker ps -aq)

ee5b015f653d

0a41bfa1a187

b0b23842617f

570652be65c5

[root@localhost tpr]# docker rm $(docker ps -aq) # rm removes container

ee5b015f653d

0a41bfa1a187

b0b23842617f

[root@localhost tpr]# docker rmi d1a364dc548d d1165f221234 # rmi removes container images.

[root@localhost tpr]# docker run --rm -dit nginx bash  --rm will remove container if container exits.

docker exec -it nginx /etc/init.d/nginx restart

**Networking**

NodePort/HostPort: Port on the host.

Container/Target Port: Port on container

[root@localhost tpr]# docker run --rm -dit --hostname nginx3 -p 80:80 --name nginx3 nginx

# hostPort:ContainerPort

[root@localhost tpr]# docker exec -it cont1 bash  to log into container

[root@localhost tpr]# docker exec -it nginx3 apt install net-tools  to run a command in container

[root@localhost tpr]# docker network ls

NETWORK ID NAME DRIVER SCOPE

0012e04ff979 bridge bridge local

eda3c8c37801 host host local

d243d7538a38 none null local

**Create and Push Image to hub.docker.com**

[root@localhost tpr]# docker run -it nginx bash  install all needed SW

[root@localhost tpr]# docker commit 7aba06a1efdf itscloud2020/nginx:v1  Container name

[root@localhost tpr]# docker push itscloud2020/nginx:v1

# docker run --rm -dit --name cont1 --hostname cont1 --network=&quot;bridge&quot; itscloud2020/nginx:v1

# docker run --rm -dit --name cont2 --hostname cont2 --network=&quot;bridge&quot; itscloud2020/nginx:v1

# docker exec cont2 bash /etc/init.d/nginx restart

# docker run --rm -dit --name cont3 --hostname cont3 -p 9000:80 --network=&quot;bridge&quot; itscloud2020/nginx:v1

# docker run --rm -dit --name cont3 --hostname cont3 -p 9100:80 --network=&quot;none&quot; itscloud2020/nginx:v1

# docker run --rm -dit --name cont4 --hostname cont4 -p 9100:80 --network=&quot;none&quot; itscloud2020/nginx:v1

# docker ps

# docker exec cont3 bash /etc/init.d/nginx restart

# docker exec cont4 bash /etc/init.d/nginx restart

[root@localhost tpr]# docker inspect cont1 | grep IPAddress

&quot;SecondaryIPAddresses&quot;: null,

&quot;IPAddress&quot;: &quot;172.17.0.2&quot;,

&quot;IPAddress&quot;: &quot;172.17.0.2&quot;,

[root@localhost tpr]# docker network ls

NETWORK ID NAME DRIVER SCOPE

0012e04ff979 bridge bridge local

eda3c8c37801 host host local

d243d7538a38 none null local

Storage:

[root@localhost tpr]# docker volume create vol1

vol1

[root@localhost tpr]# docker volume create vol2

vol2

[root@localhost tpr]#

[root@localhost tpr]# cd /var/lib//docker/volumes/

[root@localhost volumes]# ll

total 24

brw-------. 1 root root 8, 3 May 25 12:28 backingFsBlockDev

-rw-------. 1 root root 32768 May 27 11:19 metadata.db

drwx-----x. 3 root root 19 May 27 11:19 vol1

drwx-----x. 3 root root 19 May 27 11:19 vol2

[root@localhost tpr]# docker run --rm -dit --name nginx -p 8000:80 -v vol1:/vol1 itscloud2020/nginx:v1

[root@localhost tpr]# docker run -dit nginx bash /etc/init.d/nginx restart

[root@localhost tpr]# docker exec -it nginx bash

root@1516d2e226f6:/vol1# apt update

root@1516d2e226f6:/vol1# apt install git

root@1516d2e226f6:/# cd vol1

root@1516d2e226f6:/vol1# git clone [https://github.com/mavrick202/dockertest1.git](https://github.com/mavrick202/dockertest1.git)

root@1516d2e226f6:/vol1/dockertest1# ls -l

[root@localhost tpr]# ls -l /var/lib/docker/volumes/vol1/\_data/dockertest1/

[root@localhost tpr]# docker run --rm -dit --name nginx -p 8000:80 -v vol1:/usr/share/nginx/html itscloud2020/nginx:v1

[root@localhost tpr]# docker exec -it nginx bash

root@de153a3c258f:/# cd /usr/share/nginx/html/dockertest1

root@de153a3c258f:/usr/share/nginx/html/dockertest1# cp \*.\* ../

now access from browser and check.

[root@localhost tpr]# docker run --rm -dit --name nginx2 -p 9000:80 -v vol1:/usr/share/nginx/html itscloud2020/nginx:v1

[root@localhost tpr]# docker exec -it nginx2 bash /etc/init.d/nginx restart

[root@localhost tpr]# docker volume rm vol1

vol1

[root@localhost tpr]# docker volume rm vol2

vol2

[root@localhost tpr]# cd /var/lib/docker/volumes/

[root@localhost volumes]# ll

total 24

brw-------. 1 root root 8, 3 May 25 12:28 backingFsBlockDev

-rw-------. 1 root root 32768 May 27 12:55 metadata.db

[root@localhost volumes]#

Dockerfile: Dockerfile is used to create container Images

Dockercompose: This is used to deploy whole application. It is for Development, not used in production . Docker compose should be installed separately.

Dockerfile explained: [https://takacsmark.com/dockerfile-tutorial-by-example-dockerfile-best-practices-2018/](https://takacsmark.com/dockerfile-tutorial-by-example-dockerfile-best-practices-2018/)

Publish vs expose

# Docker Cookbook - Second Edition

Ansible – Push architecture

Puppet, Chef – Pull Architecture
