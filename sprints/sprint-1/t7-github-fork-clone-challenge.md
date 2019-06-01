[Sprint 1 Home](README.md)|
---| 

# GitHub Fork & Clone Curriculum Challenge

### Learning Competencies
By the end of this exploration, you should be able to:

- Fork a repository 
- Clone a forked repository

## Summary
You will use this deep dive exploration to create your own forked version of a repo. You will then clone a copy to your machine. This clone is where you will be working on reflections for the rest of your learning exploration and assessments. 


## Timebox

Activity | Time|
------------|----------|
Explore | 45 minutes 
Fork, Clone | 1-2 hours
Reflect | 15 minutes |

Follow the timebox suggestions. If you get stuck, take a quick break and come back to it. Reach out to the community on slack. Let the learning competencies be your guide.

## Introduction 

In this challenge, you will be creating your own forked version of the reflections repo which you'll work with throughout Foundations. By creating a forked version, your changes will not show on the master EDA version.

> "A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project.  
Most commonly, forks are used to either propose changes to someone else's project or to use someone else's project as a starting point for your own idea." [Official GitHub article](https://help.github.com/articles/fork-a-repo/)

## Forking Workflow 

[Excerpt from Atlassian](https://www.atlassian.com/git/tutorials/comparing-workflows/forking-workflow)  

The Forking Workflow is fundamentally different than other popular Git workflows. Instead of using a single server-side repository to act as the “central” codebase, it gives every developer their own server-side repository. This means that each contributor has not one, but two Git repositories: a private local one and a public server-side one. The Forking Workflow is most often seen in public open source projects.

The main advantage of the Forking Workflow is that contributions can be integrated without the need for everybody to push to a single central repository. Developers push to their own server-side repositories, and only the project maintainer can push to the official repository. This allows the maintainer to accept commits from any developer without giving them write access to the official codebase.

The Forking Workflow typically follows a branching model based on the Gitflow Workflow. This means that complete feature branches will be purposed for merge into the original project maintainer's repository. The result is a distributed workflow that provides a flexible way for large, organic teams (including untrusted third-parties) to collaborate securely. This also makes it an ideal workflow for open source projects.

## Explore Forking 

Use the Timebox suggestions and exploring Forking. 

Suggested Resources:  
[GitHub for Poets Forks and Pull requests](https://www.youtube.com/watch?v=_NrSWLQsDL4)      
[Practice Forking GitHub Help](https://help.github.com/articles/fork-a-repo/)      
[Atlassian Forking Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/forking-workflow)    


## Step 1: Fork
Navigate to the [reflections repo](https://github.com/dev-academy-foundations/reflections) in the foundations organisation.

Create your own version of the repo by forking it to your account. Below is an example of this process using the foundations repo.  

__Origin:__ https://github.com/dev-academy-foundations/reflections  
__Destination:__ https://github.com/YOUR-GITHUB-USERNAME/reflections 

<figure>
  <figcaption>
    <p><strong>Figure 1:</strong> Fork Repo from origin</p>
  </figcaption>
  <img src="/resources/images/github_1_original.png" alt="Fork GitHub Repo"><br>
</figure>


<figure>
  <figcaption>
    <p><strong>Figure 2:</strong> View of Forked repo in destination </p>
  </figcaption>
  <img src="/resources/images/github_3_forked.png" alt="View Forked GitHub Repo"><br>
</figure>


## Step 2: Cloning
Right now your repository exists on GitHub, but in order to add or edit files using your text editor, you need it to exist on your computer (i.e. you need to clone it locally). 

<figure>
  <figcaption>
    <p><strong>Figure 3:</strong> Clone button </p>
  </figcaption>
  <img src="/resources/images/github_4_clone_button.png" alt="gitHub clone button"><br>
</figure>


1. Click the clone button (copies link) (figure 3)
2. You're about to paste the link you just copied. When you do so it will create a directory called 'foundations'. __Think about where you that directory to live.__  Is it for example in `desktop/dev-academy/reflections` or does it make more sense to have it on your root directory e.g. `users/hinemoana/reflections` ? There is no right answer, just a location that makes the most sense to you (that isn't itself a git repo).
3. In your terminal, navigate __INTO__ the directory you created/would like to use to hold the cloned repo.
4. Enter the command `git clone` and use keyboard shortcut `cmd v` (mac) or `ctrl v` (win) to paste
5. Follow the username and password prompts if required.

<figure>
  <figcaption>
    <p><strong>Figure 4:</strong> Terminal commands for cloning </p>
  </figcaption>
  <img src="/resources/images/github_5_git_clone_terminal.png" alt="gitHub terminal clone commands"><br>
</figure>

## Step 3: Open in Visual Studio Code
Visual Studio Code is a text editor you installed during initial setup. You may have also dabbled in other text editors like 'Atom' or 'Sublime Text' but for this course, our editor of choice is Visual Studio (VS) Code. Open VS Code and then open the reflections directory you just cloned.

<figure>
  <figcaption>
    <p><strong>Figure 5:</strong> Local cloned repo viewed in text editor </p>
  </figcaption>
  <img src="/resources/images/github_6_clone_open_visual_studio.png" alt="local repo in terminal"><br>
</figure>


## Step 4: Add your (previous) Reflections 
The repo you cloned has a folder for each of the sprints you will do, and a`my-reflections` markdown (`.md`) file in each folder, as well as an `end-of-sprint` file that contains the checklist and final reflections you will do once the sprint is completed.  
From now on, you'll add your reflections to these files on your __local version of repo__ and push them back up to your forked version on GitHub.  

Have a look around the files in the sprint 1 folder. If you would like to hold any other reflections or noticings in this repo, please feel free to add your own files.

__Pro-tip: Use command line to navigate, open applications and open files.__

1. Open the reflections repo in VS Code. 

2. Copy and paste your previous reflections into the file. Use [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) to make the question format 'bold' or into headers.  
3. Stage your file. 

## Reflect
Open `my-reflections-sprint-1.md` in VS Code and add your reflections from this challenge. The questions are under the heading `GitHub Fork & Clone` in that file.

Stage, commit, and push the reflections repo to github.

## Additional Practice and Resources
[GitHub Guides - Practice Forking Projects](https://guides.github.com/activities/forking/)  
[Git the simple guide](http://rogerdudler.github.io/git-guide/)
[Forking (GitHub Article)](https://help.github.com/articles/fork-a-repo/)

