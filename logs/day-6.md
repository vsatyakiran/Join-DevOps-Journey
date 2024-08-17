---
layout: default
title: Day 6 - Git and GitHub
---

# Day 6: Git and GitHub

<div class="date">August 14, 2024</div>

Version control system(Git and GitHub)
--------------------------------------

# What is version control?

It helps you track different versions of your code and collaborate with other developers.

VCS can be categorized into three models:

**1. Local VCS:** Here, the database is stored on the hard disk of the local machine.

**2. Centralized VCS:**  Here a centralized server exists, every developer takes the code from that repo. 

 **Disadv:** Single point of failure.

**3. Distributed VCS:** Each developer has a complete copy of the project, allowing offline work and later synchronization with others

#  What is Git?

Open source distributed version control system.

Git is a widely-used distributed version control system, allows multiple developers to work on the same project simultaneously.

# What is GitHub?

GitHub is a cloud-based hosting platform built on top of Git. It allows developers to store, manage, and track their codebase and collaborate with others.

# Why Git Famous?

- Previous VCS like CVS, SUN are centralized systems, where git is a distributed VCS.

- **Branching and Merging:** Git allows for easy branching and merging of code, making it simple to work on multiple features simultaneously.

- **Data Integrity:** Git uses a SHA-1 hash to ensure data integrity, making it difficult to change the contents of a file without Git knowing.

- **Open Source:** Git is open source and has a large community of developers contributing to its development.

<hr>

# Git Branching Strategy

<div class="date">August 15, 2024</div>

# What is branching?

It allows you to create a new version of the codebase that is separate from the main branch, which is usually called "master".

When you create a new branch in Git, you are creating a new pointer to a specific commit in the repository. This new branch is a copy of the current state of the repository at that point in time.

Common Git branching strategies include:

- **Feature branching:** Creating a new branch for each new feature or set of features.

- **Release branching:** Creating a new branch for each new release or version of the software.

- **Hotfix branching:** Creating a new branch to fix a critical bug or issue.

<hr>

# Rebase vs Merge

- **Merge:** Retains the original branch history, creating merge commits to integrate changes. This leaves a clear history that shows the integration point. Merge is considered a safe option that preserves the entire history of the repository.

- **Rebase:** Rewrites the commit history by transplanting changes onto a new base commit. This creates a linear development history without merge commits and removes unwanted entries. Rebase takes all the changes, compresses them into a single patch, and integrates the patch onto the target branch.

<hr>

# Interview Questions

1) How to unstage git?

git restore filename

2) rename Branch : git branch -m old-branch new-branch

3) Rename File : git mv OLD-FILENAME NEW-FILENAME

4) Git all remote urls : git remote -v

5) Clone vs Fork?

**Fork:** Get copy of repository to my GitHub

**Clone:** Downloading the repo 

6) How to get history?

git log, we can go to previous commit using 

7) What is git cherry-pick? 

Used to merge the two branches, it is helpful only there are few commits because we use commit hash to merge

8) What is git stash?

git stash is used to save the changes in the working directory and index, and revert to a clean working directory.

9) What is git rebase?

Rebase is used to integrate changes from one branch to another. It is an alternative to merge and results in a cleaner commit history.

10) What is git pull?

git pull is used to fetch and download content from a remote repository and immediately update the local repository to match that content.

# Key Points

- **Version Control System:** A system that records changes to a file or set of files over time so that you can recall specific versions later.

- **Git:** A distributed version control system that allows multiple developers to work on the same project simultaneously.

- **GitHub:** A cloud-based hosting platform built on top of Git that allows developers to store, manage, and track their codebase and collaborate with others.

- **Branching:** Creating a new version of the codebase that is separate from the main branch, allowing for parallel development.

- **Merge:** Integrating changes from one branch into another, creating merge commits to retain the original branch history.

- **Rebase:** Rewriting the commit history by transplanting changes onto a new base commit, creating a linear development history without merge commits.

# Resources

- [Git Handbook](https://guides.github.com/introduction/git-handbook/)

- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)

- [Pro Git Book](https://git-scm.com/book/en/v2)

# Conclusion

Understanding Git and GitHub is essential for modern software development. By mastering version control systems, you can collaborate effectively with other developers, track changes to your codebase, and manage complex projects with ease.

<div class="navigation"> 
    <a href="day-5.html"> << Prev: Shell Scripting </a> 
    <a href="../allfiles.md"> All Logs </a>
    <a href="day-7.html"> Next:  >></a>
</div>