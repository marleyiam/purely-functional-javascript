=========================================
 Programming as Mathematical Expressions
=========================================

Programming is the act of communicating ideas with the computer in order
to have it do something for you. Incidentally, most of today's
programming happens using things called “Programming Languages,” which
are not much different from our so familiar natural languages, such as
English or French. They are composed of syntax (how you may form valid
constructs in the language), and semantics (what those valid constructs
mean). A programmer will usually wield both of these in order to express
a particular program.

But how can we understand programs? How do we know that what we've
communicated to the computer is, in fact, what we wanted to communicate?
When we're communicating with other people, we can look for hints in
their expressions and get immediate feedback on whether what we're
communicating is getting through or not, and if not, we can work
together on how to get our point across better, adapting our messages,
or the media we're using to communicate. We are not so lucky with
computers, unfortunately. The state of the tools for programming does
not allow such expressive way of finding what's wrong.

There are different approaches to assessing such errors, and
understanding the behaviour of our programs as the computer would. One
of them, which is fairly pervasive in the field, involves role-playing a
computer. You go through each line of your program and tell yourself to
do this, and do that. This approach involves a high cognitive load,
since one must keep in their head a broad range of knowledge about the
entire world, and how things affect one another. While there are certain
tools that might help one role-play computers, such as *stepping
debuggers*, they only lessen a the problem a little bit.

An alternative approach is to treat each program as a single
mathematical expression, such that one may understand the behaviour of
their programs by equational reasoning. This means that a programmer can
reason about their programs by understanding how the smaller and simpler
pieces work, and generalising to form the big picture. In other words,
if I can understand how addition works for 1 and 2, I can use that
knowledge for understanding how addition works for any two numbers N
and M. The big advantage of equational reasoning is that it frees the
programmer from role-playing computers, in a way that programmers and
computers can complement, and aid each other in constructing programs.

The idea of functional programming stems from the λ-calculus
mathematical formalism, developed by Alonzo Church. The idea of this
calculus is that computations are expressed entirely as function
abstractions and applications. It is, in essence, *programming with
(mathematical) functions*. Programs expressed in λ-calculus can be
resolved by substitution and reduction rules, similar to what one is
used to in simple mathematical expressions.


An overview of λ-calculus
=========================

But what is λ-calculus anyway? To understand, we can start from the
following mathematical expression:

.. math::

   x = 4 / 2


This expression tells us that :math:`\, x \,` is equivalent to the
expression :math:`\, 4 / 2 \,`, so anywhere we see :math:`\, x
\,` we can replace it by the thing on the right of the equals, and
vice-versa. We can further generalise this expression over all numbers:

.. math::

   half(x) = x / 2
   

Now we're getting close to λ-calculus. In λ-calculus, all expressions
are represented by functions, where functions are things that map inputs
over a particular domain (e.g.: all numbers), to an image. For the
aforementioned expression, it would be a function that maps all numbers
to their halves. There's only one catch with λ-calculus: in order to
achieve the abstractive power we want, we shall simplify the function
even further, by treating it anonymously. So, instead of giving the
function an explicit name, we'll just replace that name with the
:math:`\, \lambda \,` symbol:

.. math::

   \lambda x. x / 2


The previous form is called a **lambda abstraction**, as it represents a
mathematical expression in an abstract form, since some of the terms
that make up the expression are not concrete values. To move from an
abstract expression to a concrete one, we need to provide the values for
the lambda abstraction. This process is called **(function)
application**, and has a form similar to that of multiplication. That
is, it's a juxtaposition of terms :math:`\, t x \,`, where :math:`\, t
\,` and :math:`\, x \,` are both expressions. :math:`\, x \,` is called
the *argument* of the function application.

.. math::

   \begin{align}
       & (\lambda x. x / 2) 4  \\
     = & (\lambda 4. 4 / 2)
   \end{align}


Function application is straight-forward to reason about, since it just
means “substitute :math:`\, x \,` by this concrete value,” where the
concrete value in this case is 4. We can compute the value of any lambda
abstraction by substituting and reducing the expression to simpler
terms. This form of computation is called *the substitution model*, and
provides a powerful framework for understanding the computations:

.. math::

   \begin{align}
       & (\lambda x. x / 2) 4  \\
     = & (\lambda 4. 4 / 2)    \\
     = & (4 / 2)               \\
     = & 2
   \end{align}



The λ-calculus in JavaScript
============================

By understanding the previous section, you're one step from becoming a
programmer. The only thing left is to make the computer understand those
expressions. Sadly, there isn't a computer program that will interpret
such arcane mathametical symbols for you, so we'll have to use a
different set of symbols that our computer can understand instead. For
this, we'll use the JavaScript programming language.

In JavaScript, the ``function`` construct represents a lambda
abstraction. Note that, since JavaScript is not expression-oriented like
λ-calculus, we need to explicitly state that our lambda abstraction is
the same as the expression ``x / 2`` using the ``return`` construct::


    (function (x) { return x / 2 })


Likewise, λ-calculus' function application concept is represented by the
function application construct in JavaScript, where instead of simply
juxtaposing the argument, we need to put it inside parenthesis::


    (function (x) { return x / 2 })(4)


You can run this snippet in your JavaScript console, and it'll answer
you 2. Try changing the value of the argument and see what happens.

At this point, you can proudly call yourself a
programmer. Unfortunately, the amount of programs you can express using
the concepts explained is small. But don't worry. λ-calculus can express
complex computations as well, and these forms of computation are what
the next section is all about!


Abstracting the abstractions
============================


