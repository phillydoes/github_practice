# github_practice
Tutorial and Practice on using GitHub effeciently
For more detail:https://github.com/joshnh/Git-Commands

Common Commands:


    -> git pull	 

    -> git clone ssh://git@github.com/[username]/[repository-name].git
    or
    -> git init
    
    -> git status
    -> git add [file-name.txt]
    -> git rm -r [file-name.txt]
    
    -> git commit -m "[commit message]"
    -> git push
    
    -> git branch [branch name]
    -> git merge [source branch] [target branch]
    
----------------------------------------------------------------------------------- 
1. Starting off

  If a repository is already created, create a local copy of the repo by typing in the command line;
  -> git clone ssh://git@github.com/[username]/[repository-name].git
    Example: Clone this repo "github_practice.git" using;  
  -> git clone ssh://git@github.com/phildo59/github_practice.git
  
  Else create a new local repo at the current file address using;
  -> git init
  
----------------------------------------------------------------------------------- 
2. Status

  After adding or creating a repo then accessing repo;
    1. Check status to see if cloning was successful using;
      -> git status
     Example: 
     -> pdo@ada1:~/[repository-name].git git status
        On branch master
        Your branch is up-to-date with 'origin/master'.
        nothing to commit, working directory clean
        
 -----------------------------------------------------------------------------------  
3. Files
  After confirming repo status, add files using;
    -> git add [file-name.txt] //add a specific file to staging area 
    -> git add -A              //Add all new and changed files to staging area
  
  Remove a file using;
    -> git rm -r [file-name.txt] //Remove a file or folders
    
-----------------------------------------------------------------------------------   
4. Commit

  After updates are ready to saved, create a record of all files have been modified using;
  Note: Adding a concise commit message is good manners to others working on the same repo. 
    -> git commit -m "[commit message]"
    
  Commit messages should contain;
    1.All changes made
    2. End Goal and Daily Goal
    3. Problems
    4. Information to help understand changes
    
-----------------------------------------------------------------------------------   
5. Branching & Merging

    Create a branch from the master branch
    when developing new changes that may result in a unstable master branch.
    
      List:
        -> git branch                                           //list branches. (*) denotes current branch
        -> git branch -a                                        //list all branches(local and remote)
      
      Create:
        -> git branch [branch name]                             //creates a new branch with [branch-name]
        -> git checkout -b [branch name]                        //creates and switch to new branch
        -> git checkout -b [branch name] origin/[branch name]	  //Clone a remote branch and switch to it
      
      Remove:
        -> git branch -d [branch name]                          //Delete branch [branch name]
        -> git push origin --delete [branchName]	              //Delete a remote branch
        -> git checkout -- [file-name.txt]                      //Discard changes to a file
      
      Access:
        -> git checkout [branch name]                           //switch to branch [branch name]
        -> git checkout -                                       //switch to branch last checked out

      Merge:
        If branch is stable and ready to be added to master branch, use;
        -> git merge [branch name]                              //Merge a branch into the active branch
        -> git merge [source branch] [target branch]	          //Merge a branch into a target branch

      Stash:
        "Stashing takes the dirty state of your working directory
           — that is, your modified tracked files and staged changes —
           and saves it on a stack of unfinished changes that you can 
           reapply at any time."
         Source:https://git-scm.com/book/en/v1/Git-Tools-Stashing
         
         -> git stash                                           //stash changes in a dirty working directory
         -> git stash clear                                     //Remove all stashed entries
-----------------------------------------------------------------------------------
6. Sharing & Updating Projects

      Push: Apply changes to remote repository
        -> git push                                             //Push changes to remote repository (remembered branch)
        -> git push origin [branch name]	                      //Push a branch to your remote repository
        -> git push -u origin [branch name]	                    //Push changes to remote repository (and remember the branch)
        
        -> git push origin --delete [branch name]	              //Delete a remote branch
        
      Pull: Update local repo with remote repo
        -> git pull	                                            //Update local repository to the newest commit
        -> git pull origin [branch name]	                      //Pull changes from remote repository 
    
    
      Remote:
        -> git remoteadd origin 
        ssh://git@github.com/[username]/[repository-name].git   //Add a remote repo
        
        -> git remote set-url origin 
        ssh://git@github.com/[username]/[repository-name].git	  //Set a repository's origin branch to SSH
        
-----------------------------------------------------------------------------------
7. Inspection & Comparison

      -> git log                                                //View changes
      -> git log --summary                                      //View detailed changes
      -> git diff [source branch] [target branch]	              //Preview changes before merging
      
-----------------------------------------------------------------------------------
Summary:
  When working with a co-workers on a project, GitHub is popularly used to easily develop within a group.
  Knowing how to effectively use GitHub and their commands can help production and development.

      
     
