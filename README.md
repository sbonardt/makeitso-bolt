MAKEITSO
========

MAKEITSO - get to viable at warp speed

Startup your frontend/theme development 

1. Frontend setup
2. Bolt theme starting point

MAKEITSO started out as 'flat' frontend project but now is incorporated
in a Bolt CMS (boltcms.io) theme. You can view the 'flat' example html files in the /dist/ folder

Clone the repo and view the four available HTML pages in your browser by going to
"/dist/index.html"

Or -like you should- use Bolt CMS, clone this repo in the Bolt themes folder of your project and
go to: "[projectroot]/theme/makeitso/dist/index.html"

MAKEITSO templates, available in /dist:
---------------------------------------

- index.html
- article.html
- listing.html
- form.html

Base templates are viewable in your browser after running 'npm install' and 'npm start' or,
in a Bolt installation, after cloning the theme in the themes folder: [webroot]/theme/makeitso/dist/index.html


Installing MAKEITSO theme:
-------------------------

1. Clone the repo. Preferably in the /theme folder of your Bolt 4 installation (see https://boltcms.io)
2. Go to /makeitso and run 'npm install' to install all required dev dependecies
3. See package.json for the scripts and set your localdev environment.
3. Run 'npm start'. This will build and watch the scss and js files, and set up a browsersynced environment


Technical information about the frontend in MAKEITSO:
-----------------------------------------------------

1. MAKEITSO is a stripped down startup kit. Not a frontend framework. It has some basic styling to get you started. This version
is however a bit more opinionated. Some base design cases are already filled in. The CSS selectors might help you get up and running,
so give it a shot.

2. SASS/SCSS files are compiled with NPM scripts. There is a screen.scss file in /source/scss. This references all 
required partials. You can see in the file it starts with _base.scss. The _base.scss file contains all your settings,
variables [vair-ee-uh-buh-l's], and mixins. After that _normalize.scss is imported and used. This is a copy of the version of normalize.css,
just renamed to .scss. I update it now and then.
All SASS partials are in the _modules subfolder. Some choices have been made about dividing/splitting up SCSS into several 
partials. _layout.scss should only contain layout/positioning for the scaffolding/setup of the page(s) at a high level. The
names of the other partials should give you insight into what's there to find. As a general rule, if it's styling for a block or 
other piece of content, put it in _theme.scss. If the combined amount of lines exceeds around 50 lines of code, put it in it's own partial file. (e.g. _search.scss)

3. NPM Scripts. All compiling, autoprefixing, minifying and compressing is done with NPM Scripts. No Grunt/Bower/GULP/Something

4. CSS - in package.json you'll see some scripts for compiling the scss to the main screen.css file in the '/dist/css/' folder. If, for development sake, you want a not-minified CSS file, change the compressed parameter in the 'scss:' task in package.json

5. JAVASCRIPT - in package.json you'll see some scripts for combining and minifying the javascript files into one minified scripts.js. That one is available at /dist/js/. The custom.js fiel is the main JS file for UI and interaction stuff. If you would like to add a js file (of a third party) you must specify it in the package.json file in the jsFiles variable and add the file to the /source/js/lib folder. Add the file location to the "uglifyjs" task in package.json, in the js order you would like

6. EXTRA CONTENTBLOCKS example yaml file for Bolt 4 websites - In the MAKEITSO theme 'config' subfolder you will find an example 'contenttypes.dist.yaml' file. This contains a yaml repeated node you can use in your Bolt 4 contenttypes.yaml in the main Bolt installation 'config' folder. When added this works together with the templating in the file '_contentblocks.twig' which you can find in the MAKEITSO theme subfolder 'partials'. The basic Bolt 4 templates in MAKEITSO already include this partial.


Make it so

Screenshots
-----------

Homepage

<img src="https://github.com/sbonardt/makeitso/blob/master/dist/images/theme-screenshots/01-MAKEITSO-homepage-desktop.png" width="100%">

Homepage on tablets

<img src="https://github.com/sbonardt/makeitso/blob/master/dist/images/theme-screenshots/01-MAKEITSO-homepage-tablet.png" width="480" style="max-width: 100%">

Menu mobile

<img src="https://github.com/sbonardt/makeitso/blob/master/dist/images/theme-screenshots/01-MAKEITSO-menu-mobile.png" width="480" style="max-width: 100%">

Form page

<img src="https://github.com/sbonardt/makeitso/blob/master/dist/images/theme-screenshots/02-MAKEITSO-form-desktop-1.png" width="100%">

Form page, 2

<img src="https://github.com/sbonardt/makeitso/blob/master/dist/images/theme-screenshots/02-MAKEITSO-form-desktop-2.png" width="100%">



