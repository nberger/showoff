<!SLIDE react bullets incremental>

# React.js

<img class="react-logo" src="../_images/react.png" alt="react logo" />

* A library for building composable user interfaces

* React Wrappers: Om, **Reagent**, Quiescent, Rum


<!SLIDE reagent incremental>

# Reagent

"A minimalistic ClojureScript interface to React.js"

* Create React components using (almost) just plain ClojureScript functions

* J̶S̶X̶ Hiccup

<!SLIDE reagent>

# Reagent

"A minimalistic ClojureScript interface to React.js"

* Create React components using (almost) just plain ClojureScript functions

* J̶S̶X̶ Hiccup

Example:

    @@@ clojure
    (defn todos-view [todos]
     [:div {:text-align "center"}
      [:h3 "Todos"]
      [:ul#todos
       (for [todo todos]
         [:li.todo
          (:description todo)
          [delete-todo-btn todo]]]

<!SLIDE re-frame bullets incremental>

# Re-frame

* Built on top of reagent

* Redux-like library

* Single store (atom)

* State changed via event/handler (action/reducer)

* One-way data flow: handlers -> store -> view

* Logging, time-travel, hot-reload, record & replay

<!SLIDE references>

# References/Links

ClojureScript official site - https://clojurescript.org/

Using React.js with ClojureScript - Arne Brasseur (Lambda Island) - https://www.youtube.com/watch?v=Sbej4OYTwjg

Idée Fixe - David Nolen - GOTO 2017 - https://www.youtube.com/watch?v=lzXHMy4ewtM

Developing ClojureScript With Figwheel - Bruce Hauman - https://www.youtube.com/watch?v=j-kj2qwJa_E

Why I chose ClojureScript over JavaScript - akiroz - https://m.oursky.com/why-i-chose-clojure-over-javascript-24f045daab7e
