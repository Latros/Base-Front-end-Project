Base-Front-end-Project
======================

A solid base layer to build new front end projects on. Includes grunt, bower, and a dozen useful grunt tasks and commands for ease of development and live reloading.

Simply follow the below instructions and you'll be up and running with Node.JS, Grunt, Bower, LESS and LiveReload.

1. Install your appropriate version of Node.JS (http://nodejs.org/download/)
2. Clone this repo (open a terminal in your coding folder and type `git clone git@github.com:Latros/Base-Front-end-Project.git`)
3. Once the repo has been cloned, type "npm install"
4. (Optional) Change your version number, website address, and project name in both `package.json` and `Bower.json` in the root directory
5. Type "grunt go" in your terminal. This will bring up a grunt web server with live file watching & live reloading in your browser
6. Open up /app/assets/styles/styles.less, change `@color: red;` to `@color: blue;` and hit save -- watch your browser automatically reload to reflect the change for you!
