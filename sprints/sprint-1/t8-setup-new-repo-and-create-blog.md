[Sprint 1 Home](README.md)|
---|

# Setup new Repo & Create Blog Challenge

## Learning Competencies
By the end of this you should be able to:

- Create a new repository
- Understand what GitHub pages are
- Have a skeletal framework to build your blog 


## Summary
Today you'll begin a blog that you'll work on throughout Foundations and you'll do so using a service called [GitHub Pages](https://pages.github.com/). You'll create a repo, clone a repo, add some files and push it up to GitHub Pages.



## Application

Application | Time|
------------|----------|
Create a website repository | 20 minutes 
Reflect | 15 minutes |


## Introduction 

The purpose of the blog is triple fold: 
- To continue honing your skills in GitHub workflow  
- To provide a home for assignments and reflections  
- To practice HTML, CSS and JS.  

It can be tempting to tinker for hours with the visual elements of your blog, but there is no award for best design. 

Stay focused, stay sharp. You're here to learn breadth, not depth. 

As always, keep your learning objectives in mind and hone your practice. Follow the timebox suggestions and reach out to the community if you feel blocked.



## Create a new Repo 
1. Create a [new repository](https://github.com/new) 
2. Use the syntax `your-github-username.github.io` for your repository name (example Figure 1). Make sure you use your _GitHub username_ when naming this repo, otherwise GitHub Pages won't work correctly when we set it up
3. Select the options shown in Figure 1

<figure>
  <figcaption>
    <p><strong>Figure 1:</strong> Preference setting for New GitHub repo</p>
  </figcaption>
  <img src="/resources/images/github_13_new_repo.png" alt="Create new repo"><br>
</figure>
  

## Clone Repo
__Important!__ Do not clone into an already existing repo (e.g. reflections). 

Cloning to the same parent directory is fine, for example:  

Example: Good   
`User/Kiri/Dev-Academy/reflections`    
`User/Kiri/Dev-Academy/ko-wai-koe`  
`User/Kiri/Dev-Academy/jamanius.github.io` 

Example: Incorrect   
`User/Kiri/Dev-Academy/ko-wai-koe/jamanius.github.io` 

1. Navigate to the directory where you want to clone your github.io repo
2. Clone it 


## Add a temporary index.html file 
1. Navigate __INTO__ the github.io repo 
2. Create a file called `index.html` (in command line type `touch index.html`
3. Open index.html with VS
3. Add this text to the index.html file and __save it__

```html
<html>
  <head>
    <title>My blog</title>
  <body>
    <h1>Kia ora Taiao! (Hello World!)</h1> 
    <p> This is the beginning of my website home page.</p>
    <p> It will eventually contain a list of links to all my blogs. </p>
  </body>
</html>

``` 
## Commit and Push 

1. Commit and Push the changes to GitHub
2. Navigate to your [USERNAME].github.io repo on GitHub
3. Enter the settings menu for that repo and scroll down to the GitHub Pages section
4. Under the `Source` option, select the master branch
5. You can check out your live repo by visiting `http://[USERNAME].github.io`* 

<figure>
  <figcaption>
    <p><strong>Figure 3:</strong> Example of Blog online.</p>
  </figcaption>
  <img src="/resources/images/github_15_blog_index.png" alt="image of website blog"><br>
</figure>

_Note: After pushing to GitHub pages, there might be a delay - it can sometimes take 15 minutes for your site to rebuild on GitHub, so don't be surprised if you can't see changes immediately_


## Step 5: Reflect 
Open `my-reflections-sprint-1` and answer the questions following `Setup Repo & Create Blog`.

Add, commit and push!


