# MEMO GIT

This repo contains my pesonnal GIT command help guide



Contents
========

 * [1. init](#init)
 * [2. status](#status)
 * [3. add](#add)
 * [4. commit](#commit)
 * [5. branch](#branch)
 * [6. checkout](#checkout)
 * [7. merge](#merge)
 * [8. rebase](#rebase)
 * [9. revert](#revert)
 * [10. reset](#reset)
 * [11. tag](#tag)
 * [12. log](#log)


------------

<a name="init"></a>
## 1. init

Init the GIT repo localy. That's all.


<br />


<a name="status"></a>
## 2. status

Give the local repo state. ?????? 


<br />


<a name="add"></a>
## 3. add [file]

That command is used to select one or files to be send to the staging area.
<pre>
$ git add . 
</pre>
This command send ALL modified files to the staging area, this is A BAD WAY.
<br />
Commit must be as precise as possible, so commited changes must relatited.


<br />


<a name="commit"></a>
## 4. commit -m "message"

Tell GIT "ok those files are in same 'block of changes', you can place a milestone here".
Option -m add a message to commit, this is important.


<br />


<a name="branch"></a>
## 5. branch

This command have several behaviour according to options :
<pre>
$ git branch
</pre>
Will give all branch names. '\*' indicates the current branch (working on)
<br />
<pre>
$ git branch -M oldBranch newBranch
</pre>
Will rename the oldBranch if specified, if not the current one will be renamed.


<br />


<a name="checkout"></a>
## 6. checkout [somewhere]

Move to the specified commit, or anything that refer to a commit.
<pre>
$ git checkout -b branchName someWhere
</pre>
Will create a new branch then checkout. SomeWhere is optionnal.

<br />


<a name="merge"></a>
## 7. merge

Merge to branch into one :
<pre>
$ git merge featureBranch
</pre>
Merge the specified branch into the current one.


<br />


<a name="rebase"></a>
## 8. rebase

Apply commits of current branch ahead of specified one :
<pre>
$ git rebase "destination" "source"
</pre>


<br />


<a name="revert"></a>
## 9. revert

Revert commits : if specified commit was a new line, the line will be remove.
<pre>
$ git revert anyCommit anOtherCommit
</pre>





