
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
Run git diff HEAD~1..HEAD</li>

<ul><h4>Working copy,staging,repository</h4></ul>
<li>Careful about what you actually staging</li>

<ul><h4>Deleting files</h4></ul>
<li>rm filename (to remove file)</li>

<ul><h4>Undoing changes to the working directory</h4></ul>
<li>git checkout filename (to clean changes or to revert changes that you made by mistake,pull changes out of repo) </li>
<li>git reset --hard (Move to head again revert changes) </li>

<ul><h4>Undoing and Redoing</h4></ul>
<li>git reset --soft HEAD~1(Move back to staging area so that we can reorganize things)</li>
<li>git reset --soft HEAD~1 (Delete the present head , move to previous head and discard all changes)</li>

<ul><h4>Cleaning the working copy</h4></ul>
<li> git clean -n (tell what would be clean)</li>
<li> git clean -f (actually perform the cleaning operation)</li>

<ul><h4>Ignoring files with .gitignore</h4></ul>
<li>We don't want log files to be added to our repo so git provide .gitignore.</li>













