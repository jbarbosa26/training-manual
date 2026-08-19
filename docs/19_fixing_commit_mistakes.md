## Fixing commit mistakes

In this activity, we will begin to explore some ways Git and GitHub can help us shape our project history.

### Revising your last commit

`git commit --amend` allows us to make changes to the commit that HEAD is currently pointing to. Two of the most common uses are:

- Re-writing commit messages
- Adding files to the commit

Let's see this in action:

1. Create a new file:
   - Bash: `touch file7.md`
   - CMD: `echo > file7.md`
   - PowerShell: `Out-File file7.md`
1. When you are adding files to the previous commit, they should be in the staging area. Move your file to the staging area: `git add file7.md`
1. `git commit --amend`
1. The text editor will open, allowing you to edit your commit message.

>You can actually amend any data stored by the last commit such as commit author, email, etc.

### Oops, I forgot to create a branch

If you begin working, but you are still on `main`, don’t panic! Changes aren't “on” a branch until they are committed. Your working directory and staging area are attached to `HEAD`, _not_ a branch. So, you can change branches, and any changes that are not committed will come with you.