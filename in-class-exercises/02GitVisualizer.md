## Git Visualizer Instructions ##

- [Git visualizer](https://git-school.github.io/visualizing-git/)

> In the dropdown in the top left select "Free Explore with Remote"

You are a software developer for a game developer. The game you are working on has a new feature that needs to be implemented. It is an online game and we are adding vehicles that players can drive. It's going to require you to create a Vehicle class. You'll need to create a new branch for this feature.

```
git checkout -b feature-Vehicles
```

Then you'll need to create the `Vehicle` class and commit it to your local HEAD.

```
git commit -m "create Vehicle class"
```

After creating this class you'll need to reference it in other places in the app and commit those code changes.

```
git commit -m "use new vehicle class"
```

You are realize you haven't pushed your changes. Better do that so you don't lose them. You are off for the day and head home.
```
git push
```

While you were home that night an urgent fix happened on another branch by one of your coworkers. The bug was causing the came to crash.

(Pretend you are your coworker)
```
git checkout master
git checkout -b hotfix-fix-crashing-bug
git commit -m "fixed crash"
```

The bugfix code was completed then merged into the master.

```
git checkout master
git merge hotfix-fix-crashing-bug
```


The next morning you decide it's time to merge your code into master. The first thing you need to do is pull to see if there were any changes.
```
git pull
```
NOTE: You will see 'Fetched 0 commits'. In the real world if you weren't the one to make the bug fix changes on master you would not have those commits in your local repository. They would then come down and you would see that there were changes. You would then see if this code was needed for your current feature.

Because your code is behind the master you will need to merge that code into your feature branch before you can merge it into master.

```
git checkout feature-Vehicles
git merge master
```

Now that the fix code has been merged into `feature-Vehicle` you have noticed some strange behavior with the `Vehicle` class. You fix it and need to commit the changes.

```
git commit -m "Vehicle class fixes"
```

Now that the code is working you can merge it into the master branch.

```
git checkout master
git merge feature-Vehicles
```

Push your changes to origin.
```
git push
```

NOTE: Normally you would submit a pull request when you were done with your feature and that is when you handle the merging of master. If there are any conflicts you would handle them on your local repo and then commit them to origin then the pull request could be merged into master in the remote repository.
