# Intro to Webservers and Flask
## Overview

### What You'll Learn
In this section, you'll learn
1. What webservers do and how
2. How to set up a Flask webserver in Python

### Prerequisites
Before starting this section, you should have 
1. Python and Flask installed on your computer, explained [here](https://github.com/ajstensland/flask-tutorial/blob/hackbu-webdev/README.md#before-we-start)
1. An understanding of [Introductory Python](https://github.com/HackBinghamton/PythonWorkshop)

### Introduction
In this section, we'll discuss how to host webpages with Flask and give you enough background on HTTP(S) to make you comfortable with the next two sections.

---

# What Do Webservers... Do?

Right now, you're viewing the GitHub website. In order for you to view this website, a few things had to happen:

1. Your browser sent out an HTTP "GET request" to GitHub
1. A webserver at GitHub received your HTTP request
1. The webserver sent you the correspoding HTML/CSS/JS to display this page

Webservers have the following responsibilities:

1. Store web pages (e.g. HTML/CSS/JS)
1. Listen for user requests (e.g. "Send me your index.html" or "Here's my survey results, store them, please")
1. Act on those requests appropriately
1. Respond to users with updated content

How does this all happen? We could discuss things such as the [OSI model](https://www.lifewire.com/layers-of-the-osi-model-illustrated-818017) and [socket programming](https://docs.python.org/3/howto/sockets.html), but thankfully Flask abstracts most of this away for you.

We will, however, have to discuss some HTTP concepts before diving in.

# What is HTTP?

To be  continued...

# What is Flask?

Flask allows someone to easily set up a webserver that fulfills all of the above responsiblities with just a little bit of Python code.

