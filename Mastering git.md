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




