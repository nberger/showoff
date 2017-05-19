<!SLIDE[bg=BirdFlyingUshuaia.jpg] title>

~~~SECTION:notes~~~
Flying is about going fast and safe.

Write code that runs fast in the browser, with less bugs. And write it fast with a small team

Help airlines give a better customer service to their passengers who are... flying
~~~ENDSECTION~~~

# Flying with ClojureScript and React

## Travel Tech Con 2017

Nicolás Berger
/
[fa-github-alt]
nberger

<img src="../_images/roomstorm.png" height="24" style="margin:0;display:inline" alt="roomstorm logo" />
Roomstorm

<!SLIDE agenda bullets incremental>

# Agenda

* ClojureScript
* Google Closure
* React
* Reagent & Re-frame
* Interactive development
  * REPL
  * Live Reload
  * Devcards

<!SLIDE cljs>

# ClojureScript

~~~SECTION:notes~~~
A LISP language.

Lots of parens, but other languages too, and also commas and semicolons
~~~ENDSECTION~~~

<img src="../_images/cljs.png" style="width:60%" alt="cljs logo" />

@@@ Clojure
(let [coll [1 3 5 7]]


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

<!SLIDE reagent re-frame>

<!SLIDE references>

Using React.js with ClojureScript - Arne Brasseur (Lambda Island) - https://www.youtube.com/watch?v=Sbej4OYTwjg

Idée Fixe - David Nolen - GOTO 2017 - https://www.youtube.com/watch?v=lzXHMy4ewtM

Why I chose ClojureScript over JavaScript - akiroz - https://m.oursky.com/why-i-chose-clojure-over-javascript-24f045daab7e

<!SLIDE[bg=Sunset.jpg] thanks>
# Thanks!

[fa-github-alt]
nberger
/
[fa-twitter]
nicoberger

.photos-credit All photos by myself

<!SLIDE just-words>
Foreword: explain title, introduce myself and roomstorm - 1min
what's clojurescript: Who has heard about clojureScript? Who has used ClojureScript in a project?
What's React: I guess almost everyone heard about React. Who uses React in their projects?
Key things about Cljs: Immutable data structures, pure functions, data-oriented programming, extensible language, better semantics than js (equality
