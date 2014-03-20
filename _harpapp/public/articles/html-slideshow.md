HTML slideshow systems
=====================

*An overview of the most popular open source HTML slideshow systems*


Benefits:

- Can easily embed audio and video with HTML5
- Easy to switch to browser (for example a code demo) for presentation
- Can be more freeform, doesn't have to follow a sequential chronology 
- Can work with only a browser
- If you host it online, you never have to keep track of a file
- Can edit with just a text editor
- The entire Web is accessible from the presentation
- Another plus is if your presentation is really good and you use it as content marketing, it's hosted right on your website rather than being on SlideShare and you can link inside the presentation 


Features I look for:

- Viewable on mobile
- Markdown support would be ideal
- Can be printed to PDFs
* Can link to a specific slide using fragment identifier (I think this is universally a yes)
* Auto-play
* Table of contents (mostly if I want others to look at it later)




###deck.js
Slides are HTML
deck.core module keeps track of slide states and deck states
CSS defines what each state looks like and how to transition
Extensions use core events and modules to add anything you want (for example, a visual navigation UI at bottom with deck.navigation, or a deck.status which shows where you are in the deck)

You can link to fragments within a slide
Cool fancy transitions
You can use premade templates to make slides immediately, or make custom decks with the API exposed by the core and extensions

Depends on jQuery and Modernizr

-Viewable on mobile NO (not exactly optimized)
-Markdown support would be ideal
-Can be printed to PDFs

Can look great if you know what you're doing; otherwise can be simple

http://imakewebthings.com/deck.js/


###jmpress.js
jQuery port of Impress.js
Basically adds more features with plugin interface and is less of a tech demo
Can use templates where you set attributes of your element with JavaScript (this way x and y and scale data are in the HTML file but are defined in the JavaScript)
Can be used embedded on pages or within another jmpress
Can be timed, yes

-Viewable on mobile 
-Markdown support would be ideal
-Can be printed to PDFs YES

Good perhaps better for implementing a fancy design, not for just throwing together a quick presentation

http://jmpressjs.github.io/jmpress.js


###Impress.js
Open Prezi-like canvas, with transforms and transitions using CSS3
Doesn't really work in older browsers, forget IE9 and back

-Viewable on mobile NOPE/can work on some tablets but not optimized
-Markdown support would be ideal
-Can be printed to PDFs

No reason to really choose above jmpress.js

https://github.com/bartaz/impress.js


###Reveal.js
Most common one
Nested slides (necessary though?)
Slides can be written in HTML or Markdown
CSS 3D transforms
Javascript API
PDF export

-Viewable on mobile YES (but not that great)
-Markdown support would be ideal YES
-Can be printed to PDFs YES 

Most likely to use, just nicely designed and quick to use

http://lab.hakim.se/reveal-js


###Google HTML5 slides

-Viewable on mobile YES
-Markdown support would be ideal YES
-Can be printed to PDFs  

More advanced features than I need, clean but not fancy visually
Nice features if I'm actually making a company presentation

https://code.google.com/p/io-2012-slides/


###Landslide
Generates Google HTML5 slides from Markdown using Python program
Really cool if I want to set it up for regular use

https://github.com/adamzap/landslide


###Shwr.me
Good-looking theme if a bit more static-looking than other systems

-Viewable on mobile NO
-Markdown support would be ideal NO
-Can be printed to PDFs YES 

Very simple and pleasant

https://github.com/shower/shower/


###Bespoke.js
Beautiful and cute
Super minimal and DIY with plugin system

http://markdalgleish.com/projects/bespoke.js/


###FerroSlider
jQuery plugin, quite flexible in terms of making a slider usable fullscreen
"jQuery plugin that allows you to organize the contents of websites in a unusual and cool way"

Can be used to develop some cool, if not super easy-to-use sites

http://www.alessandroferrini.it/lab/jQueryPlugins/ferroSlider/docs/

---

A startup http://www.slidecaptain.com/
