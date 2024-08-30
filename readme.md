## Step 1: Create a local Git repo
### To connect a new project to a remote Git repository, you must create a Git repo locally, add files and perform at least one commit. The terminal window commands to do this are as follows:
 
 
```markdown
git init
git touch alpha.txt
git add alpha.txt
git commit -m "Git commit history created"
```

## Step 2: Add a reference to the remote repo
### To connect this new project to a repo on a remote hosting service such as GitHub, GitLab or Bitbucket, obtain the Git URL of the remote repository and issue the following command:

```
git remote add origin https://github.com/cameronmcnz/remote-repo-url.git
```
This adds a reference to the remote server in your local project.

## Step 3: Push your changes to the server
### After the remote reference is configured, you can transfer your local files to the server with the git push command.

```
git push -u origin master
```

### When you clone, all the remote references and upstream branches are preconfigured automatically. There's no need to run the git remote add origin command. The process will already add the remote.

```
git clone https://github.com/scrumtuous/repos-git-url.git
```


### The following commands assume your local branch is named master and the remote branch is named main. When performed, divergent Git commit histories are safely combined and a push to origin does not require force.

```
git remote add origin https://github.com/example/repo-git-url.git
git pull origin
git switch master
git rebase main
git push origin
git branch -d main
```
