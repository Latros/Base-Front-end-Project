This week I spent a large chunk amount of time learning the ins & outs of Grunt, Yeoman & Bower (henceforth referred to as GYB). I've been using them for awhile, but mostly by copying other peoples Grunt tasks and never truly hunkering down to *learn* them. That's what I did this week.

I'm by no means an expert, but I definitely feel comfortable enough with each to confidently say "if you're a developer who ISN'T using these, you're *probably* taking crazy pills, or just don't know any better". Either way, if you read through this article, hopefully you'll see the light :)

GYB is what I'll call a "workflow stack". The stack is aimed at making development faster, easier, and (best of all) more automated. It allows for a lot of the boilerplate "best practice" techniques used in web development to be done automatically behind the scenes, freeing up your time and brain to focus on the fun stuff (the programming, not the grunt work!).

Here's a breakdown of a bunch of common tasks that almost every web developer will find themselves doing at some point:

Asset minification / concatenation tasks that you *shouldn't* be doing manually
===============================================================================
- Compiling your LESS/SASS into CSS (either client side or on the server side)
- Minifying (incl. removing comments) JavaScript & concatenating it all into one .JS file
- Minifying (incl. removing comments) CSS/LESS/SASS & concatenating it all into one .CSS/LESS/SCSS file
- Minifying (incl. removing comments) your HTML

Workflow tasks that you *shouldn't* be doing manually
=====================================================
- Changing a file, alt-tabbing to your browser, hitting refresh (this method is still used far too much these days!)
- Going to jQuery.com or getbootstrap.com, downloading the latest jquery/bootstrap, dragging it into your projects library directory, and then writing the script/link tag in your HTML. This applies to *any* javascript or css framework that you would need to fetch for your project

Deployment tasks that you *shouldn't* be doing manually
==================================================
- Copying only the necessary project files (once minified and concatenated) from a development directory into a production-ready directory
- Deploying that production-ready directory off to a remote server to be pushed live to the public

Misc best-practice tasks that you *shouldn't* be doing manually
===============================================================
- Validating your HTML against W3 standards by going to their site and pasting your html and checking if it validates
- Optimizing your images for web use (PNG/GIF/JPEG file sizes made much smaller -- I'm looking at you Photoshop "Save for Web" abusers)

There is a better way to do *all* of the above, 100% automatically.

- What if your images could automatically be optimized for web *the second you drag them into your `/images/` folder*?
- What if your HTML could automatically be validated against W3 standards *the second you hit "save" after writing some code*?
- What if you could automatically copy all your concatenated / minified assets to a production directory, and then push it to your live server *with a single command in your terminal*?
- What if you could install a library (bootstrap, jquery, etc), have it put into your libraries directory, and automatically have its `<script>`/`<link>` tag injected into your HTML *with a single command in your terminal*?
- What if your browser could automatically reload itself without you needing to switch to it and hit refresh the second you change any JS/HTML/CSS?
- What if your LESS/SASS could be compiled and minified, and your JS concatenated and minifed, and your HTML minified automatically any time you hit "save" on those files?

Enter Grunt, Yeoman, Bower! **All of the above** is easily achievable using the GYB "workflow stack".


// TODO: finish article


-- You are doing yourself a huge disservice by not optimizing and automating the above processes - not only from a productivity standpoint, but also from a work-happiness standpoint. Once you experience the awesomeness of GYB, you won't go back, I promise you that.

--  Thats nonsense! The second you save an HTML/style file, that change should automatically appear in your browser, without the need to make a jarring switch from a "coding in my editor" mindset to a "debugging in my browser" mindset

Base-Front-end-Project
======================

A solid base layer to build new front end projects on. Includes grunt, bower, and a dozen useful grunt tasks and commands for ease of development and live reloading.

Simply follow the below instructions and you'll be up and running with Node.JS, Grunt, Bower, LESS and LiveReload.

1. Install your appropriate version of Node.JS (http://nodejs.org/download/)
2. Clone this repo (open a terminal in your coding folder and type `git clone git@github.com:Latros/Base-Front-end-Project.git`)
3. Once the repo has been cloned, still in your terminal, type "npm install"
4. (Optional) Change your version number, website address, and project name in both `package.json` and `Bower.json` in the root directory
5. Type "grunt go" in your terminal. This will bring up a grunt web server with live file watching & live reloading in your browser
6. Open up /app/assets/styles/styles.less, change `@color: red;` to `@color: blue;` and hit save -- watch your browser automatically reload to reflect the change for you!
