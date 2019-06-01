[Sprint 5 Home](README.md)|
---|

# Calculator

For this sprint we are going to work through the FreeCodeCamp ['Build a calculator'](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects/build-a-javascript-calculator/) project, preferably with another member of your bootcamp cohort. Keep it simple, it's well within your capabilities. And don't look at the sample solution just yet.

If working in a pair, you can use this time to put into practice some of the techniques you learnt about in the [pair programming](t2-pair-programming.md) primer, and remember to start your pair programming sessions with a check-in.

## Timebox

Challenge || Time|
------------|---|----------|
Calculator | (Part 1) | 15 hours
Refactor | (Part 2) | 5 hours
Reflect || 30 minutes

## Part 1 
---
## Build it!

Set up:

1. Fork the [calculator repo](https://github.com/dev-academy-foundations/calculator) from [foundations](https://github.com/dev-academy-foundations) to your github and then clone your copy.

2. After cloning your own repo, create a branch called `pseudocode` to hold the first part of this challenge. 

3. Reverse pseudocode the [sample solution](https://codepen.io/freeCodeCamp/pen/EPNZYW).\
_Remember, there is no 'right way' - the sample solution is just one implementation, but we can learn a lot by breaking it down and seeing the steps it is taking._

4. Push this to your `pseudocode` branch

Build the app:

5. Create and checkout a `first-draft` branch. If you create it while on your `pseudocode` branch, it will contain the pseudocode you created previously for reference.

6. Start with the `index.html` and building the structure, think about what buttons are needed on a calculator

7. Next, give your calculator some style. Use a CSS framework, raw CSS, or whatever you feel like to make your buttons look more like a real calculator

8. Finally, start working through the Javascript, this is the hardest part, so...
    - Take your time and work through small problems.
    - Make small commits
    - Refer to your pseudocode
    - Use the Developer Tools in your browser
    - Reference other projects/materials for app structure
    - If pairing, Change driver-navigator roles approx. every 30 mins
    - Ask for help. You can do this!

Once completed:

9. Ensure all your hard work has been pushed to your `first-draft` branch
 
10. If you did this challenge as a pair, spend 10 minutes asking each other these questions:
    - What did you find awesome about our pairing session?
    - What could have been more awesome?

    This question and answer may feel difficult, but is a very valuable learning tool. It can be kind to gently help someone identify their weaknesses so that they can work on them. Remember too that your pair may not completely understand the concept in question, so take their feedback with a grain of salt.

    - Did you notice any gaps in my understanding?


## Part 2
---
## Writing short functions

Take a look at your code from the calculator. Unless you've written perfect code, chances are some of it isn't as well-structured and [DRY](https://code.tutsplus.com/tutorials/3-key-software-principles-you-must-understand--net-25161) as it could be.

Your task now, either with your pair or working alone, is to refactor your code with a view to writing smaller functions that only have one job each. To help, consult the [Writing short functions](https://github.com/dev-academy-programme/curriculum/tree/master/resources/js-writing-short-functions-ARTICLE) resource.


1. Beginning with your calculator branch that contains the completed code from Part 1, check out a new branch called `refactor`

2. Work through all of the code, making small changes, saving and testing them frequently as you go along
    - Working slowly and methodically is key during this process. Don't be tempted to change too much at once, only to find the code breaks and you're not sure why!

3. Each time you encounter part of your code that is longer or more complex than you'd like, move some of the code into another function
    - As a very rough rule of thumb, if the function is longer than about ten lines it may need refactoring. Err on the side of creating a new function even if it seems unnecessary or pedantic, just to get the practice.

4. Each time you create a new function, and have tested it to ensure that your code still works, create a new Git commit

5. When you're done, push the new branch to GitHub

## Publish your Calculator
---

Now that you've finished creating your calculator, let's publish it to GitHub Pages so you can see it online.

As we have been working from branches, before we can publish it we need to update your `master` branch with your newly created code. There are two ways to do this:

- On github, create and merge a pull request from your branch into master

- In the command line, use `git pull origin my-branch` while on the master branch to pull the branch into your local master (replacing `my-branch` in the command with your branch name).

Once your master has been updated to contain your calculator, we can now publish the repo on GitHub.
1. Navigate to the calculator repo in your GitHub account
2. Enter the settings menu for the repo and scroll down to the GitHub Pages section
3. Under `Source`, select the master branch

This may take a small period of time to appear, but you will soon be able to go to `your-username.github.io/calculator` and see your game online!

Share your link with your cohort and post the link to the #show-eda channel on Slack with the hashtag #calculator to let other people have a go.


## Reflection

Open `my-reflections-sprint-5.md` in VS Code and add your reflections from this challenge under the heading `Calculator`.

Commit and push to GitHub