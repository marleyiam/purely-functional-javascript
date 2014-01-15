==============
 Introduction
==============

Writing correct and maintainable software is a difficult task, specially as
software gets more and more complex, more and more concurrent, as the trend
suggests they shall. These problems motivate the pursuit of alternative
approaches to programming in order to keep up with the times, and functional
programming has been re-discovered over and over again over the past years,
with subsets of it slowly finding their way into mainstream programming
languages.

In the next chapters we will study the pure functional approach to programming,
from which most of today's ideas for managing complexity comes from. Functional
programming comes from the idea that programs are just mathematical
expressions, and can be resolved like any mathematical expression, by
substituting and reducing expressions. This in turn means that a computation
can't perform observable effects, such as showing a message on the screen, or
saving some contents to a file in the HDD.

At first, pure functional programming might sound like a fairly useless
approach, since the goal of all programs is to effect the world in some way,
and allow computer users to observe them. In fact, pure functional programming
makes such effects more powerful. By replacing the actual effects with a
description of what should happen they allow the programmer to abstract over
effects in the same way as they would abstract over any other value. An
interpreter then takes care of applying these descriptions to the world, in a
way that the effects can be observed.



Why Functional Programming Matters?
===================================

One might say that other approaches to programming can also solve the problem
of writing correct and maintainable software. That is true. There are many
approaches to programming that allow one to achieve such a goal, and functional
programming is just another approach.

There are two points where functional programming particularly excels:
reasoning, and abstracting. A pure functional program is just a mathematical
expression, and as such it can be understood by the use of equational
reasoning, just like any other mathematical computation. More so, functional
programming draws from some of the most abstract branches of mathematics, such
as Category Theory, in order to provide tools for generalising computations as
much as possible and increasing code re-usability, which in turn lessens the
amount of concepts that need to be understood by the programmer.

It's important to note that functional programming's influence of Category
Theory and other abstract branches of mathematics is a double-edged sword. On
one hand, it provides powerful tools for the programmer to manage complexity by
working with higher-level concepts, and the ability of applying such concepts
to as many contexts as possible. On the other hand, it offers little guidance
to the uninitiated, and can be perceived as a higher barrier to entry than a
programming approach that focuses on concrete concepts instead.

Thorough this book, we will see that, while the perceived conceptual barrier of
abstractions might be scary at first, they're easier to understand on the long
run, and not that difficult to learn. Besides, abstractions allow code to be
more reusable, such that bigger programs can be easily composed in terms of
smaller ones. This is an important characteristic for writing maintainable
software, as they grow more complex.

..
  :REVIEW:
  Probably would be interesting to create a better parallel between imperative
  programs and functional ones, with examples. Hughes' WFPM could also provide
  some good quotes.


Why use JavaScript?
===================

JavaScript isn't the simplest or most straight-forward language for the purely
functional approach, but it has one point in favour: it is ubiquitous. It's
much easier for one to explore the concepts presented in this book in
JavaScript, since it's fairly likely that they already got everything they
need.

Besides, pure functional programming is often seen as not-practical, and
fantasy-land of sorts, whereas JavaScript is increasingly seen as a practical
language. One of the goals of this book is to show that pure functional
programming can be not only practical, but also enjoyable, and
powerful. Applying the concepts to JavaScript seems to be a good way of
achieving this.

    “But JavaScript isn't a functional programming language!”

You will often see people saying that language X is or is not functional. Most
of these people actually mean that language X offers or not facilities to apply
the concepts of functional programming in a straight-forward fashion. Haskell
is seen as one of the best languages for applying this style of programming,
but for the concepts presented in this book, any programming language that
allows first-class and higher-order functions (such as Scheme, Python, Lua,
Smalltalk, etc.)  will suffice.


How to follow the examples in this book?
========================================

The examples in this book are presented using the JavaScript programming
language. If you're following the book in your web-browser, you likely have
everything that you need to for experimenting with the concepts. Just open the
JavaScript console on your browser's development tools and you're good to go.

Alternatively you can download `Node.js`_ and follow along in your terminal's
REPL. Or you can follow along in any language supporting first-class and
higher-order functions, if you prefer. But do note that this will require you
to have a comfortable knowledge of both the target programming language, and
JavaScript.

..
  :REVIEW:
  This should be entirely rewritten :(
