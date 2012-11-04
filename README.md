gitly-diffs
===========

tiny repos to play and explain some git basics

### diff

Rule of thumb - the diffs are shown assuming the right-nand side (RHS) as base - i.e. 

`- A` - this line is present in the RHS, but has been deleted in the LHS
`+ A` - this line is missing in the RHS, it has been added in the LHS

to reverse the sides in the diff output, use the `-R` option

---
`git diff` - diff between working directory (WD) and index
`git diff --staged` - diff between the index and the HEAD
`git diff HEAD` - diff between WD and HEAD (in other words, all changes since the last commit, staged or not) 

`git diff <branch-name>` - ?? (comparing with the tip of another branch TODO - what use is it - I though Im diffing the WD and index - the branch doesnt count)

`git diff HEAD -- ./A.txt` - diff only the A.txt file (is the HEAD necessary?) 

`git diff HEAD^ HEAD` - compare the last commit with the one before it

`git diff <branch1> <branch2>` - compared the two branch tips
`git diff <branch1>..<branch2>` - does the same

`git diff <commit1> <commit2>` - compared the two branch tips
`git diff <commit1>..<commit2>` - does the same

Note: the `..` syntax does not denote a range.

---
git is not able to perform a diff between a local and a remote branch per se - you will need to **fetch** the remote one first.

the rest is the same as with local branches:

`git diff HEAD origin/master`





