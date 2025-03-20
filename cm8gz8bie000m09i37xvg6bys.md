---
title: "Source Code Management : Git & GitHub Fundamentals That Everyone Should Know."
datePublished: Thu Mar 20 2025 06:35:02 GMT+0000 (Coordinated Universal Time)
cuid: cm8gz8bie000m09i37xvg6bys
slug: source-code-management-git-and-github-fundamentals-that-everyone-should-know
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1742452247493/343c2c05-28f0-4283-b080-cfcf64001753.webp
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1742452477962/c4b2ddb0-037f-4f42-a921-902ddff33692.webp
tags: github, git, devops, devops-journey, learninpublic, trainwithshubham, tws, devopscommunity, source-code-management

---

Before getting deep dive into the git and github, i learn the history and some fundamentals.

## What is GIT?

* ### History :
    

Basically, Git is a Global Information Tracker Tool Which is Developed by the Founder of Linux Linus Torvalds to track the changes and for maintaining the history of the changes in code.

* ### what is VCS? (Version Control System
    
    * You can use git even when you're offline.
        
    * Create branches, work locally, isolate your work and merge seamlessly.
        
    
    Code revisions (commit) that you made would be available to only you locally unless you push to remote repo.
    

## **What is GitHub :**

GitHub is **a web-based platform for version control and collaboration among software developers**. It allows users to store, manage, and track changes to their code, facilitating collaboration on projects with tools for managing changes from multiple contributors.

GitHub is owned by Microsoft and is used by over 150 million developers, including 90% of Fortune 100 companies.

( Note : There are other platforms like GitLab, BitBucket, AWS Code Commit, Azure Repo )

The most features of version control sysytem it provides :

* Local & Remote
    
* Date & Time
    
* Author
    
* History
    
* Restore & Recover
    

## Stages in Version Control System

There are a three stages in a git…

* Untracked
    
* Staged
    
* Tracked
    

Firstly, Any changes that we made are in the Untracked stage.

From Untracked to Staged, We use a `git add <file name>` ( only a specified file ) also `git add .` ( it pushes all changes at once without specifying it to staged.)

If we want push changes from staged to get it tracked. - `git commit -m <message>`

Also you can revert the changes from staged to untracked by doing `git rm -- cached <file_name>`

## **Repository Management**

* ### **Cloning a Repository**
    

To create a local copy of an existing GitHub repository, use:

This downloads all the project files, history, and branches to your local system.

* ### **Forking a Repository**
    

Forking creates a personal copy of someone else’s repository in your GitHub account. This allows you to modify the project without affecting the original repository.

* ### **Understanding GitHub Repositories**
    

A repository (repo) is a storage location for project files, including their version history. GitHub repositories allow multiple developers to collaborate using features like pull requests and issue tracking.

## **Configuring GitHub to Local**

To connect your local Git repository with GitHub, follow these steps:

* Set your global username and email in Git:
    
    `git config - - global user.name <username>`
    
    `git config - - global user.email <email>`
    
* Link your local repository to a remote GitHub repository:
    
* Verify the remote repository.
    
* Push your local commits to GitHub.
    

## Workflow & Commonly Used commands.

Let's review a simple project workflow and the CLI commands that help us move from one step to the next. Below is a diagram of a workflow including Git & Github. This diagram most closely represents the flow of

![Simple Git Workflow](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fvpxeexqyfvf4hw3zxtbn.png align="left")

* **git clone**
    

The very first step (not included on diagram) is to clone the repository to your local machine. Be sure to clone the project in a working directory that makes sense so you can easily remember where your local project lives.

* **git pull origin master**
    

Next, pull down from the remote repository (reminder, this lives on GitHub) to make sure you have up to date information. Believe it or not, changes could have been made by a team member in the time it took you to clone down the repository to your computer.

* **git checkout -b new\_branch\_name**
    

Create your own branch! If you’re working in a group project like I was, you will probably want to create a new branch for the feature you are working on. Make sure you are titling your branch according to the standards of your workplace expectations. You now have your own little place to experiment with code without immediately affecting changes on the master branch!

\*\* **note**: you might not need to create a new branch if you are intentionally editing an existing branch. In that case, be sure you are on the correct branch and not the master prior to making any changes. Always check with your teammates before creating/editing branches.

* **git add file\_name**
    

After your code has been tested and is complete, add your changes to the staging area. This means that your files are tracked by Git, changes are complete, and code is prepped, and ready to be added back to the repository.

**git status**

Run git status to confirm that your files have been added to the staging area. If the name of the file is listed in green - you're good to go! If not, try adding again.

* **git commit -m "valuable\_but\_short\_message\_here"**
    

Commit your changes back to the repository. Add a brief, but detailed comment about the changes that were made, code that was written, or bug that was fixed. Make it easy for your team members and future team members to understand what the alterations were.

* **git push branch\_name**
    

Next up - push your changes to the repository! You have now transferred your code up to GitHub. The code you've pushed up lives in the current branch you've worked on. We learned (the hard way) how important it is work on your branch *and* to push to your own branch. If you accidentally push up to the master you run the risk of overwriting code the master branch which lives within GitHub.

![Diagram of Pushing Branches to Branches in GitHub](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F3af6c4hearaarbhyezwn.png align="left")

Finally, you'll need to create a **pull request** through GitHub. This may vary depending on the nature of the project. Submitting a pull request will notify the owner of the repository that you are ready to merge your code with the master branch. It is up to the owner to review your code prior to finalizing the merge. In our particular situation we had team members look at the code together as we completed the pull request. Because we were still relatively new to the GitHub process, we wanted to be sure that no code was accidentally overwritten when a branch was merged with the master.

![Image of Pull Request example from GitHub](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fr5dy45nshfrhvenb0wdn.png align="left")

* **git pull origin master**  
    This command was mentioned above as the first thing you should do after cloning to your machine. Again, you'll need to complete this once the master has been revised. This command gets a *honorable mention* for playing a critical role in keeping your working version up to date. After the master branch in a repository has been updated from a pull request, be sure to pull down from the repository into your local branches. This will ensure that you are working on the most up to date files moving forward.
    

## **Authentication in GitHub-**

Their is two ways -

1. Using PAT (Personal Access Token)
    
2. Using SSH
    

* ### **Using Personal Access Token (PAT)**
    
* GitHub has replaced password-based authentication with Personal Access Tokens (PATs) for enhanced security. To generate a PAT:
    
    1. Go to GitHub → Settings → Developer Settings → Personal Access Tokens.
        
    2. Generate a token with required permissions (e.g., `repo` access).
        
    3. Use the token instead of a password when pushing or pulling.
        
* ### Using SSH
    
* To use SSH, you should have a public and private key for that, if you do not have a keys you can generate the keys. by doing `ssh -keygen`
    
* Go to .ssh and their you have the `ed25519 (private key) and ed25519 (public key)`
    
* Copy the public key by opening it.
    
* Go to GitHub → Settings → SSH and GPG keys → New SSH key → Paste the public key → Save.
    

Now,GitHub(Remote) has my public key and my local has a priavate key,

you can securely push and pull repositories without entering credentials repeatedly

## Conclusion

I hope that this post helps to explain some of the fundamentals of using both Git and GitHub. Writing this blog was a valuable exercise to me, as I was able to reflect on the processes that challenged and learn more about them through further research. Note that there are many common commands that this post didn't cover and I encourage you to look those up as needed. I’d love to hear feedback on this post -comments are welcome!

Happy Learning!