<!SLIDE cljs bullets incremental>

# ClojureScript

<img src="../_images/cljs.png" style="width:25%" alt="cljs logo" />

* Clojure compiled to Javascript

* A LISP language

~~~SECTION:notes~~~
Clojure on JVM

Cljs everywhere: browsers, servers, phones or even toasters

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

* Immutable (persistent) data structures

* Concise and expressive

* Stable and extensible language

* Better semantics

* Google Closure

~~~SECTION:notes~~~
It's not about the syntax

Functions as 1st class citizens

Pure functions

The fewer side-effects the better

Immutable by default

Extensible: macros
~~~ENDSECTION~~~

<!SLIDE cljs>

# ClojureScript

## Immutable Persistent data structures

* Vectors: [1 13 42]

* Maps: {:name "Nico" :team "Atlanta"}


* Persistent: Tree structure. New versions share structure with old versions

    @@@ Clojure
    (def david {:name "David"})

    (assoc david :language "ClojureScript")
    ;; {:name "David" :language "ClojureScript"}

~~~SECTION:notes~~~
Also list, set, and others optimized for specific use cases

No copy -> efficient and fast
~~~ENDSECTION~~~


<!SLIDE cljs>

# ClojureScript

## Concise and expressive

    @@@ Clojure
    (->> (range)
         (map #(* % %))
         (filter even?)
         (map inc)
         (take 3))
    ;; (1 5 17)

~~~SECTION:notes~~~
Lazy sequences allows for very expressive code

No need for lodash or underscore.js
~~~ENDSECTION~~~

<!SLIDE cljs>

# ClojureScript

## Extensible language

* Macros

* Helps to keep the language small

* Code-as-data - use same language to transform code

<!SLIDE cljs macros>

# Macros

## Example: Threading macro ->>

    @@@ Clojure
    (take 3
          (map inc
               (filter even?
                       (map #(* % %)
                            (range)))))
    ;; (1 5 17)

<!SLIDE cljs macros transition=fade>

# Macros

## Example: Threading macro ->>

    @@@ Clojure
    (->> (range)
         (map #(* % %))
         (filter even?)
         (map inc)
         (take 3))
    ;; (1 5 17)

<!SLIDE cljs macros>

# Macros

## Example: doto

    @@@ Javascript
    var myDate = (function(){
      var d = new Date();
      d.setDate(21);
      d.setMonth(10);
      d.setFullYear(2015);
      return d;
    }());

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

    @@@ Javascript
    var myDate = (function(){
      var d = new Date();
      d.setDate(21);
      d.setMonth(10);
      d.setFullYear(2015);
      return d;
    }());

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

<!SLIDE cljs>

# Better semantics

No variable hoisting

    @@@ Javascript
    // Variable "hoisted" to the top of the scope in JS. No warn/error
    function sayHi() {
      console.log('Hi, ' + who);
      var who = 'Pete';
    }

    sayHello();
    // Hi, undefined


    @@@ Clojure
    (defn say-hi []
      (println "Hello, " who)
      (let [who "Pete"]))

    (say-hi)
    ;; Use of undeclared Var flying/who

<!SLIDE cljs bullets incremental>

# Better semantics

Sane equality
