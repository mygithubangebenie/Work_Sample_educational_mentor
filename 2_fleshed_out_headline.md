# Objectives of This Courses
The aim of this courses is to Learn and Understand how HTML,Css,Js,Ruby,Ruby algorthm
and Git/Github then it will help you to enlarge your knowledge and skills in Software development after this course student will be able to use all of this and has experience of using Github.

# HTML
# Html Overview
HTML stands for Hypertext Markup Language, and it is the most widely used language to write Web Pages. As its name suggests, HTML is a Markup Language which means you use HTML to simply "mark-up" a text document with tags that tell a Web browser how to structure it to display.
In this article we cover the absolute basics of HTML. To get you started, this article defines elements, attributes, and all the other important terms you may have heard. It also explains where these fit into HTML.
# what is it in head,Meta data in HTML
The HTML head is the contents of the <head> element — unlike the contents of the <body> element (which are displayed on the page when loaded in a browser), the head's content is not displayed on the page. Instead, the head's job is to contain metadata about the document. In the above example, the head is quite small:
<head>
  <meta charset="utf-8">
  <title>My test page</title>
</head>

# Html text fundamentals
What are the fundamentals of HTML?
HTML Fundamentals
Structure of HTML Documents and HTML Document Tags.
 The first thing in your HTML document is a <! ...
HTML Syntax (elements) Each HTML tag consists of an opening and a closing , that is, <name> ..
Document Structure Tags.
List Tags.etc ..
# Creating hyperlinks
Hyperlinks are really important — they are what makes the Web a web
Hyperlinks are one of the most exciting innovations the Web has to offer. 
here there is example of hyperlink
<p>I'm creating a link to
<a href="https:www.diveintocode.jp">the homepage</a>.
</p>

# Advanced text formatting
The purpose of these formatting is to mark up a set of items and their associated descriptions
# Document and website structure
Starting a website is much easier and cheaper than it used to be thanks to the wide variety of user-friendly.

Basic sections of a document
Webpages can and will look pretty different from one another, but they all tend to share similar standard components, unless the page is displaying a fullscreen video or game, is part of some kind of art project, or is just badly structured:

Header: Usually a big strip across the top with a big heading, logo, and perhaps a tagline. This usually stays the same from one webpage to another.

navigation bar:this content usually remains consistent from one webpage to another — having inconsistent navigation on your website will just lead to confused

main content:A big area in the center that contains most of the unique content of a given webpage

sidebar :Some peripheral info, links, quotes, ads, etc. Usually, this is contextual to what is contained in the main content 

footer:A strip across the bottom of the page that generally contains fine print, copyright notices, or contact info. It's a place to put common information
# Debugging Html
Writing HTML is fine, but what if something goes wrong, and you can't work out where the error in the code is? This article will introduce you to some tools that can help you find and fix errors in HTML.
The Nu HTML5 is a popular HTML 5 Validator Online tool. Nu HTML5 helps to scan the complete application and find out all the syntax errors in the application.
# Assessment
This assessment tests your ability to use HTML to structure a simple page of content, containing a header, a footer, a navigation menu, main content, and a sidebar.
------------------------------------------------------------------------------------------------
# CSS
# What is Css?
CSS stands for Cascading Style Sheets
CSS describes how HTML elements are to be displayed on screen, paper, or in other media.
# Getting started with Css
Adding Css to our document
The very first thing we need to do is to tell the HTML document that we have some CSS rules we want it to use.There are three different ways to apply CSS to an HTML document 

- Create a file in the same folder as your HTML document and save it as styles.css. The .css extension shows that this is a CSS file.
- To link styles.css to index.html add the following line somewhere inside the <head> of the HTML document:
<link rel="stylesheet" href="styles.css">

# How css is structured
First, let's examine three methods of applying CSS to a document: with an external stylesheet, with an internal stylesheet, and with inline styles.

- External style sheet
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>

- Internal style sheet
An internal stylesheet resides within an HTML document. To create an internal stylesheet, you place CSS inside a <style> element contained inside the HTML <head>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
    <style>
      h1 {
        color: blue;
        background-color: yellow;
        border: 1px solid black;
      }

      p {
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>

- Inline style sheet
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
  </head>
  <body>
    <h1 style="color: blue;background-color: yellow;border: 1px solid black;">Hello World!</h1>
    <p style="color:red;">This is my first CSS example</p>
  </body>
</html>

# How Css works?
How does CSS actually work?
When a browser displays a document, it must combine the document's content with its style information. 
# Css building block
here there is css selector!
CSS selectors
There are a wide variety of CSS selectors available, allowing for fine-grained precision when selecting elements to style. In this article and its sub-articles, we'll run through the different types in great detail, seeing how they work. The sub-articles are as follows:
- Type, class, and ID selectors
- Attribute selectors
- Pseudo-classes and pseudo-elements
- Combinators
What is a selector?
You have met selectors already. A CSS selector is the first part of a CSS Rule.

h1 { 
  color: blue; 
} 

.special { 
  color: blue; 
} 
# Styling text
The CSS text-align property defines the horizontal text alignment for an HTML element:
<h1 style="text-align:center;">Centered Heading</h1>
<p style="text-align:center;">Centered paragraph.</p>

# Css Layout
a collection of popular layouts and patterns made with CSS
So that I collect most popular layouts and patterns that can be built with pure CSS.
They are powered by modern CSS features such as flexbox and CSS grid.

# Assessment
What does CSS stand for?


---------------------------------------------------------------------------------
# JS

# what is Javascript?
JavaScript is a text-based programming language used both on the client-side and server-side that allows you to make web pages interactive. Where HTML and CSS are languages that give structure and style to web pages, JavaScript gives web pages interactive elements that engage a user.

# Basic math in Javascript,Numbers and operators
JavaScript Math Object
Math.round() Math.round(x) returns the value of x rounded to its nearest integer: 
Math.pow() Math.pow(x, y) returns the value of x to the power of y:
Math.sqrt() Math.sqrt(x) returns the square root of x: 
There are four different types of calculation operators: arithmetic, comparison, text concatenation, and reference.
What is () called in math?
- This symbol is called an asterisk. In mathematics, we sometimes use it to mean multiplication, particularly with computers. For example, 5*3 = 5 times 3 = 15.

# Handling text and string in Javascript
Strings are dealt with similarly to numbers at first glance, but when you dig deeper you'll start to see some notable differences
- Creating a string
To start with, enter the following lines:
let string = 'The revolution will not be televised.';
string;
- If you don't do this, or miss one of the quotes, you'll get an error. Try entering the following lines:
let badString = This is a test;
let badString = 'This is a test;
let badString = This is a test';
# Useful string method

Strings as objects
Most things are objects in JavaScript. When you create a string, for example by using:
let string = 'This is my string';
Finding the length of a string
This is easy — you simply use the length property. Try entering the following lines:
let browserType = 'mozilla';
browserType.length;

# Array
JavaScript arrays are used to store multiple values in a single variable.
Example
var cars = ["Saab", "Volvo", "BMW"];

# What is an Array?
An array is a special variable, which can hold more than one value at a time.
If you have a list of items (a list of car names, for example), storing the cars in single variables could look like this:
var car1 = "Saab";
var car2 = "Volvo";
var car3 = "BMW";

# JavaScript Array Methods
Converting Arrays to Strings
The JavaScript method toString() converts an array to a string of (comma separated) array values.

Example
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();
Result:
Banana,Orange,Apple,Mango

# Introducing Javascript Object
What is JavaScript Object Notation (JSON) and how can you put it to work? This concise guide helps busy IT professionals get up and running quickly with this popular data interchange format, and provides a deep understanding of how JSON works. 

# How do you declare an object in JavaScript?

Creating a JavaScript Object
There are different ways to create new objects: Define and create a single object, using an object literal. Define and create a single object, with the keyword new . Define an object constructor, and then create objects of the constructed type.

# Asynchrounous Javascript

Why study Asynchronous JavaScript?
Asynchronous JavaScript can be tricky even for experienced developers, but it’s part of what makes JavaScript such a powerful and efficient programming language.
# What is synchronous and asynchronous in JavaScript?

synchronous code is executed in sequence – each statement waits for the previous statement to finish before executing. Asynchronous code doesn't have to wait – your program can continue to run. You do this to keep your site or app responsive, reducing waiting time for the user.

# Assessment

------------------------------------------------------------------------------------------------
# Ruby
# Ruby Language Overview

Ruby is a general-purpose, interpreted programming language. Ruby is a true object-oriented programming language. Ruby is a server-side scripting language similar to Python and PERL. Ruby can be used to write Common Gateway Interface (CGI) scripts.
Dynamically typed
Interpreted
Can be modified at runtime
Object oriented
Blocks / lambdas / closures
Perl-like regular expressions
Closely tied to shell & OS
# Features of Ruby

Ruby is an open-source and is freely available on the Web, but it is subject to a license.
Ruby is a general-purpose, interpreted programming language.
Ruby is a true object-oriented programming language.
# Built-in Types
Numbers
42
Booleans
true
false
Strings
"apple"
'banana'
Symbols
:apple
Arrays
["apple", "banana"]
# Functions And loops

 while loop is a control flow statement that allows code to be executed repeatedly based on a given Boolean condition. 
Example:

filter_none
brightness_4
# Ruby program to illustrate 'while' loop 
  
# variable x 
x = 4
  
# using while loop  
# here condtional is x i.e. 4 
while x >= 1 
  
# statements to be executed 
  puts "GeeksforGeeks"
  x = x - 1
    
# while loop ends here 
end

# Classes and methods
a method provides functionality to an Object. A class method provides functionality to a class itself, while an instance method provides functionality to one instance of a class.

class Calculator
  def add(a,b)
    a + b
  end
end
# How Ruby Works with Databases
Using GEM files (Ruby Libraries)•Supported: MySQL, Oracle, Neo4J, DB2, SQLite, ODBC.
# Rails Architecture (Based on MVC)
MVC is a pattern for the architecture of a software application. It separates an application into the following components:
- Models for handling data and business logic
- Controllers for handling the user interface and application
- Views for handling graphical user interface objects and presentation
# How to install Ruby?
apt (Debian or Ubuntu)
Debian GNU/Linux and Ubuntu use the apt package manager. You can use it like this:

- sudo apt-get install ruby-full
- sudo yum install ruby
- sudo snap install ruby --classic
- sudo snap switch ruby --channel=2.3/stable
- sudo snap refresh

# Creating a project in ruby
Creating a New Rails Project. 
- Scaffolding the Application.
- Creating the Application Root View and Testing Functionality.
- Adding Validations.
- Adding Authentication.
- Create database
- Migrate database
- Starting server
-------------------------------------------------------------------------
# Ruby Algorthm

# Ruby Algorthm meaning and Understanding Flowchart
HOW TO USE IT?
- Process Flowchart is one of the most basic diagram you will meet. It is a great one to begin with since it is used to describe a high-level process of the whole system.
- Ruby Algorthm : An algorithm is a step by step procedure to solve logical and mathematical problems. A recipe is a good example of an algorithm because it says what must be done, step by step.
# Meaning of pseudocode and steps of using it in algorthm

It is a simpler version of a programming code in plain English which uses short phrases to write code for a program before it is implemented in a specific programming language.
# understanding and implementing bubble sort in ruby 

Bubble sort, sometimes referred to as sinking sort, is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements and swaps them if they are in the wrong order. 

def bubble_sort(array)
  array_length = array.size
  return array if array_length <= 1

  loop do
    # we need to create a variable that will be checked so that we don't run into an infinite loop scenario.
    swapped = false

    # subtract one because Ruby arrays are zero-index based
    (array_length-1).times do |i|
      if array[i] > array[i+1]
        array[i], array[i+1] = array[i+1], array[i]
        swapped = true
      end
    end

    break if not swapped
  end

  array
end

unsorted_array = [11,5,7,6,15]
p bubble_sort(unsorted_array)
Running ruby ruby-sorting.rb in the terminal produces the following:

[5, 6, 7, 11, 15]
# Error handling in algorthm

Error handling refers to the response and recovery procedures from error conditions present in a software application. In other words, it is the process comprised of anticipation, detection and resolution of application errors, programming errors or communication errors.
There are four main categories of errors:

Logical errors
Generated errors
Compile-time errors
Runtime errors
-----------------------------------------------------------------------------------
# Git/Github

# Purpose of Using Git
GitHub is a Git repository hosting service, but it adds many of its own features. While Git is a command line tool, GitHub provides a Web-based graphical interface. It also provides access control and several collaboration features, such as a wikis and basic task management tools for every project.

# What Is Git? and What Is GitHub?
Git is a version control system that lets you manage and keep track of your source code history. GitHub is a cloud-based hosting service that lets you manage Git repositories. 
# Installation of Git
Debian/Ubuntu
- Git packages are available using apt.
- It's a good idea to make sure you're running the latest version. To do so, Navigate to your command prompt shell and run the following command to make sure everything is up-to-date: sudo apt-get update.
- To install Git, run the following command: sudo apt-get install git-all.
- Once the command output has completed, you can verify the installation by typing: git version.
# Configuration of Git
As you read briefly in Getting Started, you can specify Git configuration settings with the git config command. One of the first things you did was set up your name and email address:
- git init
- git add .
- git config --global user.name "Ange benie"
- git config --global user.email angebenie@example.com
etc...
# Github
What is GitHub? GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere. This tutorial teaches you GitHub essentials like repositories, branches, commits, and Pull
# How To Get Started With GitHub
- Signup with github
- then Sign in

