#svn-git-mirror
Simple script to mirror a subversion repository to a git repository

##Dependencies
svn-git-mirror depends on a few command line utilities:
* git
* git-svn
* subversion


##Installation
To install `svn-git-mirror`, simply copy the script to somewhere in your path

or

use the full path name when invoking the script
    
    
##Usage
First, a workbench needs to be initialized. This workbench then becomes the staging area where svn changes are fetched before
pushing them to git. From a command line, run:

   `svn-git-mirror init -s <subversion_repo_url> -g <git_repo_url> -d <workbench_directory>`
   
Next, whenever you would like to push changes to git, simple run:

   `svn-git-mirror update -d <workbech_directory>`
   
To see the full list of arguments supported, run

   `svn-git-mirror`
   
   
##Notes
* To schedule the 'update' to occur periodically, you can schedule the 'svn-git-mirror update' call via cron
* The script assumes a standard svn layout (with branches, trunks, tags). If you have a non-standard layout, supply the "-n" argument to the init command
* An authors file is supported by specifyinhg the "-a" argument. Note that all authors must be defined in this file or running update will fail



