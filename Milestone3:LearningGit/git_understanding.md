# Git Understanding

**What is the difference between staging and committing?**  
Staging adds files and changes to the commit so that you can stage files over time before committing all the files and changes to the branch. This commit shows up in the history of the repo with the commit message, what changes were made between commits, and when they were made.

**Why does Git separate these two steps?**  
When committing to a branch you want to have a clear history of the changes with relevant comments, if you stage every change you've made into a commit it can become bloated with changes that aren't relevant to each other. Only staging changes relevant to the current commit so that you can create this accurate history of changes is important for version control.

**When would you want to stage changes without committing?**  
You would want to stage changes that you've made to a file but before making changes to another file that is also relevant to the issue you are fixing so that once those changes are made, they can be staged and committed together.

**Why is pushing directly to main problematic?**  
This is because the changes you have made have not been reviewed by anyone and making these direct changes to main could cause problems with the ongoing service that the repo provides.

**How do branches help with reviewing code?**  
Branches help by letting you see how the changes that you've made would fit into the main repo, and how many commits ahead and behind that branch is. Being able to test a branch to make sure that the code runs correctly is important before merging any branches into main.

**What happens if two people edit the same file on different branches?**  
Those two branches will not interact with each other until pull requests are submitted and then you can end up with merge conflicts that will needed to be resolved before that PR is able to be merged into main.

**What caused the conflict?**  
Changes were made to the same file that would interact with each other and needed to be resolved before the branch could be merged into main.

**How did you resolve it?**  
I accepted the changes that had been made in main and the changes that had been made in the branch were removed.

**What did you learn?**  
That using branches is important for review as if multiple people all made changes to main then whoever did the last change would always overwrite the other changes. I was also able to test the merge feature in the VScode client and the merge viewer to see how I can use this when I face real merge conflicts with my work.

**What does each command do?**  
```git checkout main -- <file>``` is used to restore or add a specific file from the main branch to your current working branch while not affecting other files or changes.
```git cherry-pick <commit>``` lets you merge in a specific commit from another branch without merging the entire branch.
```git log``` allows you to see a history of the commits, who authored them, when they were committed, and the commit messages.
```git blame <file>``` allows you to see the who made changes to a file line by line as well as commit information about those changes.

**When would you use it in a real project (hint: these are all really important in long running projects with multiple developers)?**  
```git checkout main -- <file>``` would be used if I made changes to a file that were unwanted or by accident that would let me restore it to the original from the main branch.
```git cherry-pick <commit>``` if a commit from another branch was releveant to the work I was doing on the current branch that would let me create a new commit in the current branch containing the same changes.
```git log``` if I wanted to see who was commiting to a branch if something unexpencted was changed.
```git blame <file>``` if I want to know who made changes to specific lines of code, in case something was wrong or unexpected, so that you can follow up with them why the changes were made.

**What surprised you while testing these commands?**  
```git cherry-pick``` make a copy of the commit so that can be unwanted as there are 2 commits that perform the same thing. You can also use ```git blame``` on this file to see the same information about the author the commit that it was last changed in each line.

**What does git bisect do?**  
git bisect is a command that assists in finding in which commit a change was made, usually a bug but can also just be a positive change as well, by setting a starting point as good (before the bug was introduced) and bad (after the bug was introduced) and picks a point in the middle to test if the bug was included in this commit and let you assign that commit as good or bad, this occurs until the commit including the change is found.

**When would you use it in a real-world debugging situation?**  
When you want to determine who introduced the bug so that you can determine the cause, be malicious or by accident, as well as you can see if the commit brought in any other similar bugs that have gone un-noticed. 

**How does it compare to manually reviewing commits?**  
If reviewing a large amount of commits it can be much quicker as you don't need to sort through them yourself especially if you have a script that can determine if a commit is good or bad, however when reviewing a short amount with good commit messages sometimes it can be just as fast to quickly go through the commits to find the error.

**What makes a good commit message?**  
A good commit message is clear and brief, and anyone who reads it should be able to easily understand what has been changed or introduced.

**How does a clear commit message help in team collaboration?**  
It helps other understand what has been commited when they are reviewing commits so that they can easily find a commit they are looking for without having to open every commit to check if its the one they wanted to see.

**How can poor commit messages cause issues later?**  
Vague commit messages can cause misunderstanding on what has been changed in a commit so that on review they might not be able to find a commit due to not using keywords to do with the fix/change, they might also overlook a commit they think is insignificant if a commit message is poorly labled as a formatting fix that included logic changes that introduces a bug. 