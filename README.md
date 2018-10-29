# flask-tutorial
A tutorial about Flask for HackBU

Before we get started, make sure that you have Python 3 and Flask installed.

The latest version of Python 3 for your OS can be found at https://www.python.org/downloads/.

Once Python is installed, open the command prompt and run 'pip install Flask'.










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

If all of your files are in the correct place, this should run your website with
