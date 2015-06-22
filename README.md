# Barebones Bootstrap-SASS website

Contains: 

 - Bootstrap-sass 3.3.5
 - Glyphicons (Bootstrap)
 - jQuery 1.11.3
 - Animate.css

This is supposed to be used by those of you who constantly make bootstrap-sass websites, and have to be copying files from older projects whenever you start a new one. 

## How to use

**SASS**

Don't edit the vendor/ folder, we'll use it for original files only. There's one exception though: you can comment out any @import you don't need, inside sass/vendors/_bootstrap.scss, in order to make the compiled css a little bit lighter.

Throw all your "components" inside the components/ folder.

I order to customise any bootstrap component or css style, copy its file from vendor/bootstrap to libraries/ and link it at the top of the styles.sass file.

A sample _variables.sass file is included inside libraries/, use it to customise bootstrap's variables without messing up the original files.

If you use CodeKit (https://incident57.com/codekit/), just compile styles.sass inside the css/ folder.

**Javascript**

The _scripts.php file is called at the bottom of index.php. It already calls jQuery and Bootstrap from CDNs, as well as the following functions:

    addScript(src);
    addStylesheet(src);

Use them to inject non-indispensable javascript and css files inside the setTimeout that's at the bottom, so as to improve loading times.