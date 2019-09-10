
1. Draw a diagram of the commits and branches in repository.

    - Use `git branch` to list the branches in this repository.
    - Use `git checkout` to explore each branch.
    - Use `git log --decorate` to explore the structure of commits.

``` 
     ->F2			
    / 
	F1-->F3
```		

2. Try `git log --graph --all` to see the commit tree. What do you see?
```
I see 3 commits. The initial commit to add a draft of A.py, “adding some more knowledge to the function” in the math branch, and then “a small change here” to the math branch


```

3. Use `git diff BRANCH_NAME` to view the differences from a branch and the current branch.
   Summarize the difference from master to the other branch.

```

The branch has added python code to print ‘That was easy bud’ if two numbers are summed, and ‘subtraction’ if we subtract the 2nd number from the 1st number. Otherwise, the calculation will print ‘My knowledge is limited’

```

4. Write a command sequence to merge the non-master branch into `master`

``` 
Pauls-MacBook-Pro:handson pauldeasy$ git checkout master
Pauls-MacBook-Pro:handson pauldeasy$ git merge math
Merge branch 'math'
“INF502 Assignnment#1 Q4”
# Please enter a commit message to explain why this merge is necessary,
# especially if it merges an updated upstream into a topic branch.
#
# Lines starting with '#' will be ignored, and an empty message aborts
# the commit.
Pauls-MacBook-Pro:handson pauldeasy$ git commit

```


5. Write a command (or sequence) to (i) create a new branch called `math` (from the `master`) 
and (ii) change to this branch

```
Pauls-MacBook-Pro:handson pauldeasy$ git branch math
Pauls-MacBook-Pro:handson pauldeasy$ git checkout math
```
   
6. Edit B.py adding the following source code below the content you have there
```
Pauls-MacBook-Pro:handson pauldeasy$ git
print 'I know math, look:'
print 2+2
```

7. Write a command (or sequence) to commit your changes
```
Pauls-MacBook-Pro:handson pauldeasy$ git commit -a -m "New B.py file"

```

8. Change back to the `master` branch and change B.py adding the following source code (commit your change to `master`):
```
print 'hello world!'
```

9. Write a command sequence to merge the `math` branch into `master` and describe what happened
``` 

Pauls-MacBook-Pro:handson pauldeasy$ git checkout master
Pauls-MacBook-Pro:handson pauldeasy$ git merge math
It states "fix conflicts and then commit the result

Because we changed the same code of the master twice, we cannot merge the branch into the master.

```
   
10. Write a set of commands to abort the merge
```
Pauls-MacBook-Pro:handson pauldeasy$ git merge --abort

```
   
11. Now repeat item 10, but proceed with the manual merge (Editing B.py). All implemented methods are needed. Explain your procedure
```


```

12. Write a command (or set of commands) to proceed with the merge and make `master` branch up-to-date
```


```

### Part 2: Using GitHub

The goal of this assignment is to put you in touch with the fork-pullrequest process, with an extra of dealing a little bit with Markdown. To learn more about Markdown [click here](https://guides.github.com/features/mastering-markdown/).

**You must fork this repo and submit a pull request back**

1. Into the students folder, create a file called LASTNAME_FIRSTNAME.md (please change LASTNAME_FIRSTNAME for your actual last and first names). 
2. Use Markdown to structure the following information about the last paper you've read (you can structure your markdown the way you want):
- Title
- Venue (journal name/conference)
- Number of pages
- 3 outcomes of the paper
- link to the paper online

3. Send your file back to this repository until creating a pull request (your pull request needs to appear [here](https://github.com/igorsteinmacher/CS502-Fall2019/pulls)).

4. Report your experience of making this submission, including the steps followed, commands used, and hurdles faced (within the file you created for the **Part 1**.
```


```






