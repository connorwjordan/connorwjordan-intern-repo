# Git Understanding

**What is the difference between staging and committing?**  
Staging adds files and changes to the commit so that you can stage files over time before committing all the files and changes to the branch. This commit shows up in the history of the repo with the commit message, what changes were made between commits, and when they were made.

**Why does Git separate these two steps?**  
When committing to a branch you want to have a clear history of the changes with relevant comments, if you stage every change you've made into a commit it can become bloated with changes that aren't relevant to each other. Only staging changes relevant to the current commit so that you can create this accurate history of changes is important for version control.

**When would you want to stage changes without committing?**  
You would want to stage changes that you've made to a file but before making changes to another file that is also relevant to the issue you are fixing so that once those changes are made, they can be staged and committed together.