#Case 0: Setting up a project with Git
Create a folder on your machine where you would like your new project to exist. If you already have a project, navigate to it.

Create the new project.

Write in the terminal, at the root folder of this project:
```
git init
```
If you are using IntelliJ it looks like the following after initializing git.
(If using Mac)
<a href="http://imgur.com/WxUk3NI"><img src="http://i.imgur.com/WxUk3NI.png" title="source: imgur.com" /></a>

(If using Windows)
<a href="http://imgur.com/yhW0g3r"><img src="http://i.imgur.com/yhW0g3r.png" title="source: imgur.com" /></a>

##Creating a .gitignore file
Create a .gitignore file to avoid adding irrelevant files to your repository.
We only want to include source code files, so anything else should be excluded in the .gitignore file. You could also include other resources like readme.txt (text files), feature change list, language files or other relevant files. Do not include files which can be generated/compiled from other files, eg. java .class files or similar.

<table>
<tr>
<td>
To create the .gitignore file on a Mac
In the terminal write:
```
touch .gitignore
open .gitignore
```
</td>
<td>
To create the .gitignore file on Windows
In the command prompt write:
```
notepad .gitignore
```
</td>
</tr>
</table>


Insert the files and directories that you want to exclude. Each line in the file is one exclusion eg. a directory with all its files or a file. You can also use * as a wildcard.

In this example our .gitignore file looks like the following:
<table>
<tr>
<td>
(Mac)
<a href="http://imgur.com/Ytyd8zn"><img src="http://i.imgur.com/Ytyd8zn.png" title="source: imgur.com" /></a>
</td>
<td>
(Windows)
<a href="http://imgur.com/wdjLGYx"><img src="http://i.imgur.com/wdjLGYx.png" title="source: imgur.com" /></a>
</td>
</tr>
</table>

Next, we set up a remote repository. In this case we use bitbucket.org but you could also use github or other services.
Register as a user at bitbucket.org. All team members must create an account.
Create a repository with Git as a versioning control system.
At the time of writing, creating a repository, bitbucket looks like the following:
<a href="http://imgur.com/k2qei87"><img src="http://i.imgur.com/k2qei87.png" title="source: imgur.com" /></a>

After creating the remote repository we need to set up our local repository and point it to the remote repository.
To do that we write:
```
git remote add origin https://ChristianKirschberg@bitbucket.org/ChristianKirschberg/gittest.git
```
Replace the URL with your relevant URL. The URL can be found in your bitbucket account at the following location.
<a href="http://imgur.com/dYT8BGh"><img src="http://i.imgur.com/dYT8BGh.png" title="source: imgur.com" /></a>

If, for some reason, origin is already set and you get the error message =="fatal: remote origin already exists."==, you can delete the existing with:
```
git remote rm origin
```
Then, we would like to copy (push) our code from the local repository to the remote repository, so other developers can get (pull) the code.
To do that we, first, add all files except those defined in the .gitignore file by:
```
git add --all
```
Then, we  commit our new or changed files to the local repository:

```
git commit -m "Initial commit"
```

(notice the commit message here, in the quotes, where we write a message relevant to the changes to the code we have made).
Then, we push our local repository code to the remote repository.
```
git push origin master
```
After this the base project is in the remote repository and other developers can get (pull) the code which we will do in the next section.
