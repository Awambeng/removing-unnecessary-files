## Removing unnecessary files from a commit after pushing to GitHub.
If you are working on a project and pushed a file which wasn’t intended for that commit and you want to remove the file. You can follow these steps:

### Identify the commit which the file was added to:
```Run the command “git log --oneline”```
- This command will display all your commit history along with their hashes(unique identifiers), you then locate the commit where the file was added.
### Create a new branch:
- Create a new branch just before the one where the file was added. Let’s say the file in which you want to remove is “cache” and the commit hash is let’s say “57a2a40” you can use this in creating the new branch use the command 
```“git checkout -b fix/remove-cache 57a2a40”```
### Remove the file:
- Remove the cache file from your working directory using the command “git rm cache” 
### Commit changes:
- Commit the changes with a  message like
```git commit -S -m "Remove cache from the commit"```
### Push the commit your repository:
- Using the command “git push -u origin fix/remove-cache” you can push your new branch to your git repository.
### Create a pull request:
- Create a pull request on the repository, targeting the branch you had made the accidentally commit of the file. In the pull request description, explain that you removed the unintended file from the commit.
### Merge:
- Merge the changes into the first branch, this would effectively remove the file "cache" from the commit history.


