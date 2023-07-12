<h1>Getting Started with Git</h1>
<h2>Introduction</h2>
<p>As you now know, Git is a version control system. The Learn platform at Flatiron school has a deep integration with Git and GitHub. GitHub is an online hosting platform that uses Git. We need to teach you just enough Git to interact with GitHub like a real developer. While you can run Python notebooks on the Learn platform itself, you'll also want to be able to download material to your local computer so you can work on it there.</p>
<h2>Objectives</h2>
<p>You will be able to:</p>
<ul>
<li>Describe the difference between a forked and a cloned respository</li>
<li>Use <code>git clone</code> to clone a repository</li>
<li>Use <code>git add</code>, <code>git commit</code>, and <code>git push</code> to make changes to a repository</li>
<li>Compare local and remote repositories</li>
</ul>
<h2>Some terminology and concepts</h2>
<p>As you can see from the objectives above, we're going to dive in and use several Git commands in this lesson. </p>
<p>The first thing we'll look at is <em>forking</em>, a concept from the GitHub platform.</p>
<p>Forking is the process of making a personal copy of the Learn lab on GitHub. It's basically how you tell Learn that you have started working on a lab.</p>
<p><img alt="What's a Fork" src="http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/git-workflow-1.png"/></p>
<p>Afterward, we'll then use <code>git clone</code> from a bash shell like terminal or git bash in order to copy the material from the web to our local computer.</p>
<p>From there, Git will allow us to continue to track and incorporate changes that we make to our work. </p>
<p><code>git status</code> allows us to see if we have made any changes.</p>
<p>If we have made changes that we would like to save to our version control history, we can then use <code>git add</code> to add the changed files to the version history and <code>git commit</code> to finalize the process. Finally, we can then use <code>git push</code> to push our changes to the web so that we or collaborators can access them from anywhere. </p>
<p>Now that you have a brief overview of what we're about to dive into, let's go through the process step by step.</p>
<h2>Open up a Bash Shell and Create a Course Folder / Subfolder</h2>
<p>To use Git, we're going back to the bash shell (mac: terminal, windows: git bash) once again!
To start:</p>
<ul>
<li>Create a folder on your computer for your course materials and navigate into it (preferably using <code>mkdir</code> and <code>cd</code>) </li>
<li>Then create a subfolder titled "Section1", "Bash_and_Git" (or whatever you find to be an appropriate title) and navigate into that </li>
<li>Return to your web browser and navigate to the lesson you want to download </li>
<li>Click the GitHub icon</li>
</ul>
<p><img src="https://curriculum-content.s3.amazonaws.com/data-science/images/learn_github_logo.png"/></p>
<p>You'll be redirected to the associated github repository like this.<br/>
<img src="https://curriculum-content.s3.amazonaws.com/data-science/images/github_fork_button.png"/></p>
<ul>
<li><strong>Click the fork button</strong>, as shown above in order to create a copy to your personal account which you can edit and update.</li>
</ul>
<p>After a moment of this:</p>
<p><img src="https://curriculum-content.s3.amazonaws.com/data-science/images/github_forking_in_progress.png"/></p>
<p>You'll be redirected to your new personal copy of the repository:</p>
<p><img src="https://curriculum-content.s3.amazonaws.com/data-science/images/forked_github_page.png"/></p>
<h2><code>git clone</code></h2>
<p>Now that you have your own copy (by forking), we're going to download this copy to your local computer using <code>git clone</code>.</p>
<ul>
<li>
<p>Copy the URL </p>
<ul>
<li>Mac: Press <strong>cmd+L</strong> to highlight the url bar and <strong>cmd+c</strong> to copy the url</li>
<li>Windows: Press <strong>Ctrl+L</strong> to highlight the url bar and <strong>Ctrl+c</strong> to copy the url</li>
</ul>
</li>
<li>
<p>Return to your bash shell</p>
</li>
<li>
<p>Type: <strong>git clone</strong> and paste your repo url (<strong>cmd + v</strong> or <strong>Ctrl+V</strong>)</p>
</li>
</ul>
<p><strong> Voila!  </strong></p>
<p>The repository and all of its contents will be downloaded locally to your computer!</p>
<p>You should be able to see the new folder by listing the files in the current directory with <code>ls</code>.<br/>
You can then navigate into the git directory with <code>cd directory_name</code>.</p>
<p>Now that you have a local copy, we can further investigate some more Git commands for version control. <strong>Note that for these to work you must be in the git folder (the one you just cloned above). Make sure to navigate into the folder using the <code>cd</code> command.</strong></p>
<h2><code>git status</code></h2>
<p>Once you have a Git repository downloaded locally, Git will keep track of every change you make to the code in that folder. You can ask Git what the differences or changes you've made since the last commit by typing <code>git status</code> into your terminal.</p>
<p>It's really helpful to constantly get the status from Git to see what changes you need to stage, add, commit, or push.</p>
<h2><code>git add</code></h2>
<p>Adding changes with the <code>git add</code> command is a way to stage any changes and get them ready to be a permanent record in your Git log via a commit. The workflow worth memorizing right now is to simply add all your changes via <code>git add .</code>.</p>
<h2><code>git commit</code></h2>
<p>A commit is a permanent moment in time in your Git history. A commit creates a new version of your code. To commit, memorize this command. <code>git commit -am "Your commit message"</code>. You are using the <code>git commit</code> command with the flags <code>-am</code>, which tell Git to commit all the changes and to include a commit message. You supply the commit message in <code>""</code> directly in the command, <code>"Your commit message"</code>.</p>
<h2><code>git push</code></h2>
<p>Pushing is the process of taking your local code and commits and syncing them, or uploading them, to GitHub. You're updating the GitHub remote (remotes are just fancy names for copies of the repository), generally your fork, represented by a remote named <code>origin</code>, by pushing your code to the remote. The Git command to do this is simply <code>git push</code>. When you <code>git push</code> from within a Git repository, it will take all the commits that you have locally and push them to the online remote.</p>
<h2>Additional Resources</h2>
<ul>
<li>
<p><a href="https://www.git-tower.com/blog/git-cheat-sheet/">Git Cheatsheet</a> </p>
</li>
<li>
<p><a href="https://www.git-tower.com/learn/git/ebook/en/command-line/appendix/best-practices">Git Best Practices</a> </p>
</li>
<li>
<p><a href="https://guides.github.com/introduction/flow">Understanding the GitHub Flow</a> </p>
</li>
<li>
<p><a href="https://guides.github.com/activities/hello-world">Hello World GitHub</a> </p>
</li>
<li>
<p><a href="https://guides.github.com/activities/forking">Forking on GitHub</a> </p>
</li>
<li>
<p><a href="http://rogerdudler.github.io/git-guide/">Git - The Simple Guide</a> </p>
</li>
<li>
<p><a href="http://gitimmersion.com/">Git Immersion</a> </p>
</li>
<li>
<p><a href="http://try.github.com/">Try Git</a> </p>
</li>
</ul>
<p data-visibility="hidden">View <a href="https://learn.co/lessons/enough-git-for-learn-co" title="Enough Git for Learn">Enough Git for Learn</a> on Learn.co and start learning to code for free</p>
<h2>Summary</h2>
<p>In this lesson, we took an introductory look at Git and GitHub. First, we saw how to fork and clone repositories from Learn onto your local machine. From there, we then further discussed how to add changes to git, commit them, and push them online.</p>