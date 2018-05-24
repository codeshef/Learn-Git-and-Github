
<h1> Learn-Git-and-Github</h1>
<h2> Basic Git concepts</h2>

<h3> A Brief history of version control</h3>
<ul><h4>First Generation</h4></ul>
<li>single-file</li>
<li>no networking</li>
<li>e.g. SCCS,RCS</li>

<h4>Second Generation</h4>
<li>Multiple files</li>
<li>centralized</li>
<li>e.g CVS,SVN</li>

<h4>Third Generation</h4>
<li>Changesets</li>
<li>Distributed</li>
<li>e.g Git,Hg,Bazaar,BitKeeper</li>

<h3>Advantages of DVCS</h3>
<li>Different Topologies.</li>
<li>Backups are easy.</li>
<li>Reliable branching and Merging.</li>
<li>Full local history.</li>
<li>New Ideas.(Deployment like git push heroku prod_branch)</li>

<h3>About Git</h3>
<li>Created by Linus Torvalds,who created Linux.</li>
<li>Prompted by Linux-Bitkeeper separation.</li>
<li>Started in 2005.</li>
<li>Written in Perl and C.</li>
<li>Runs on Linux,OS X,Windows,and many other operating systems.</li>
<li>Design goals:</li>
<li>Speed</li>
<li>Simplicity</li>
<li>Strong branch/merge support</li>
<li>Distributed</li>
<li>Scales well for large projects</li>


<h3>Installing Git</h3>
<ul>apt-get install git-core(Debian/ubuntu distros)</ul>
<ul>yum install git-core(Fedora distros)</ul>

<h3>Configuring Git</h3>
<ul>System-level configuration:</ul>
<ul>git config --system</ul>
<ul>Stored in /etc/gitconfig or c:\Program Files(x86)\Git\etc\gitconfig</ul>

<ul>User-level configuration:</ul>
<ul>git config --global</ul>

<ul>Repository-level configuration:</ul>
<ul>git config</ul>
<ul>Stored in .git/config in each repo</ul>

<h3>Working Locally with Git</h3>
<h4> Overview : </h4>

<ul><h4>Creating local repository</h4></ul>
<li>git init(Using this command turn your empty directory into local git repo.create .git which contain repo and its metadata)</li>
<li>git status</li>

<ul><h4>Adding Files</h4></ul>
<li>git add fileName(To add files)</li>
<li>git add -u(To update all the previously added files)</li>
<li>git add -A (add untracked files)</li>

<ul><h4>Commiting changes</h4></ul>
<li>git commit -m"Message" (commit files in staging area)</li>

<ul><h4>Viewing history</h4></ul>
<li>git log (To check history)</li>

<ul><h4>Viewing a diff</h4></ul>
<li>git diff</li>
<li> latest commit is known as head ,
Run git diff HEAD~1..HEAD to move to previous head.</li>

<ul><h4>Working copy,staging,repository</h4></ul>
<li>Careful about what you actually staging</li>

<ul><h4>Deleting files</h4></ul>
<li>rm filename (to remove file)</li>

<ul><h4>Undoing changes to the working directory</h4></ul>
<li>git checkout filename (to clean changes or to revert changes that you made by mistake,pull changes out of repo) </li>
<li>git reset --hard (Move to head again revert changes) </li>

<ul><h4>Undoing and Redoing</h4></ul>
<li>git reset --soft HEAD~1(Move back to staging area so that we can reorganize things)</li>
<li>git reset --hard HEAD~1 (Delete the present head , move to previous head and discard all changes)</li>

<ul><h4>Cleaning the working copy</h4></ul>
<li> git clean -n (tell what would be clean)</li>
<li> git clean -f (actually perform the cleaning operation)</li>

<ul><h4>Ignoring files with .gitignore</h4></ul>
<li>We don't want log files to be added to our repo so git provide .gitignore.</li>

<h3> Working Remotely with Git</h3>

<ul><h4> Cloning Remote repo into Local repo</h4></ul>
<li>git clone <repo link></li>
  
<ul><h4>Basic Repository statistics</h4></ul>
<li>To check no of commits use git log --oneline | wc -1</li>
<li> Alternate way to do same is to use git log --online --graph</li>
<li> Use git shortlog (Tell us which commit is made by which author)</li>
<li> git shortlog -sne where s -sort in decresing order of number of commits and e -to add user email</li>

<ul><h4> Viewing Commit</h4></ul>
<li> git show Head~1</li>
<li> git remote (Tell us where the source came from)</li>
<li>git remote -v (Show both the fetch and pull url for remote)</li>

<ul><h4>Git Protocols</h4></ul>
<li>Git use protocol http ,https(80),git protocol(9418),ssh(22),file</li>

<ul><h4>Viewing Branches and Tags</h4></ul>
<li>Display all the branches using git branch</li>
<li>To Display remote branches use git branch -r </li>
<li>git tag (To tag versions)</li>

<ul><h4>Fetching from remote</h4></ul>
<li>git remote add origin <link> (To add remote origin) and we can have more than one</li>
<li>git fetch pulls down changes from remote repo</li>
<li>If multiple remotes use git fetch origin</li>
<li>git merge origin/master to master changes from remote to local repo</li>

<ul><h4>Pulling from remote</h4></ul>
<li>git pull to pull changes from remote</li>
<li>In above case git does n't know which branch to merge with so we use git branch --set upstream master origin/master</li>
<li>Other option is to use git pull origin master</li>

<ul><h4>Pushing to remote</h4></ul>
<li>git push to push changes to remote</li>
<li>To remove origin use git remove rm origin</li>

<ul><h4>Creating and Verifying tags</h4></ul>
<li>git tag v1.0 to tag versions</li>
<li>git tag -a v1.0 with message to add message</li>
<li>git tag -s v1.0_signed (It automatically requires message)</li>
<li>git tag -v  v1.0 with message to verify tag</li>
<li>Not verify in case of usigned and verify in case of signed tag</li>

<ul><h4>Pushing Tags to remote</h4></ul>
<li>git push --tags to push tags</li>


















