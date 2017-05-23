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


<!SLIDE react bullets incremental>

# React.js

<img class="react-logo" src="../_images/react.png" alt="react logo" />

* A library for building composable user interfaces

* React Wrappers: Om, **Reagent**, Quiescent, Rum


<!SLIDE reagent incremental>

# Reagent

* Makes it easy to create React components

* ~~JSX~~ Hiccup

<!SLIDE reagent>

# Reagent

* Makes it easier to create React components

* ~~JSX~~ Hiccup

Example:

    @@@ clojure
    [:div {:text-align "center"}
     [:h3 "Todos"]
     [:ul#todos
      (for [todo todos]
        [:li.todo (:description todo)]]]

<!SLIDE re-frame bullets incremental>

# Re-frame

* Built on top of reagent

* State management

* Redux-like library

* Single store (atom)

* State changed via event/handler (action/reducer)

* One-way data flow: handlers -> store -> view

* Logging, time-travel, hot-reload, record & replay

<!SLIDE references>

# References

Using React.js with ClojureScript - Arne Brasseur (Lambda Island) - https://www.youtube.com/watch?v=Sbej4OYTwjg

Idée Fixe - David Nolen - GOTO 2017 - https://www.youtube.com/watch?v=lzXHMy4ewtM

Why I chose ClojureScript over JavaScript - akiroz - https://m.oursky.com/why-i-chose-clojure-over-javascript-24f045daab7e
