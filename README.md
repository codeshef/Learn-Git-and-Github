
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













