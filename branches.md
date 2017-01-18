#Case 3: Using Branches

**The following are notes and should be explained like the above cases.**
Features should be developed in branches and then merged into the main-development branch when the feature is finished. That way multiple programmers working on the feature can share the code without pushing their (not finished) code into other programmers’ (who are working on something else) code base.

Create a branch:
Programmer 1:
```
git checkout -b smart-feature
```
“make changes”
```
git add --all
git commit "some message that describes what you did"
git push origin smart-feature
```
Programmer 2:
```
git fetch -p
git branch -a
git checkout -b smart-feature
git pull origin smart-feature
```
(make changes, work work work, add, commit, push).

Extra: (git push --set-upstream origin smart-feature): Sets default when writing git pull or git push.

Merge af master and smart-feature:
```
git checkout master
git merge smart-feature
```
Delete a feature branch that you do not use anymore:
```
git branch -d smart-feature
```
To delete a remote repo.
```
git push origin --delete smart-feature
```
To update the local database of remote branches
```
git fetch -p
```
