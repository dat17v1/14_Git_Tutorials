#Case 2: Handling merge conflicts
**The following are notes and should be explained like the above cases.**
Continuing from the previous case, with no merge conflicts, you can also experience that you get a merge conflict when programmer no. 2, Claus, tries to push his changes.
We will see an example of that in the following:

When 2 or more developers work on the same classes, merge conflicts can happen. Here we see this scenario and how to handle it.
Eg. we have the class defined as
```
public class Car {
   private String brand;
   private double mph;
}
```
Programmer1 adds a set method.

Programmer2 adds a constructor, like:
```
public class Car {
   private String brand;
   private double mph;
   public Car(String brand, double mph) {
       this.brand = brand;
       this.mph = mph;
   }
}
```

Now, programmer1 commits and pushes the changes and that goes well.

Programmer2 commits and pushes the changes and cannot before the new changes are pulled.

Programmer2 makes a pull and gets a merge conflict because Git cannot automatically merge the changes. Programmer 2 must now edit the conflicted files, add, commit and push them. Programmer 2 decides what to keep and what to delete (if anything).

It is a good idea to push your changes often to avoid handling merge conflicts. It is always the last programmer to push their changes who must handle the merge conflicts (just before he or she is supposed to leave the office for the day, but oh no, merge conflicts to handle…)
