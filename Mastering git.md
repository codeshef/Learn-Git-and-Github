<p><h1>Mastering git</h1></p>
<p>In this we deep look at the fundamental commands to the design of distributed workflow</p>
<p>We focus on how git is thinlking</p>
<p><h2>Four Areas : Introduction</h2></P>
<p><h3>Basic model of Git </h3></p>
<p> Git works in four areas:</p>
<ul>Working area where we keep our files and folders</ul>
<ul>Repository contains entire history after commit stuff goes here</ul>
<ul>Index area is intermediate between them before commit our files are present there</ul>
<ul>Stash is temporary storage area</ul>

<p> Now two questions arises</p>
<ul>How does this command move infromation across the Four areas?</ul>
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
<p>
</ul>
</ul>


