<p><h1>Mastering git</h1></p>
<p>In this we deep look at the fundamental commands to the design of distributed workflow</p>
<p>We focus on how git is thinking</p>
<p><h2>Four Areas : Introduction</h2></P>
<p><h3>Basic model of Git </h3></p>
<p> Git works in four areas:</p>
<ul>Working area where we keep our files and folders</ul>
<ul>Repository contains entire history after commit stuff goes here</ul>
<ul>Index area is intermediate between them before commit our files are present there</ul>
<ul>Stash is temporary storage area</ul>

<p> Now two questions arises</p>
<ul>How does this command move information across the Four areas?</ul>
<ul>How does this command change the repository?</ul>

<p><h3> Now go deep into areas:</h3></p>
<ul>Working area :where our files and directories are present in our system. </ul>
<ul>Repository : Repository is in .git folder
<ul><h4>Git Objects: </h4>
<li>Blob</li>
<li>Tree : Represent folders</li>
<li>Commit</li>
<p> All of these objects are immutable they can be created ,deleted but never change</p>
<p>They link with each other that define history</p>
<p> Each commit is linked with blobs and trees . They can share common objects also.</p>
<p>Each commit pointing to parent commit.Each commit is a snapshot.There is slice referencing to commit called branches.Branches are basically enter point to history.There is special point called head there is only one head.
 Head points to current commit.Move head by checkout.</p>
 </ul>
</ul>
<ul>Index: 
  <li>Index is also called staging area.</li>
  <li>git diff comparing working area with index</li>
  <li>git diff --cached  comparing index with repository</li>
</ul>
<p><h2>Basic Overflow</h2></p>
<p>Moving data to the right : git add transfer file from working area to index area.git commit 
move data from index to repository area.git commit change the repo.</p>

<p>Moving data to left : use git checkout by moving current head and it also copy repo data in working and 
 index area.</p>
<p>Removing files in Git :Untracked means file is in working area but not in index area. 
use git rm --cached filename  to delete file from index but not from working area ie. unstaged
the file</p>
<p> Renaming/Moving  Files : mv source destination to move or to rename file. </p>

<p><h2>Resetting</h2></p>
<p>Commands that move branches : 
 <li>Commit</li>
 <li>Merge</li>
 <li>Rebase</li>
 <li>Pull</li>
 In case of new commit head points to current branch and branch moves to current commit.
</p>

<p>Now in case of reset --hard copy data from current commit to both working area and index.
 --mixed option copies data from current head to index.
 --soft does not touch any area just change the branch.
 <b> <i>Reset moves the current branch,and optionally copies data from  the repo to other 
  areas.
  </i>
 </b>
</p>
<p><h2>More Tools</h2></p>
<ul>git stash --include--untracked  to store data in stash.</ul>
<ul>git stash list to list content of stash.</ul>
<ul>git stash apply to add stash data to working area and index.</ul>

<p><h2> Solving Conflicts</h2></p>
<ul>Merge Conflict</ul>

<p><h2>History : Exploring the Past</h2>
<ul>git log --graph --decorate --online</ul>
<ul>git show commit_id to show commit</ul>
<ul>Other way of moving head reference git show HEAD@{'1 month ago'}</ul>
</p>
<p> <h3>Browsing the log </h3></p>
<ul>git log --patch to show the changes in the commit.</ul>
<ul>git log --grep apples --online to show all the commits that contain apples.</ul>
<ul>git log -3 --online to show last n commits.</ul>
 
 <p><h3>Changing History</h3></p>
 <ul>Never rebase shared commits.</ul>
 <ul>git commit --amend  when we want to add our commit to old commit and don't want to add new
commit we use amend to append our new changes in that commit.Here our goal is to get clean
history. Its internal working is that git copies content of old commit in new commit .Now head 
points to that commit and old commit is garbage collected.</ul>

<p><h3>Interactive rebases</h3></p> 
<ul>git blame fileName to see when the lines added to git.</ul>
<ul>git rebase -i origin/master to rebase history or to change history with interactive rebasing.</ul>

<p><h3>Reflog</h3></p>
<ul>To change commits.</ul>
<ul>git revert commit_Id to revert chandes in git</ul>





