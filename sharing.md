#Case 1: Sharing code via remote repository

Once the repository is setup on multiple developers machines, we would like to share our code extensions. It is important to push (deliver) and pull (receive) code regularly.
There are two scenarios when you want to share your code. Either you get merge conflicts or you get no conflicts. Here we will demonstrate sharing code with no merge conflicts.

Developer 1, in this example called David, adds the following class to the project.
```
public class Car {
   private String brand;
   private String model;
   private double engineSize;
}
```
Next we would like to share our changes with the other developers, so we first add, commit and push our changes.
Add:
```
git add --all
```
The git add --all adds all the new files or changes files to the list of files scheduled to be committed. It does not actually add the changes to the repository but only updates the list of filenames which contains changes or is new.

Commit:
```
git commit -m "Added Car class"
```

the git commit command updates the repository with the changes.

Push:
```
git push origin master
```
Pushes the changes to the shared repository.

Now developer two, in this example Claus, develops the following code:
```
public class Person {
   private String name;
   private double height;
}
```
Claus would like to, also, share this code, so he does the same, add, commit and push.
```
git add --all
git commit -m "Added Person class"
git push origin master
```
Notice the output in the terminal after issuing this command.

The push is rejected for Claus because David pushed some changes to the remote repository before Claus pushed his. To solve this Claus must first make a pull to get Davids changes into his repository.

Pull:
```
git pull origin master
```
This is the stage where merge conflicts can occur. In this case there are no merge conflicts.

After pulling the changes Claus can now push his changes to the remote repository. There are no merge conflicts (when Claus pulls Davids changes) because they worked with different classes.
```
git push origin master
```
Now Claus can work with the code shared by David and David can pull Claus changes by issuing a pull command.

In the next example we will see how merge conflicts can occur.
