# Git Learning #

* Git is the most popular version control system in the world.

# Version control system #

* A version control system recoeds the changes made to our code over time in a special database called <b> repository </b>.

## Repository ##

  * Repository means a place or something to store data ( Git usualy stores the code data )

## Advantages ##  

  * We can see the project history that who changes them and when.

  * We can also relative the previous data.

## Categories ##    

   * Centralized.

   * Distributed.

## Centralized ##   

  * In centralized systems, all team members must connect to the server to get the latest copy of the code.

  * Need to share the code with others.

  * EXAMPLE: subversion and team Foundation Server.  

## Disadvantages ## 

  * If server goes offline , no one can access.

## Distributed system ##   

  * we will have copy of project code , history in local system.So even the file gos offline , we can synchronise the code between us.

  * EXAMPLE : Git and Mecurial.

# Git #

* It is free source.
* Open source,
* Super fast.
* Scalable.
* CheapBranching/ Merging.

## Using Git ( Git environment to use ) ##

 * Command line --> It is always available and fast.
 * Code Editors , IDE --> Ex: VS code.
 * Grafical User Interface (GUI tools).
 * Source Tree.

## Installing git ( Terminal ) ##

   * mac OS --> Press command + space and type terminal.
   * Windows OS --> Click the search icon and type cmd.
   * Ubuntu OS --> click Contril + ALT + t.

## Git commands ##   

  git --version     -->  To see the version of git.

### NOTE : To install or update git version visit : git-scm.com ###

## Configuration settings in git ##

* We should specify the following data while configuring git.
  * Name .
  * E-mail.
  * Default editor.
  * Line Ending.

## Levels of configuration setting ##
 * System Level --> For all users.
 * Global Level --> All repositories of the current user.
 * Local Level --> The current repository.

## git configuration commands ##

 * git config --global user.name "User name " --> To set user name.
 * git config --global user.email "email" --> To set email id .
 * git config --global code.editor "code --wait" --> To set default editor.
 * git confug --global -e --> To edit above details.
 * git config --global core.autocrlf input --> Use this command for linux / mac.
 * git config --global core.autocrlf true --> Use this command for windows. 

## Importance of end line ##

* Windows uses end of lines as /c or /n as next lines.

* Ubunu uses only /n as next line.

## git help ##

 * git config --help --> to get help from git .
 * git config -h --> Shortcut to get help.

# Basic git workflow #

* Step 1 : Create directory.
* step 2 : Initialize git (empty) by git init command .
           A sub file is ceated within the fle . We cannot see that , we can only see using ls -a command.
           .git file will be present in the same file which contains copy of the current project files.
           NOTE : rm -rf .git --> to remove sub git repository  (DON'T do this)
* Step 3 : Finish work .
* Step 4 : After completion , we nedd to stage our changes using git add . command.
           Staging area is an intermediate state allows us to review our work before record it using commit the changes . We can also unstage them and add to another commit .
* Step 5 : After staging , Use git command -m "meaningful message" commanded to commit the changes.
           commit is like taking snapshots of our work that means recording the work and maintain history.

## Important things to know about basic flow og git ##

* Must use valid commit message to maintain good history of work . It is used to get easy identification of particular portion of the code.

* Our staging area will remain the last version of our code with last commit. It will not delete the old version once it committed.

* Each commit consists Unique id, message ,Date/time ,Author and complete snapshot of our code.

* The unique id is generated by git unique for each commit.

* The snapshot takes complete project everytime , not updating the old.

* Each commit compresses the content and it doesn't store duplicate content.So , no data storage is wasted.

## Staging files ##

* git status --> It is used to see the status ofthe working directory on the staging area.

## Methos of staging ##

* git add <filename> --> for single file.
* git add <filename> <filename> --> for multiple files.
* git add . --> for all file ( Be careful while using ) .
* git add *.txt --> files that contains .txt extensions.

## Commiting changes ##

* git commit -m "message" --> messages should be meaningful.
* To give a detailed commmit message for good understanding.
   Use / Type --> git commit and press enter
   Type your short and detailed descreption in the opened file and close yhe file to stop the process.

## Best practice of commiting ##
* As you reach a state you want to record Then , make a commit.
* Each commit should represent a logically seperate change set.
* Always use past tence in commit message.

## Skipping the staging area ##

* Mostly DO NOT use this method.
* If we are sure on our code (Whenever our code is not require review , skip yhe staging area )
* Use git commit -am "without staging"
   Here a is fr all and m is for message.

## Removing files ##   

* Commands to remove files from our local and the repository as well are below:

 * git rm -r filename.
 * git rm -r -f filname --> to force remove the file.
 * git rm -r --cached filename --> not to remove.

## Renaming our moving files ##

* i mv filename1 filename2 --> here moving and rename happens simultaneously.

## Ignoring files ##

* Special file --> .giignore --> attach this file in te file where we don't need stageing.

## Short status ##
* git status -s --> this will show the short type of work status .

## Viewing staged and unstageed files ##

* git diff --staged --> This will display a detailed comparison of old and current versions of last commited files to git.

## DIFF Tools ##
* There are lot of differnet tools first configure the setting to make vs code as default DIFF TOOL.

* git config --global diff.tool vscode
* git config --global difftool.vscode amd "cde --wait"

## Viewing the history ##

* git log --> It will show the history of all commits made with the unique id, author, date and time.
* git log --oneline  --> It will display the shortest things in history.
* git log --oneline --reverse --> It will show the history in reverse order.

## Viewing the commit ##

* git show HEAD -->It is also display the last commit details with detailed descreption.
* git ls-tree HEAD~1  

## Git objects ##

 * commits.
 * BLobs(Files).
 * Trees (Directions).
 * Tags.

 ## Unstaging files ##

 * git restore --staged filename 


## Discarding local changes ##

* git restore .
* git clean -f

## Restoring a file to an earlier version ##

* git restore --source=HEAD~1 filename




















