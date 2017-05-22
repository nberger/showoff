<!SLIDE google-closure compiler bullets incremental>

# Google Closure Compiler

* Code minification

* Dead Code Elimination (DCE)

* "Best JS to JS compiler in the world" / Idée Fixe / David Nolen

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
