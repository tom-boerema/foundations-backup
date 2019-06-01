[Sprint 1 Home](README.md)|
---|

# Branch, Pull, Merge Primer

### Learning Competencies
By the end of this exploration, you should be able to 

- Explain what a branch is and why we use it

## Summary
Shared from [GitHub Guides](https://guides.github.com/introduction/flow/)

When you're working on a project, you're going to have a bunch of different features or ideas in progress at any given time – some of which are ready to go, and others which are not. Branching exists to help you manage this workflow.

When you create a branch in your project, you're creating an environment where you can try out new ideas. Changes you make on a branch don't affect the master branch, so you're free to experiment and commit changes, safe in the knowledge that your branch won't be merged until it's ready to be reviewed by someone you're collaborating with. 

## Challenge 

Challenge | Time|
------------|----------|
Explore | 1 hour 
Reflect | 1 hour 

## Introduction 

By default, all repositories have a master branch. This is where the most perfect, well-tested code lives. The master branch should be the most ideal version of your code and always working/running properly.

In cases where people want to make changes or add features, they will make a new branch off of the master (using `git checkout branch-name`). This will take a copy of the code from the master and allow you to make changes and test them out. Once they are fully tested, they can be merged back into the master branch.

When you work in teams, it's always a good idea to have someone else review your code before it's merged into master. This is done through a pull request. A pull request is a friendly way of saying: "Hey boss! I'm done implementing this feature your asked for, can you review my code?". When working in a team, it is best practice to have at least 1 other person review your pull request and they should be the person to merge it once the changes are approved.

## Creating a Branch 

You can create a branch via the command line or on GitHub itself. 

When using your command line, you can see your local branches (the branches on your local computer) by typing:

`git branch`

If you want to see your local and remote branches, type:

`git branch -a`

Remote branches are also located on GitHub.com.


## Explore 
Explore and try out Git Branching online. You'll use what you learn in a following branching challenge. 

- [Code School Git Real - Cloning and Branching](https://app.pluralsight.com/player?name=f83ca95c-74e2-4a1d-8742-62b34ec47906&mode=live&clip=0&course=code-school-git-real&author=gregg-pollack)
- [Understanding the GitHub Flow](https://www.youtube.com/watch?time_continue=18&v=PBI2Rz-ZOxU)
- [Create Simple Pull Request - YouTube](https://www.youtube.com/watch?v=rgbCcBNZcdQ)
- [Atlassian Git Branching](https://www.atlassian.com/git/tutorials/using-branches)


## Reflect
Open your text reflections file and answer the following. 

- What is Master?
- Why create a Branch?
- Do the concepts introduced feel intuitive or difficult to understand?




