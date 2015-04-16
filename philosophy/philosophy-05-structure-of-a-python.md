Structure of a Python Program
=============================

**If might help to try things out in Python as you read through.**

Python programs (and indeed most computer programs) consist of a
series of *statements*. Each statement performs an action and the
statements are executed in order, one after the other.

Simple statements are a single line of code. For example ``x = 2 + 3``
is a statement that attaches the label ``x`` to the value ``5``.

Labels like ``x`` are sometimes called *variables* or
*identifiers*. In Python it is useful to think of labels as tags that
one can tie to objects. A tag may be tied to any object, and even
untied and then tied to a new object. Tying a tag to an object doesn't
change what the object is.

Things like ``2 + 3`` that result in a value are called
*expressions*. ``2 * x`` is an expression that evaluates to ``10``
(assuming ``x`` is still tied to ``5``).

The statement ``x = 2 + 3`` is an example of the assignment
statement. Assignment statements have the form ``<label> =
<expression>`` and allow any label to be attached to the result of the
expression. The expression is evaluated as part of the statements
action.

A little confusingly, assignments like ``x = x + 1`` are allowed. The
rule is that expression is evaluated first and then the result is
attached to the label afterwards. So, for example, if ``x`` is ``5``
to start with, then ``x = x + 1`` results in ``x`` being attached to
``5` afterwards.


Constants
---------

Constants are a common, simple and very useful kind of expression
built in to Python. There are a variey of different types of
constants.

We have already seen integer constants like ``2``, ``3`` and
``5``. These represent the corresponding whole numbers. Python also
allows negative numbers like ``-1``, ``-3``, ``-10``.

Decimal fractions are a different type, but are represented in similar
way: ``1.5``, ``-2.0``. Fractions may also be entered using scientific
notation such as ``-1.5e6`` which evaluates to ``-1.5 * 10**6`` (the
``**`` operator in Python represents "to the power of").

String constants represent strings of characters such as words and
sentences and are enclosed in either single quotes or double
quotes. For example, ``"a"`` evaluates to the letter a, ``'red'``
evaluates to the word "red" and ``"Hello, world!"`` evaluates to the
sentence "Hello, world!".

There are also a few special constants. The constants ``True`` and
``False`` represent the concepts of something being true or being
false. The constant ``None`` represents the concept of something being
absent.

Lists and tuples
----------------

Python also allows some more complex constant expressions. Lists and
tuples both represent ordered lists of items. However, lists can be
modified later, while tuples are fixed once created.

Lists constants use square brackets, e.g. ``[1, "foo", 1.5]``
evaluates to a list containing the values ``1``, ``"foo"`` and ``1.5``
(in that order).

Tuples used round brakcets, e.g. ``(1, "foo", 1.5)``.

If we assign a list or tuple to a label, e.g. ``l = ["a", "b", "c"]``,
there is a special expression syntax for accessing the items within
the list. For example, ``l[0]`` accesses the first item (``"a"""``),
``l[1]`` the second (``"b"``) and so on.

Accessing items with square brackets works for tuples too -- try it. :)


Dictionaries
------------

Python also has constants for dictionaries, which are often called
"maps" in other programming languages because they map one set of
values to another (in the same way that dictionaries map words to
definitions).

Dictionary contants use curly brackets, e.g. ``d = {"a": 1, "r": 3,
"e": 4}``. This maps ``"a"`` to ``1``, ``"r"`` to ``3`` and ``"e"`` to
``4``. We can look up values in a dictionary using square brackets,
the same way we look up items in lists and tuples, e.g. ``d["r"]`` is
an expression that evalues to ``3`` in this case.


Block statements
----------------

Python programmes may be divided up into *blocks* of statements. A
*block* consists of a contiguous list of statements all indented the
same amount.

A *block statement* is a more complex form of statement that contains
within in it a block of statements. For example:

    def f(x):
        y = x * 2
        return y

is a block statement that defines a function. The function's name is
``f`` and it contains two simple statements. ``y = x * 2`` is an
assignment statement like the ones we've seen before. ``return y`` is
a special statement that can only be used inside a function and
returns expression given when the function is called. Calling a
function runs the statements inside the statement block and returns
the specified result. For example, ``f(5)`` would evaluate to ``10``
in this case.

Another example a block statement is a loop or *for statement*:

    for x in [1, 2, 3]:
        y = x * x
        print y

In python, a loop runs the given statement block once for each item in
a list. In the example above the list is ``[1, 2, 3]``, so the block
of statements will be run three times, first with ``x = 1``, then with
``x = 2``, then with ``x = 3``. What will this for loop print out?

The last common kind of block statement is the *if statement* which
runs the contained block if some expression evaluates to a "true"
result:

    if x == 3:
        print "x is three!"

This will print "x is three!" is the value of ``x`` is ``3`` and no
execute any statements otherwise. ``x == 3``.


Operators
---------

We've been glossing over things like ``*``, ``+``, ``-``, ``==`` and
``**``. These are called *operators* because they operator on
expressions to produce new expressions. For example, in ``2 + 3``,
``+`` operators on ``2`` and ``3`` and adds them to produce ``5``.

``==`` is an example of a comparison operators -- it compares two
expressions and returns ``True`` if they are equal and ``False`` if
they are not. ``<``, ``>``, ``>=`` and ``<=`` are other examples of
comparison operators. Try them out to see what they do.



Glossary
--------

* *statement*: performs an action.
* *expression*: result in a value.
* *variables*: labels that can be attached to values.
* *block*: a group of statements all indented the same amount.
* *block statement*: a complex statement that contains blocks of other statements.
* *operators*: operate on expressions to produce new expressions.


Futher reading
--------------

* [An Informal Introduction to Python](https://docs.python.org/2/tutorial/introduction.html)
* [More Control Flow Tools](https://docs.python.org/2/tutorial/controlflow.html)
