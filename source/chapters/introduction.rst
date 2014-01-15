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



Why care about Functional Programming?
======================================

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


Why use JavaScript?
===================



