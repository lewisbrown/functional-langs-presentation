functional programming

 


why functional?

will make you think differently about programming
will make you a better programmer
will improve your productivity


what is functional programming?

SQL - an expression involving projections, selections, joins, etc.
query says what relation should be computed, without saying how it should be computed
query can be evaluated in any convenient order as determined by optimizer


what is functional programming?

Spreadsheet - you say what you want done
app figures out how it should be evaluated


functional features

everything is an expression
everything is first class
  higher order functions
closures
currying
immutable types
  no side effects
referential transparency
algebraic datatypes
pattern matching/destructuring
macros
recursion & tail calls
reflexivity
garbage collection


everything is an expression

everything is an expression
expressions return values


everything is an expression

imperative program: is a sequence of commands which are executed strictly one after the other
functional program: is a single expression, which is executed by evaluating the expression, using one of a number of different evaluation orders


everything is an expression


lambda returns a function

      (let-values (((struct:a make-a a? a-ref a-set!) (make-struct-type 'a #f 2 1))
         (display make-a)
      #<procedure:make-a>

      make-struct returns a type, a constructor, and getter & setter functions


everything is an expression


everything is an expression


everything is first class

functions, types, structs, classes, regular expressions, macros
first class objects are available at run-time, not just compile time
first class objects can be passed to functions and returned from functions


functions are first class


functions are first class


functions are first class


higher order functions

functions that take or return functions
very powerful constructs


higher order functions


higher order functions


higher order functions


higher order functions


higher order functions


closures

objects are state data with attached behavior
closures are behavior with attached state


closures now common


currying


immutable types

new data structures are appended or created as needed
no side effects
this can be an efficiency issue


no side effects

side effect = an observable modification of state or environment

    setting a non-stack variable
    reading or writing 
    exceptions


no side effects

In the presence of side effects, a program's meaning & behavior depends on history
the order of evaluation matters
side effects -> not referentially transparent


no side effects

Most functional languages use side-effects to some extent
it is a matter of style - poor or good
Some - Haskell & Clean - do not have side effects
     Haskell uses Monads
     Clean uses Uniqueness Types


referential transparency

if all functions are pure (always returns the same value) then this
implies determinism which
allows auto memoization


referential transparency

a non-pure function:     (current-time)


referential transparency


referential transparency


algebraic data types

a composite type
product types: tuples & records
sum types: tagged unions or variant types; enumerated types


algebraic data types


pattern matching

Operations on algebraic data types can be defined by using pattern matching to retrieve the arguments.
i.e. deconstructive binding


pattern matching


macros

allows strict-evaluation languages to not evaluate some code
i.e. control structures/forms
Lisps have eager evaluation - must evaluate all arguments before function is applied


macros


macros


macros

compiler construction kit with full language capabilites
Racket has used its hygenic macro system to implement
          typed Racket
          lazy Racket
          functional reactive Racket
          module and unit systems
          Java and Algol syntax languages
          CLOS style Meta Object Protocol
          etc       


 recursion & tail calls


reflexivity: metaprogramming

eval
macros - quasiquote & unquote
repl


garbage collection

we're all used to this now
ain’t it great! no malloc
but for a long time, functional languages were the only game in town


functional Languages

variations in languages
strict vs non-strict (eager vs lazy)
      print length([2+1, 3*2, 1/0, 5-4])
dynamic vs static typing with inference
pure vs impure


functional Languages

ML Family
  Standard ML
  Haskell
  Curry
  OCaml
  Clean


functional Languages

Lisp Family
  CLOS
  Scheme
  Racket
  Clojure
  Emacs Lisp


functional Languages

Others
  Erlang/Elixir
  Scala
  Kinda - Perl, Ruby, JavaScript, ...
  Still trying to catch up - Java


why functional?

can make powerful abstractions
functions are easy to create; don't need names
lifts the problem up into the domain of discourse -> domain specific language
abstractions allow for more structured programs
makes program more declarative, thus more comprehendible
good abstractions make programs shorter, thus easier to understand
productivity in terms of lines of code is same for any programming language, thus more productive
the high-level "what" rather than the low-level "how"


why functional?

pure functions are easy to test
In an imperative or OO language, you have to set up the state of the object, 
and the external state it reads or writes 
make the call
inspect the state of the object, and the external state
perhaps copy part of the object or global state, so that you can use it in the postcondition


why functional?

verifiable - in theory
practical, useful languages are not fully verifiable
but libraries & subsystems may be
better than nothing!


why functional?

concurrency (parallelism)
purely functional programs are deterministic
because there are no side effects nor immutable data structures
so order of evaluation is irrelevant
synchronization issues vanish
becomes more like the data flow paradigm

automatically parallelizing is another question, however
but higher order functions like map, fold, & reduce are inherently automatically parallelizable


why functional?

may not always be the right solution for the problem
but will provide you with the proper insight for when it is
most functional languages have imperitive and OO features as well


why functional?

Productivity
fewer lines of code per unit of functionality


