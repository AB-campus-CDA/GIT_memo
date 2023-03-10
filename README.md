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
 * [13. config](#config)
 * [14. list](#list)


------------

<a name="init"></a>
## 1. init

Init the GIT repo localy. That's all.


<br />


<a name="status"></a>
## 2. status

Give the local repo state :
- Compare branch with remote(s)
- Staged files (ready to be commited)
- Files with changes that are not staged


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
Will create a new branch then checkout. SomeWhere is optional.

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


<br />


<a name="reset"></a>
## 10. reset

Will forget the last commit.


<br />


<a name="tag"></a>
## 11. tag

Add a tag to the current commit, or optionaly to a specified commit :
<pre>
$ git tag VERSION_1 5ceg36f
</pre>


<br />


<a name="log"></a>
## 12. log

Show history of commits. May be cool with options :
<pre>
$ git log --oneline --graph
</pre>
Will show one commits by line : sha1 + branch, tag, repo + message


<br />


<a name="config"></a>
## 13. config

Modify GIT config file, add --globale option to make changes to all projects :
<pre>
$ git config --global merge.ff false
</pre>
Will disable fast forward default option on merge command.


<br />

<a name="list"></a>
## 14. list

List a particular kind of file :
<pre>
$ git ls-files -m
</pre>
The -m option select modified files

<br />
<br />


## 15. conflits de merge

Un conflit se mat??rialise par une portion de code modifi?? diff??rement en local et en remote.
<br />
Le gestionnaire ne sait pas quelle version conserver : la distante ou la locale ??
<br />
Un IDE permet de r??soudre facilement le probl??me car il affiche en parall??le les portions ?? ??valuer. Au final la portion de code est soit une des 2 versions soit un mix.

<br />
<br />



De grands pouvoirs impliquent de grandes responsabilit??s.
