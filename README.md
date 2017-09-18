# responsive
Testing steps to push local to remote repo after - git init the local repo
The content of this repo is a frame of a responsive page generated via initilizr.com
This is a test procedure of the steps to push a local repo to this remote repo.
Steps
1. Connect to github ssh - gitbash
  $ eval $(ssh-agent -s)      <start the ssh agent>
  $ ssh-add ~/.ssh/privateKey <add private key >
    requires the key passphrase
  $ ssh -T git@github.com     <Test SSH connection>
2. Create a new local repo via CLI
  $ cd new-project
  $ git init	    <create the .git repo>
  $ git add .	    <recursively add working files to local repo index>
  $ git commit -m "first commit"    <result: working dir clean>
3. Push the local repo to the remote repo
  Use this process for a local repo created in a project directory via $ git init 
  (and the $ git add & $ git commit operations have been accomplished)
4. On github.com youraccount - create the remote repo shell - "git@github.com:youraccount/new-project.git"
  $ git remote add origin git@github.com:youraccount/new-project.git
  $ git push -u origin master
The local working directory and repo are synced with the remote repo on github
