# flask-tutorial
A tutorial about Flask for HackBU
## Before We Start
Make sure that you have Python 3 and Flask installed.

The latest version of Python 3 for your OS can be found at https://www.python.org/downloads/.
If using Linux of some variety, try to install it through your package manager (e.g. apt-get, pacman, etc.) before downloading from the website.

Once Python is installed, open the command prompt and run 'pip install Flask'.

You should be good to go!

## 1. Raw Basics
Import Flask from flask -- this will let you run Flask!

Then, use function decorators to tell flask how to route your page.

What your function returns 

## 2. Making It Pretty

## 3. Taking Input and Output: Zalgo Text Generator

## 4. Converting HTML5UP Templates Into Flask-Ready Format
If you want to make your new website look a bit more exciting, you can always grab a template from html5up: https://html5up.net/.

Once you've downloaded and extracted a zip file for the template that you like, move the index.html file into the templates folder of your project. Then rename your old index.html to something else (like index2.html or something along those lines).

Back in the extracted template directory, go into the assets folder and move the fonts folder into the static folder of your project. Then, move just the contents (folders and all) from the css and sass folders into the static folder as well.

Because of some differences in how Flask handles html and css files, you'll need to change a few things before your template will work.

Start by opening up the index.html that you just moved into your templates folder.

Anywhere that you see:

```html
"rel="stylesheet" href="assets/css/..."
```

replace it with:

```html
"rel="stylesheet" href="{{ url_for('static', filename='...') }}"
```

If all of your files are in the correct place, this should run your website with the new template.

All you'll have to do now is edit the new index.html file with your own information.

If you're feeling ambitious, you can also copy the html from index into the other pages that we made in this demo. You'll also need to add links that connect all of the pages. If you need any help with this, feel free to ask any of the organizers.
