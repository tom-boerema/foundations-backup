[Sprint 1 Home](README.md)

# Branch, Pull, Merge Challenge

### Learning Competencies
By the end of this exploration, you should be able to 

- Create a new branch on a cloned repo
- Pull down changes  
- Merge changes  


## Summary

In this challenge you will test your knowledge of Git branch workflow. 

## Challenge 

Challenge | Time|
------------|----------|
Challenge | 30 minutes

## Repos within repos

__Important!__ Make sure you do not clone the new repo (Ko Wai Koe) into an already existing repo. We recommend creating a 'Dev-Academy' parent directory that can contain your Dev Academy Repos. If you put one repo inside another, it's very easy to get confused and you may end up committing the whole thing somewhere you did not intend.

Cloning to the same parent directory is fine, for example:  

Example: Good 
```sh
User/Hemi/Dev-Academy/Ko-wai-koe  
User/Hemi/Dev-Academy/A-second-repo 
User/Hemi/Dev-Academy/A-third-repo
```

Example: Incorrect   

```sh
User/Hemi/Dev-Academy/an-already-cloned-repo/a-second-repo
```
  
## Steps

1. Navigate to https://github.com/dev-academy-foundations/ko-wai-koe   
2. Clone it (somewhere other than `Foundations` repo).
3. Create a branch using your full-name e.g. `hemi-marton`.
4. Switch to (`checkout`) the new branch.
5. Create an `.md` file and save it as your-full-name (e.g. `Hemi-Marton.md`) .
6. Open your file in VS Code and write your mihimihi or copy and paste the template (below) with your answers.
7. Save your file, stage and commit it.
8. Check for and pull down any changes to the `master` branch. The simplest way is to checkout `master`, pull, and then checkout your branch again.
9. Push to a new branch on origin (hint `git push origin your-name`).
10. Create a new pull request (hint: navigate to the repo on GitHub, choose your branch and click _New pull request_.
11. Ask someone in your cohort to `merge` your pull request and delete your branch.
12. Checkout master and pull down changes.

## Resources 

- [Create Simple Pull Request - YouTube](https://www.youtube.com/watch?v=rgbCcBNZcdQ)  
- [Code School Git Real - Cloning and Branching](https://app.pluralsight.com/player?name=f83ca95c-74e2-4a1d-8742-62b34ec47906&mode=live&clip=0&course=code-school-git-real&author=gregg-pollack)  
- [Atlassian Git Branching](https://www.atlassian.com/git/tutorials/using-branches) 
- [Opening VS Code in Command Line](/resources/vs-code-in-terminal.md) 

## Template:

__Where I grew up:__   
__Where my family is from:__    
__My name:__   

---

## Side Note:

Sometimes when you `git pull` work into a repo you have been working in you will find that a file you have been working on has an issue when you pull. This is known as a "merge conflict". Someone else has been making changes to the same file too! If this happens, here is a link to a quick walkthrough on what to do: [Merge conflicts](/resources/resolving-conflicts.md)


---

## Change the Curriculum:

Now that you're comfortable with how to clone, create a new branch and create a pull request, you can now use these skills to suggest changes to the foundations curriculum!
If you see a typo, or a link has stopped working, you can create a branch to make the changes you want to make. Remember to pull before pushing, and push to `git push origin your-branch-name`, NOT to master. Then create a pull request and we can review your changes.
