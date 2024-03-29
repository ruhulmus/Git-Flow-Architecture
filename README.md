# Git Work Flow Architecture

<p align="center">
<img src="https://github.com/ruhulmus/Git-Flow-Architecture/blob/main/Git-FLow.png" alt="Git-Flow-Architecture"/>
<p/>

<h4 align="center">Managing Branch using Git Work Flow Architecture </h4>

<p align="center">
<a href="https://github.com/ruhulmus/Git-Flow-Architecture/blob/main/LICENSE" target="blank">
<img src="https://img.shields.io/github/license/ruhulmus/Git-Flow-Architecture?style=flat-square" alt="Git-Flow-Architecture licence" />
</a>
<a href="https://github.com/ruhulmus/Git-Flow-Architecture/fork" target="blank">
<img src="https://img.shields.io/github/forks/ruhulmus/Git-Flow-Architecture?style=flat-square" alt="Git-Flow-Architecture forks"/>
</a>
<a href="https://github.com/ruhulmus/Git-Flow-Architecture/stargazers" target="blank">
<img src="https://img.shields.io/github/stars/ruhulmus/Git-Flow-Architecture?style=flat-square" alt="Git-Flow-Architecture stars"/>
</a>
<a href="https://github.com/ruhulmus/Git-Flow-Architecture/issues" target="blank">
<img src="https://img.shields.io/github/issues/ruhulmus/Git-Flow-Architecture?style=flat-square" alt="Git-Flow-Architecture issues"/>
</a>
<a href="https://github.com/ruhulmus/Git-Flow-Architecture/pulls" target="blank">
<img src="https://img.shields.io/github/issues-pr/ruhulmus/Git-Flow-Architecture?style=flat-square" alt="Git-Flow-Architecture pull-requests"/>
</a>
<a href="https://twitter.com/intent/tweet?text=👋%20Check%20this%20amazing%20repo%20https://github.com/ruhulmus/Git-Flow-Architecture,%20created%20by%20@rhulmus%20and%20friends%0A%0A%23DEVCommunity%20%23100DaysOfCode"><img src="https://img.shields.io/twitter/url?label=Share%20on%20Twitter&style=social&url=https%3A%2F%2Fgithub.com%2Fruhulmus%2FGit-Flow-Architecture"></a>

<p align="center">
    <a href="https://github.com/ruhulmus/Git-Flow-Architecture/issues/new/choose">Report Bug</a>
    ·
    <a href="https://github.com/ruhulmus/Git-Flow-Architecture/issues/new/choose">Request Feature</a>
</p>
 
### 👋  Git Branching/Git Work Flow to manage proper Branching

Git Work Flow Architecture is ideally suited for projects that have a scheduled release cycle. Actually Git workflows are nothing special. They are just a documented branching and integration strategy teams can adhere to in order to allow lots of people to work on a project together seamlessly.

Here i have shared the process and branching structure that i maintain for my any projects.

### 🧱 **Structure of Branch Name :**
1. **Feature** (Create branch for each feature like User Management,Project management)
2. **Dev** (Serves as an integration branch for features)
3. **Release** (Create branch for each release, it can be multiple feature or per Sprint wise delivery feature)
4. **Master** (Master branch stores the official release history. Only Latest version code will be there)
5. **Hotfix** (Create branch, if any minor change like field name, label name or any bug arise from production server)

### ⛹️‍♂️ Process/Flow  :
1. Depeloper pull the latest code from **Dev** branch
2. Create a New Feature Branch (ex: user management)
	- Developer work locally and Push/Pull and commit to **feature** branches based on each feature 
	- Completed task/feature, tested and resolved all issues for this feature. 
	- Merge feature branch into **dev** branch.
	- Delete **feature** branch.
7. Create a New release branch by forking Dev branch ( Ex: release 2.1 - created by any senior developer)
	- Deployed to a staging server for QA testing
	- Bug resolved, changes or commit to release branch.
	- Deployed the latest code in the staging server.
	- Merged into **dev** branch and as well as **master** branch
	- Delete **release** branch
13. Master branch :
	-  **Master** branch has the latest code. Now need to tag with a version number in **master** branch (ex: 2.1) *git tag -a v2.1 -m "my release 2.1"*
	-  Deployed to production server
16. Create a new **Hotfix** branch by forking master branch:
	-  Changes, resolve, tested and commit to hotfix branch
	-  Once tested, must be merged into **master** and **dev** branch
	-  Tagged again with a version number (ex: 2.2)  *git tag -a v2.2 -m "release 2.2 bug resolved"*
	-  Deployed to production server
	-  Delete **Hotfix** branch

### ✔️ Summary:
1. Master branch is the rolled out production code with tagged versions.  It's mean it's an final version of your Production Deployment.
2. Only hotfix, and release branches get merged into master (Also dev branch if needed).
3. Feature branches are merged into dev branch.
4. Only bugfixes, not new features, are merged into release branches. If development of a new feature needs to continue, it is merged into dev branch, not the release branch.


### 📒 Resources :
1. [Git Setup & Configuration](https://github.com/ruhulmus/Git-Flow-Architecture/blob/main/GIT%20Setup_configuration.pdf)
2. [Git Cheatsheet](https://github.com/ruhulmus/Git-Flow-Architecture/blob/main/git_cheatsheet.pdf)
3. [Git Workflow Diagram](https://github.com/ruhulmus/Git-Flow-Architecture/blob/main/Git-FLow.pdf)


### 📚 References : 
[Atlassian BitBucket - Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)

[Vincent Driessen - A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model")

<h3 align="center">
A ⭐️ to <b>Git Flow Architecture</b> is must as a motivation booster.
</h3>
