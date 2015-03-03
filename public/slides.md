layout: true
class: middle

---

# Git and Github

---

# Maybe you're wondering
* What is Git/Github?
* Why Git/Github?
* How Git/Github?

---

# What is Git?
Git is a version control system. A version control system is a piece of software designed to keep track of the changes made to files over time.
More specifically, Git is a distributed version control system, which means that everyone working with a project in Git has a copy of the full
history of the project, not just the current state of the files.

.center[![Git](http://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Git-logo.svg/170px-Git-logo.svg.png)]

---

# What is Github?
Github is a website where you can upload a copy of your Git repository. It provides a centralized location to share the repository, a web-based
interface to view it, and additional features which allow you to specify, discuss, and review changes.

.center[![Git](http://media.creativebloq.futurecdn.net/sites/creativebloq.com/files/images/2013/06/16-logo.jpg)]

---

background-image: url(http://pavetech.olhblogspace.com/wp-content/uploads/2012/09/teamwork_teamwork_A.jpg)

---

# Why Bother With Git?
* Complete history of all changes
* Undo changes
* Restore deleted or overwritten files
* Confidently change anything
* Documentation of who/when/why changes were made
* A central authoritative source for up to date documentation and code
* Allow collaboration on the same file(s) without stepping on each other

---

# Git Lets You Do This:

.center[![Git](http://hades.name/media/git/git-history.png)]

---

# Git Basics
* **Clone:** Download a repository
* **Commit:** Snapshot your local repository
* **Push:** Send your commits to your remote repository
* **Pull:** Get others' commits from your remote repository

.center[![Git](http://guides.beanstalkapp.com/version-control/intro-to-version-control/cvc.png)]

---

# Installing Git
http://git-scm.com/download/win

---

# Enable Explorer Integration
.center[![Git](/git_setup.png)]

---

# 1st Option
.center[![Git](/git_setup2.png)]

---

# 1st Option
.center[![Git](/git_setup3.png)]

---

# Tell Git Who You Are

```bash
$ git config --global user.email "you@example.com"
$ git config --global user.name "Your Name"
```

---

# Working With Local Repositories

---

# Git Init

```bash
$ cd demo
$ git init
```

---

# Staging

```bash
$ git status
$ git add file.txt
```

---

# Commit

```bash
$ git commit -m "What changed and why"
```

---

# Viewing an Old Revision

```bash
$ git log
$ git checkout a1e8fb5
$ git checkout master # go back
```

---

# .gitignore File
* Keep passwords, keys, and other sensitive information out of git
* Don't need to track log files most of the time

---

# Working With Remote Repositories

---

# SSH Keys
https://help.github.com/articles/generating-ssh-keys/

---

# Create a Repository

.center[![Git](https://help.github.com/assets/images/help/repository/repo-create.png)]

---

background-image: url(https://help.github.com/assets/images/help/repository/repo-create-name.png)

---

# Git Push

```bash
$ git remote add origin git@github.com:jrabovsky/demo.git
$ git push -u origin master
```

---

# Git Clone

```bash
$ git clone git@github.com:jrabovsky/demo.git
```

.center[![Git](https://help.github.com/assets/images/help/repository/clone-repo-clone-url-button.png)]

---

# Git Pull

```bash
$ git pull
```

---

background-image: url(http://jordankasper.com/git/images/DistributedVCS.png)

---

# Merge Conflicts

```bash
$ git pull
remote: Counting objects: 3, done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From github.com:jrabovsky/demo
   46c3bca..a2698e8  master     -> origin/master
Auto-merging animals.txt
CONFLICT (content): Merge conflict in animals.txt
Automatic merge failed; fix conflicts and then commit the result.

$ git status
On branch master
Your branch and 'origin/master' have diverged,
and have 1 and 1 different commit each, respectively.
  (use "git pull" to merge the remote branch into yours)

You have unmerged paths.
  (fix conflicts and run "git commit")

Unmerged paths:
  (use "git add <file>..." to mark resolution)

        both modified:   animals.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

---

# But Wait, There's More!
* Branching/merging
* Pull requests
* Tagging
* Submodules
