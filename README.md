Compass Tutorial
================

Instalation
-----------
1. Install [Ruby](http://www.ruby-lang.org/en/downloads/)
2. `sudo gem install compass`

Starting from scratch
---------------------
1. `git clone https://github.com/jethrolarson/sass-tutorial.git`
2. `cd sass-tutorial`
3. `compass create`

Config.rb
----------
* Directory config
* Output style

Looking at the Output
---------------------
* @import
* Finding source from compiled output
* Remove the reset

Editing
---------
Brief on sass vs. scss: The SASS syntax is a more terse, which I prefer, but can be harder to learn so this tutorial will focus on the more css-like scss syntax. There's no difference in functionality though so it's just personal preference.

1. `compass watch`
   This start a process that watches your sass directory for changes and automatically recompiles to the stylesheets directory.
2. `mate .`
3. open index.html
   update css reference to screen.css
4. _base.scss
   All files prefixed with `_` will not generate a .css counterpart, so they're good for libraries. 
5. update screen.scss

Since the stylesheets are compiled you don't have to use fewer files to cut down on HTTP requests. So you can organize your source in whatever way makes the most sense. There are some best practices for doing so, but I think that's another discussion.

Let's start with some [existing css](old.css) and clean it up some.
`cp old.css sass/_new.scss`

* Simplify this [CSS3][css3-docs] crap:  
  _base.scss: `@import "compass/css3";`

* DRY the colors with some variables
* Use Color functions to make changing colors easier

* Use variables to standardize the margins.
* Use expressions to get more out of your variables

* Use nesting to calm the chaos.
* Use & to make nesting easier

* Normally CSS3 Gradients are a pain, but compass makes it so easy we'll add one for fun.  
  `@include background-image(linear-gradient(top, white, #aaa));}`

* Define your own mixins for common problems

More Info
--------------
* [Compass Tutorials](http://compass-style.org/help/tutorials/)
* [Official Best Practices](compass-practices)

---

[css3-docs]: http://compass-style.org/reference/compass/css3/
[compass-practices]: http://compass-style.org/help/tutorials/best_practices/