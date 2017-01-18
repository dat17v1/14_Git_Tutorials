#Case 4: Going back to a previous commit
**The following are notes and should be explained like the above cases.**
...in case you made some changes that you do not want to keep.

Programmer 1 makes some changes, but regrets the changes and just want to go back to the latest code base before the changes.
```
git reset --hard
```
(this will delete your work since last commit. **Beware, there is no way to get your code back after this!**)

An alternative to this is that you would like to go back to the last commit, but with the possibility of going back to the code you are working on. (A bit like “undo” and “redo”).

In that case you must “stash” your changes, go back by resetting, and then redo by using pop.

First stash:
```
git stash
```
Then go back by using reset
```
git reset --hard
```
Redo by using pop to go back to your stashed changes.
```
git stash pop
```
After this, your stash is removed, so if you want to do it again, you must create a new stash, reset and pop.
