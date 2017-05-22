<!SLIDE cljs bullets incremental>

# ClojureScript

<img src="../_images/cljs.png" style="width:25%" alt="cljs logo" />

* Clojure compiled to Javascript

* A LISP language

~~~SECTION:notes~~~
Clojure runs on the JVM

ClojureScript runs everywhere: browsers, servers, phones or even toasters

A List Processing language. How do we delimit lists? Using parenthesis

Next slide: Lots of parens
~~~ENDSECTION~~~

<!SLIDE[transition=fade] cljs>

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
      (g a [b c] {fname "John" lname "Doe"}))

    ;; call f
    (f 42 "Forty" "Two")

<!SLIDE cljs-js-comparison>

ClojureScript:

    @@@ clojure

    (defn f [     ]
                                            )


    (f                 )


Javascript:

    @@@ javascript

    function f(       ) {

    }


    f(                  );

<!SLIDE cljs-js-comparison>

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

<!SLIDE cljs-js-comparison>

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

<!SLIDE cljs-js-comparison>

ClojureScript:

    @@@ clojure
    ;; define f
    (defn f [a b c]
      (g a                                 ))

    ;; call f
    (f                 )


Javascript:

    @@@ javascript
    // define f
    function f(a, b, c) {
      g(a,       ,                                  );
    }

    // call f
    f(                  );

<!SLIDE cljs-js-comparison>

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

<!SLIDE cljs-js-comparison>

ClojureScript:

    @@@ clojure
    ;; define f
    (defn f [a b c]
      (g a [b c] {fname "John"
                  lname "Doe"}))

    ;; call f
    (f                 )


Javascript:

    @@@ javascript
    // define f
    function f(a, b, c) {
      g(a, [b, c], {
        'fname': "John",
        'lname': "Doe"
      });
    }

    // call f
    f(                  );

<!SLIDE cljs-js-comparison>

ClojureScript:

    @@@ clojure
    ;; define f
    (defn f [a b c]
      (g a [b c] {fname "John"
                  lname "Doe"}))

    ;; call f
    (f 42 "Forty" "Two")


Javascript:

    @@@ javascript
    // define f
    function f(a, b, c) {
      g(a, [b, c], {
        'fname': "John",
        'lname': "Doe"
      });
    }

    // call f
    f(42, "Forty", "Two");

<!SLIDE cljs bullets incremental>

# ClojureScript

* Immutable (persistent) data structures

* Concise and expressive

* Stable and extensible language

* Good semantics

* Google Closure

~~~SECTION:notes~~~
Functions as 1st class citizens

Pure functions

The fewer side-effects the better

Immutable by default

Extensible: core.async as library



Next slide: Lots of parens
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


<!SLIDE cljs>

# ClojureScript

## Concise and expressive

Add code example HERE, maybe a data transformation pipeline

<!SLIDE cljs bullets incremental>

# ClojureScript

## Extensible language

* Macros

* Example: core.async. Go-style blocks (CSP) 

~~~SECTION:notes~~~
CSP: Communicating Sequential Processes

Illusion of sequential code

More than async/await: Coordinate complex async operations




