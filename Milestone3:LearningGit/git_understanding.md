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