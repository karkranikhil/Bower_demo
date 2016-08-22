#Introduction
Websites are made of lots of things- framework, assets, libraries, and Utilities. Bower manages all these things for you. Keeping track of all these packages and making sure they are up to date. Bower is an amazing tool that solves fundamental issues with modern web applications.
Bower is not the standard package manager for client-side JavaScript but the most popular one: currently there are more than sixteen thousand packages.
#What is Bower?
Bower is a front-end package manager built by Twitter. Also known as a Package manager for the Web. 
How Bower Works?
Bower works by fetching and installing packages from all over, taking care of hunting, finding, downloading, and saving the stuff you’re looking for.
#Why to use Bower?
*	We don’t have to download dependencies manually. Usually we go to the package website that we required finding the appropriate version, downloading it, unzipping and finally moving the main files to the vendor folder.
*	Reduce page load i.e. if multiple packages depend on a package-jQuery for example – Bower will download jQuery just once. This is known as a flat dependency graph.
*	Bower maintains a single version of modules, it only tries to help you select the correct/best one for you.
*	Declarative dependency management i.e. we declare our dependencies in bower.json so that other things can determine them easily.
* No need to commit dependencies to version control.
*	Portability i.e. you can distribute the bower.json file and everyone can get up to the speed with a simple “bower install”

###Prerequisites for Bower
* Command line tool
* Press Win+R on your keyboard Then, type cmd  or cmd.exe press Enter
* Node and NPM – Bower is a Node module so to get it we need NPM.
* Download the node installer from https://nodejs.org/en/
* Git – Bower packages are Git repos. Bower uses Git to understand where the package is, what version it’s  on.
* Download the Git from http://git-scm.org/
#Bower Installation and usage using Demo
I will demonstrate a demo which shows the steps for fetching Bootstrap and Angular files automatically using Bower and we will use Bower components in our web page.
#Step 1: Installing Bower
Install Bower as a global node module. To do this, type the following at command prompt:
```sh
 npm install –g bower
```
Note: use sudo on Mac or Linux
 
#Step 2: Creating bower.json File
Create and Initialize a bower.json file by typing the following at the command prompt:

```sh
 bower init
```
Bower will ask Several questions which you should answer as follows:

name : bower_demo

description : bower demo for kshop

main file : index.html

keywords: bower, demo, kshop, bootstrap, angular

authors: Nikhil karkra

license: MIT

say yes or press enter to the remaining questions

hompage

set currently install components as dependencies?  Yes

add commonly ignored files to ignore list ? Yes

would you like to mark this package as private which prevents it from being accidentally published to the registry?  Yes

Looks good?  Yes

 
After this command you will get your bower.json file  in your current directory .
* Now our current Directory c:\Nikhil_Karkra containing two files
 1)	Index.html
  2)	Bower.json
* Our bower.json will look like as below

```sh
{
  "name": "bower_demo",
  "authors": [
    "Nikhil karkra"
  ],
  "description": "bower demo for kshop",
  "main": "index.html",
  "keywords": [
    "bower",
    "demo",
    "kshop",
    "bootstrap",
    "angular"
  ],
  "license": "MIT",
  "homepage": "",
  "private": true,
  "ignore": [
    "**/.*",
    "node_modules",
    "bower_components",
    "test",
    "tests"
  ]
}


```
 
#Step 3: Installing Bower Components
We will first install Bootstrap using Bower. To do this type the following at the command prompt:

```sh

 bower install <package name>  -S
 bower install bootstrap  -S


```

* This will install Bootstrap to our project, and since bootstrap depends on jQuery, it will automatically install jQuery. 
* The “-S” flag indicates that Bootstrap should be saves as a dependency for our project in the bower.json file.
Next we will install angular using Bower. To do this type the following at the command prompt:
```sh

 bower install angular -S

```
 
#Step 4: Examining bower.json file
In the root folder, examine the contents of the bower.json file to see that Bower has added in new information about dependencies. This specifies that the current project is dependent on Bootstrap and angular.
 
```sh

{
  "name": "bower_demo",
  "authors": [
    "Nikhil karkra"
  ],
  "description": "bower demo for kshop",
  "main": "index.html",
  "keywords": [
    "bower",
    "demo",
    "kshop",
    "bootstrap",
    "angular"
  ],
  "license": "MIT",
  "homepage": "",
  "private": true,
  "ignore": [
    "**/.*",
    "node_modules",
    "bower_components",
    "test",
    "tests"
  ],
  "dependencies": {
    "angular": "^1.5.8",
    "bootstrap": "^3.3.7"
  }
}


```
#Step 5: Examining Bower Components
In root folder, you will find the bower_components folder that Bower created. The components that Bower fetched for you are stored in this folder. Browse the folder and the sub-folders there in to see the contents .
 
#Step 6: Using Bower Components files in web page (index.html)
We will use the CSS and JS links in our web pages to use the files in the Bower components folder. Update the CSS links in the index.html 
 
#Step 6: Final output Using Bower Components files in web page (index.html)
 ```sh
 <!DOCTYPE html>
<html lang="en">
<head>
  <title>Bower Demo</title>
<!--Bower components css files -->
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="bower_components/bootstrap/dist/css/bootstrap.min.css"  rel="stylesheet">
  <link href="bower_components/bootstrap/dist/css/bootstrap-theme.min.css"  rel="stylesheet">
</head>
<body>
<div class="container-fluid">
  <h2>Form Created Using Bower components</h2>
  <form class="col-sm-6">
    <div class="form-group">
      <label for="email">Email:</label>
      <input type="email" class="form-control" id="email" placeholder="Enter email">
    </div>
    <div class="form-group">
      <label for="pwd">Password:</label>
      <input type="password" class="form-control" id="pwd" placeholder="Enter password">
    </div>
    <div class="checkbox">
      <label><input type="checkbox"> Remember me</label>
    </div>
    <button type="submit" class="btn btn-default">Submit</button>
  </form>
</div>
<!--Bower components JS files -->
<script src="bower_components/jquery/dist/jquery.min.js"></script>
<script src="bower_components/bootstrap/dist/js/bootstrap.min.js"></script>
<script src="bower_components/angular/angular.min.js"></script>
</body>
</html>


 
 ```
#Step 7: Conclusion
In this Demo we learnt about Bower and how we can make use of Bower to fetch the web Components. Thereafter we learnt how to make use of the web components in our project. The final output having the form which is using the CSS from the Bootstrap framework added by bower
