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

