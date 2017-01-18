#Case 5: Accidently committed files to your repository
At some point you will most likely end up in a situation where you have committed a file or directory to your online repository, which you did not intend to have committed.
If you use the command
```
git rm -r somedir
```
You will delete the online version of the directory file but also the local file as well.

If you want to delete only the shared online version of the file and keep your local copy you will have to use a different approach.

You should remove the file from being monitored by git
```
git rm --cache -r somedir
```
Now the folder is no longer being monitored by git, and it is just a normal folder in your local filesystem.

To prevent the file from being monitored again in the future and from being placed in the online repository you should then modify your .gitignore file so the unwanted file or folder is no longer being committed

Then add, commit and push.
```
git add --all
git commit -m "removed somedir from online repository"
git push
```
Now the folder should have been removed online.
