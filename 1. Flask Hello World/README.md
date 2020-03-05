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

Hypertext Transfer Protocol (HTTP) is the language of requests and responses that drives the Web. It consists of two main parts: requests by clients (i.e. users) and responses by webservers.

Requests allow users to ask for pages from and send information to their webserver of interest. The two main requests we'll discuss are GET requests and POST requests.

## Requests: GET and POST

GET requests are the way we usually ask a webserver for a webpage. When you navigated to this URL, your browser sent a GET request asking for this page.

POST requests allow users to send data *back* to a webserver. For example, when someone fills out a form or uploads a file, the data is usually sent via POST.

## Responses: 200, 404, 403, 418...

Once the webserver gets a request, it has to let the user know its status with that request. For example, if I asked the webserver for a page that doesn't exist, it has to let me know that the file doesn't exist -- this is a 404 response.

Every response has a different "code", or number, associated with it. Here's a table of some of the most common response codes (as well as one less common one):

| Response Code | Description                                                                   |
|:-------------:|-------------------------------------------------------------------------------|
| 200           | "OK." Everything went as expected                                             |
| 404           | The file you requested was not found                                          |
| 301           | "Redirect." The site you visited is sending you to a new URL.                 |
| 500           | "Internal server error" -- a backend error.                                   |
| 418           | ["I'm a teapot"](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#418) |

Now, we need to discuss how we can programatically receive requests and reply with responses with Flask.

***Fun Exercise:*** If you open up your developer tools (F12, or go into your browser settings) and go to the "Network" menu and browse to a website of your choice, you can see all the requests you sent and responses you received!

***Note:*** While HTTP and HTML may almost look the same, keep in mind that HTML is a way of writing webpages, while HTTP is a way of sending them.

# What is Flask?

Flask allows someone to easily set up a webserver that fulfills all of the above responsiblities with just a little bit of Python code.

