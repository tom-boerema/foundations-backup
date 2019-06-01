[Sprint 2 Home](README.md)|
---|

# Your Blog - primer and setup

### Learning Competencies
By the end of this primer, you should be able to

- Understand the purpose of your blog
- Add a blog directory with template HTML
- Link your css file to your HTML file

## Summary
This Sprint is about building your blog using HTML and CSS while honing your GitHub and command line skills. You'll be learning HTML and CSS through online resources and applying what you learn to your own blog website.


## Timebox

Activity | Time|
------------|----------|
Setup part one | 20 minutes |
Setup part two | 20 minutes
Reflect | 10 minutes |


## Overview
Last Sprint you set up the beginnings of your github pages blog (`username.github.io`). You'll be expanding this with HTML,  CSS and JavaScript as you apply your learning throughout the sprints.

Your blog is a practical way to apply your learning and it will go towards your Foundations assessment. Take special note, that you will not be judged on your design application. Quite the contrary, we don't mind so much about what your blog looks like, but rather _how_ you engaged with the material; the quality of your reflections; how you identified obstacles and overcame them; if you can demonstrate an understanding of the concepts and learning objectives and how frequently you engaged and staged commits.

What your Blog is: A space where you demonstrate your skills in problem solving and reflections.
What your Blog is not: A fancy looking, perfectly put together interface.

We will however introduce you to the important aspects of design thinking, and hope that you can incorporate those into your blog.

Throughout the sprints, you'll be presented with bunch of ways to learn HTML, CSS and JS building blocks.

Some of the resources we point you towards will be media rich with audio and video. Other's, like freeCodeCamp, will look more like a terminal screen.

__This is your journey and its up to you to discern how you learn best.__

Our role is to help facilitate your critical thinking: in other words, help you identify and take ownership for where your knowledge gaps are, and to assist you in figuring out how to fill those gaps. In the world of web development, your problem solving skill set is your greatest asset. As a result of this method, the step by step instructions (like those below) will become intentionally less detailed as you move through the curriculum.

In all instances, follow the timeboxing prompts, attend the check-in's, keep to the learning objectives and reflect.

## Introduction
- In the previous challenge you started a GitHub pages repository: `username.gihub.io`.  
- Each Sprint you will create a new blog post within that repo, using HTML, CSS and JavaScript.
- Blogs will follow the naming convention sprint#-module. For example sprint1-technical and sprint1-core.

## Set up part one - Add HTML
This steps adds HTML template as a placeholder

Pro-tip-1: You can create many common file types (e.g. .html, .css) the same way you create .txt and .md files (hint: `touch`)

Pro-tip-2: If adding a new file to a new directory, remember to navigate __INTO__ new file directory after you make it.

1. Navigate to the directory where you saved your `username.github.io` repo
2. __Inside of__ the `username.github.io` directory, create a new directory called `blog` _(hint: `mkdir`)_
3. __Inside of__ the `blog` directory create a file `sprint1-technical.html` _(hint: `touch`)_
4. Open `sprint1-technical.html` in your code editor _(hint `code`)_
5. Copy [this template](/resources/sprint1-technical.html) and paste it into `sprint1-technical.html`.
4. Add and commit your changes with a good commit message
5. Push your changes
6. Visit your page on your web browser `username.github.io/blog/sprint1-technical.html`

## Set up part two - Add CSS
This step setups the directory structure for your css. The file `main.css` uses a standard naming convention (almost all websites have a file named main.css file)

1. Navigate to the directory where you saved your `username.github.io` repo
2. __Inside of__ the `username.github.io` directory create a new directory called `styles`.
3. __Inside of__ the `styles` directory, create a new file called `main.css`


## Set up part three - Link HTML and CSS
Each HTML file will need to be explicitly linked to a CSS file. This step you'll remove the placeholder link in your HTML file and link the `main.css` file you just created.

1. Navigate to your `sprint1-technical.html` file  
2. Replace the place holder as shown below  

```html

Old
<link href="your-stylesheet-link-here.css" rel="stylesheet" type="text/css">  `<title>My blog</title>`

New
<link href="styles/main.css" rel="stylesheet" type="text/css" />

```

If stuck, [This video demo's linking to css at at 5.08](https://www.youtube.com/watch?v=gBi8Obib0tw)

## Opening Your Changes in a Browser
You don't have to push your changes to github in order to see how the changes you have made in your file look in the browser. You can simply open the html file and your local copy will show in your browser so you can check it out before you push it and make it go live. Follow the instructions below for either Mac or Windows to do this -

Mac:
Use the terminal to navigate to the directory that the relevant file is located in, and use the command
`open index.html` (replace index.html with the actual file name you want to open if it is not called index.html).
If you want to use a particular browser, use the command
`open -a "Google Chrome" index.html` (replace "Google Chrome" with whichever browser you'd like to use).

Windows:
Use Git Bash for Windows to navigate to the directory that the relevant file is located in, and use the command
`explorer .` This will open up your explorer at the current directory. Double click the html file to open it in a browser.

## Reflect
Navigate to your `my-reflections-sprint-2` file (Pro-tip: Use terminal) and add your reflections from this challenge. The questions are under the heading `Your Blog` in that file.

Stage, commit, and push to github.


## Visual references


<figure>
  <figcaption>
    <p><strong>Figure 1:</strong> Add blog directory</p>
  </figcaption>
  <img src="/resources/images/blog-1-mkdir.png" alt="adding directory"><br>
</figure>

<figure>
  <figcaption>
    <p><strong>Figure 2:</strong> t1-blog in browser</p>
  </figcaption>
  <img src="/resources/images/blog-2-template-on-web.png" alt="photo of blog template on browser"><br>
</figure>
