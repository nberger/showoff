<!SLIDE cljs bullets incremental>

# ClojureScript

<img src="../_images/cljs.png" style="width:25%" alt="cljs logo" />

* Clojure compiled to Javascript

* A LISP language

~~~SECTION:notes~~~
Who has heard about clojureScript? Who has used ClojureScript in a project?
What about clojure, who has used it already?

Clojure on JVM

Cljs everywhere: browsers, servers, cars or even toasters

List Processing. How do we delimit lists? Using parenthesis

~~~ENDSECTION~~~

<!SLIDE cljs transition=fade>

# ClojureScript

<img src="../_images/cljs.png" style="width:25%" alt="cljs logo" />

Clojure compiled to Javascript

A __LIS__t __P__rocessing language

~~~SECTION:notes~~~
A List Processing language. How do we delimit lists? Using parenthesis

Lots of parens
~~~ENDSECTION~~~

<!SLIDE[bg=fortran-lisp.jpg] lisp>


~~~SECTION:notes~~~

Created in 1958, 1 year after fortran

One of the oldest high level languages still in use today

~~~ENDSECTION~~~

<!SLIDE[bg=parens.jpg] cljs-parens>

~~~SECTION:notes~~~
Lots of parens, but other languages use them too, and also commas and semicolons, so I dunno

Let's see some ClojureScript
~~~ENDSECTION~~~

<!SLIDE cljs-js-comparison>

ClojureScript:

    @@@ clojure
    ;; define f
    (defn f [a b c]
      (g a [b c] {:fname "John"
                  :lname "Doe"}))

    ;; call f
    (f 42 "Forty" "Two")

<!SLIDE cljs-js-comparison transition=fade>

ClojureScript:

    @@@ clojure
    ;; define f
    (defn f [     ]

                                )

    ;; call f
    (f                 )


Javascript:

    @@@ javascript
    // define f
    function f(       ) {




    }

    // call f
    f(                  );

<!SLIDE cljs-js-comparison transition=fade>

ClojureScript:

    @@@ clojure
    ;; define f
    (defn f [a b c]

                                )

    ;; call f
    (f                 )


Javascript:

    @@@ javascript
    // define f
    function f(a, b, c) {




    }

    // call f
    f(                  );

<!SLIDE cljs-js-comparison transition=fade>

ClojureScript:

    @@@ clojure
    ;; define f
    (defn f [a b c]
      (g a
                               ))

    ;; call f
    (f                 )


Javascript:

    @@@ javascript
    // define f
    function f(a, b, c) {
      g(a,       ,


       );
    }

    // call f
    f(                  );

<!SLIDE cljs-js-comparison transition=fade>

ClojureScript:

    @@@ clojure
    ;; define f
    (defn f [a b c]
      (g a [b c]
                               ))

    ;; call f
    (f                 )


Javascript:

    @@@ javascript
    // define f
    function f(a, b, c) {
      g(a, [b, c],


       );
    }

    // call f
    f(                  );

<!SLIDE cljs-js-comparison transition=fade>

ClojureScript:

    @@@ clojure
    ;; define f
    (defn f [a b c]
      (g a [b c] {:fname "John"
                  :lname "Doe"}))

    ;; call f
    (f                 )


Javascript:

    @@@ javascript
    // define f
    function f(a, b, c) {
      g(a, [b, c], {
        fname: "John",
        lname: "Doe"
      });
    }

    // call f
    f(                  );

<!SLIDE cljs-js-comparison transition=fade>

ClojureScript:

    @@@ clojure
    ;; define f
    (defn f [a b c]
      (g a [b c] {:fname "John"
                  :lname "Doe"}))

    ;; call f
    (f 42 "Forty" "Two")


Javascript:

    @@@ javascript
    // define f
    function f(a, b, c) {
      g(a, [b, c], {
        fname: "John",
        lname: "Doe"
      });
    }

    // call f
    f(42, "Forty", "Two");

<!SLIDE cljs bullets incremental>

# Why ClojureScript?

It's not about syntax...

<br/>

* Immutable data structures

* Concise and expressive code

* Stable and extensible language

* Better semantics

* Google Closure Compiler (& Library)

~~~SECTION:notes~~~
Pure vs side-effectful functions

Immutable by default

No defensive copying "just in case"

Extensible: macros

Stable: Well thought language, 2 years HDD
~~~ENDSECTION~~~

<!SLIDE cljs incremental>

# Immutable data structures

* Vectors: `[1 13 42]`

* Maps: `{:name "Nico" :team "Atlanta"}`

* Also list, set, queue, etc.

~~~SECTION:notes~~~
Also list, set, and others optimized for specific use cases

No copy -> efficient and fast
~~~ENDSECTION~~~

<!SLIDE cljs>

# Immutable data structures

* Vectors: `[1 13 42]`

* Maps: `{:name "Nico" :team "Atlanta"}`

* Also list, set, queue, etc.

* Persistent: Implemented as tries. New versions share structure with old

Example:

    @@@ Clojure
    (def david {:name "David"})

    (assoc david :language "ClojureScript")
    ;; => {:name "David" :language "ClojureScript"}

~~~SECTION:notes~~~
Also list, set, and others optimized for specific use cases

No copy -> efficient and fast
~~~ENDSECTION~~~

<!SLIDE cljs>

# Concise and expressive

    @@@ Clojure
    (def people [{:name "Nico" :age 38}
                 {:name "Jakub" :age 32}])

    (-> people
        first
        (assoc :hair-color :gray)
        (update :age inc))
   ;; => {:name "Nico" :age 39 :hair-color :gray}

~~~SECTION:notes~~~
Lazy sequences allows for very expressive code

No need for lodash or underscore.js
~~~ENDSECTION~~~

<!SLIDE cljs>

# Stable and Extensible language

* Code-as-data - use same language to transform code

* Macros

* Helps to keep the language small and stable

<!SLIDE cljs macros>

# Macros

## Example: Threading macro ->>

    @@@ Clojure
    (update (assoc (first people)
                   :hair-color :gray)
            :age inc)
    ;; => {:name "Nico" :age 39 :hair-color :gray}

<!SLIDE cljs macros transition=fade>

# Macros

## Example: Threading macro ->>

    @@@ Clojure
    (-> people
        first
        (assoc :hair-color :gray)
        (update :age inc))
    ;; => {:name "Nico" :age 39 :hair-color :gray}

<!SLIDE cljs macros>

# Macros

## Example: doto

js:

    @@@ Javascript
    var myDate = (function(){
      var d = new Date();
      d.setDate(21);
      d.setMonth(10);
      d.setFullYear(2015);
      return d;
    }());

<!SLIDE cljs macros transition=fade>

# Macros

## Example: doto

cljs:

    @@@ Clojure
    (def my-date
      (let [d (new Date)]
        (.setDate d 21)
        (.setMonth d 10)
        (.setFullYear d 2015)
        d))

<!SLIDE cljs macros transition=fade>

# Macros

## Example: doto

cljs:

    @@@ Clojure
    (def my-date
      (let [d (new Date)]
        (.setDate d 21)
        (.setMonth d 10)
        (.setFullYear d 2015)
        d))

using doto:

    @@@ Clojure
    (def my-date
      (doto (new Date)
        (.setDate 21)
        (.setMonth 10)
        (.setFullYear 2015)))

<!SLIDE cljs macros>

# Macros

## Other examples

* Golang-style go-routines (CSP): core.async

* OCaml/Erlang-style pattern matching: core.match

~~~SECTION:notes~~~
CSP: Communicating Sequential Processes

Illusion of sequential code
~~~ENDSECTION~~~

<!SLIDE cljs bullets incremental>

# Better semantics

* No variable hoisting

~~~SECTION:notes~~~

Even when compiled to javascript, it solves some issues from Javascript

~~~ENDSECTION~~~

<!SLIDE cljs>

# Better semantics

No variable hoisting

js:

    @@@ Javascript
    // Variable "hoisted" to top of function scope. No warn/error
    function sayHi() {
      console.log('Hi, ' + who);
      var who = 'Pete';
    }

    sayHello();
    // Hi, undefined


cljs:

    @@@ Clojure
    (defn say-hi []
      (println "Hello, " who)
      (let [who "Pete"]))

    (say-hi)
    ;; WARN: Use of undeclared Var flying/who

<!SLIDE cljs bullets incremental>

# Better semantics

Sane equality

js:

    @@@ Javascript
    1 == "1"   // => true
    0 == false // => true
    {} == {}   // => false

cljs:

    @@@ Clojure
    (= 1 "1")   ;; => false
    (= 0 false) ;; => false
    (= {} {})   ;; => true

~~~SECTION:notes~~~
There's also strict equality ===

But how to know when to you use which one?
~~~ENDSECTION~~~

<!SLIDE cljs semantics>

# Better semantics

No operator precedence table

<img src="../_images/operator-precedence.png" style="width:45%" alt="operator-precedence-js" />

<!SLIDE cljs semantics transition=fade>

# Better semantics

No operator precedence table

js:

    @@@ Javascript
    (x > 20) && (x < 80) || (y > 100) && (y < 500)

cljs:

    @@@ Clojure
    (or (< 20 x 80) (< 100 y 500))


<!SLIDE cljs semantics transition=fade>

# Better semantics

No operator precedence table

js:

    @@@ Javascript
    ((x > 20) && (x < 80)) || ((y > 100) && (y < 500))

cljs:

    @@@ Clojure
    (or (< 20 x 80) (< 100 y 500))

<!SLIDE cljs semantics transition=fade>

# Better semantics

No operator precedence table

js:

    @@@ Javascript
    if (((x > 20) && (x < 80)) || ((y > 100) && (y < 500))) {
      console.log("yay!");
    }

cljs:

    @@@ Clojure
    (if (or (< 20 x 80) (< 100 y 500))
      (println "yay!"))
