# flask-tutorial
A tutorial about Flask for HackBU










If you want to make your new website look a bit more exciting, you can always grab a template from html5up: https://html5up.net/.

Once you've downloaded and extracted a zip file for the template that you like, move the index.html file into the templates folder of your project.

Back in the extracted template directory, go into the assets folder and move the fonts folder into the static folder of your project. Then, move just the contents (folders and all) from the css and sass folders into the static folder as well.

Because of some differences in how Flask handles html and css files, you'll need to change a few things before your template will work.

First, open up the index.html that you just moved into your templates folder. Anywhere that you see:

```html
"rel="stylesheet" href="assets/css/..."

replace it with:

"rel="stylesheet" href="{{ url_for('static', filename='...') }}"
```
