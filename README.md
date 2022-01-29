# Git-Flow-Architecture
Git Work Flow Architecture for Git branching

### **Structure of Branch Name :**
1. **Feature** (Create branch for each feature like User Management,Project management)
2. **Dev** (Serves as an integration branch for features)
3. **Release** (Create branch for each release, it can be multiple feature or per Sprint wise delivery feature)
4. **Master** (Master branch stores the official release history. Only Latest version code will be there)
5. **Hotfix** (Create branch, if any minor change like field name, label name or any bug arise from production server)

### Process/Flow  :
1. Depeloper pull the latest code from **Dev** branch
2. Create a New Feature Branch (ex: user management)
	3. Developer work locally and Push/Pull and commit to **feature** branches based on each feature 
	4. Completed task/feature, tested and resolved all issues for this feature. 
	5. Merge feature branch into **dev** branch.
	6. Delete **feature** branch.
7. Create a New release branch by forking Dev branch ( Ex: release 2.1 - created by any senior developer)
	8. Deployed to a staging server for QA testing
	9. Bug resolved, changes or commit to release branch.
	10. Deployed the latest code in the staging server.
	11. Merged into **dev** branch and as well as **master** branch
	12. Delete **release** branch
13. Master branch :
	14. **Master** branch has the latest code. Now need to tag with a version number in **master** branch (ex: 2.1) git tag -a v2.1 -m "my release 2.1"
	15. Deployed to production server
16. Create a new **Hotfix** branch by forking master branch:
	17. Changes, resolve, tested and commit to hotfix branch
	18. Once tested, must be merged into **master** and **dev** branch
	19. Tagged again with a version number (ex: 2.1.1)  git tag -a v2.1.1 -m "release 2.1 bug resolved"
	20. Deployed to production server
	21. Delete **Hotfix** branch

### **References : **
[Atlassian BitBucket - Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
[Vincent Driessen - A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model")