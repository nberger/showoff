<!SLIDE cljs>

# ClojureScript

~~~SECTION:notes~~~
A LISP language.

Next slide: Lots of parens
~~~ENDSECTION~~~

<img src="../_images/cljs.png" style="width:40%" alt="cljs logo" />

<!SLIDE[bg=parens.jpg] cljs-parens>

~~~SECTION:notes~~~
Lots of parens, but other languages use them too, and also commas and semicolons, so I dunno
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
      (g a [b c]                           ))

    ;; call f
    (f                 )


Javascript:

    @@@ javascript
    // define f
    function f(a, b, c) {
      g(a, [b, c],                                  );
    }

    // call f
    f(                  );

<!SLIDE cljs-js-comparison>

ClojureScript:

    @@@ clojure
    ;; define f
    (defn f [a b c]
      (g a [b c] {fname "John" lname "Doe"}))

    ;; call f
    (f                 )


Javascript:

    @@@ javascript
    // define f
    function f(a, b, c) {
      g(a, [b, c], {'fname': "John", 'lname': "Doe"});
    }

    // call f
    f(                  );

<!SLIDE cljs-js-comparison>

ClojureScript:

    @@@ clojure
    ;; define f
    (defn f [a b c]
      (g a [b c] {fname "John" lname "Doe"}))

    ;; call f
    (f 42 "Forty" "Two")


Javascript:

    @@@ javascript
    // define f
    function f(a, b, c) {
      g(a, [b, c], {'fname': "John", 'lname': "Doe"});
    }

    // call f
    f(42, "Forty", "Two");
