<!SLIDE google-closure compiler bullets incremental>

# Google Closure Compiler

* "tool for making JavaScript download and run faster"

* Dead Code Elimination (DCE)

* Minification, inlining and more

* "Best JS-to-JS optimizing compiler in the world"

~~~SECTION:notes~~~
ClojureScript outputs js optimized for Google Closure

"The best way to use Google Closure"
~~~ENDSECTION~~~

<!SLIDE google-closure library bullets incremental>

# Google Closure Library

* Depedency management (goog.require & goog.provide)

* Takes care of browser inconsistencies

<!SLIDE closure library bullets>

# Google Closure Library

* Functions for... a lot of different things

* goog.date
* goog.dom
* goog.events
* goog.json
* goog.math
* goog.net
* goog.object
* goog.string
* goog.ui
* goog.uri
* goog.window

<!SLIDE google-closure library>

<!SLIDE react bullets incremental>

# React.js


* A javascript library for building user interfaces

* React Wrappers: Om, Reagent, Quiescent, Rum

<img class="react-logo" src="../_images/react.png" alt="react logo" />

<!SLIDE reagent incremental>

# Reagent

* Thin React wrapper

* Makes it easy to create components

* Most components are created using cljs data structures

    @@@ clojure
    [:div
     [:p "This is some "
      [:strong "text"]]
     [:ul
      [:li {:style {:margin-right "10px"}} "A list item"]
      [:li "Another list item"]]]

<!SLIDE re-frame bullets incremental>

# Re-frame

* Redux-like library

* Built on top of reagent

<!SLIDE references>

# References

Using React.js with ClojureScript - Arne Brasseur (Lambda Island) - https://www.youtube.com/watch?v=Sbej4OYTwjg

Idée Fixe - David Nolen - GOTO 2017 - https://www.youtube.com/watch?v=lzXHMy4ewtM

Why I chose ClojureScript over JavaScript - akiroz - https://m.oursky.com/why-i-chose-clojure-over-javascript-24f045daab7e
