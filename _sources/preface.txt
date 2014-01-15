Preface
=======


Recently the programming community has been increasingly interested in
subsets of functional programming, such as immutable data structures, in
light of the challenges faced in developing concurrent systems. These
subsets are slowly being incorporated into mainstream programming
languages, such as Java with Project Lambda. Likewise, the number of
articles and books on the subject of functional programming have been
increasing steadily.

None the less, the idea of purely functional programming is not as
wide-spread, or understood by the programming community at
large. The idea of thinking about programs that contain no side-effects
after years of imperative programming is a challenging one. However,
pure functional programming offers many practical advantages for several
problems encountered when developing computer systems today, specially
in terms of maintainability.

This book introduces the purely functional approach to programming,
whose mathematical roots provide a straight-forward way of reasoning
about one's programs. Purely functional programs tend to be more
abstract and general, thus can be widely reused and composed in
different contexts. The goal of this book is to provide the reader with
enough understanding of the core foundations of functional programming,
and to be able to use those for building abstractions and managing
complexity by building larger programs through the composition of
smaller ones.

The material presented in this book is highly theoretical, including
recursion, co-recursion, persistent data structures, monads, and
others. The theory is explained through concrete examples, and practical
use cases. The reader should be able to see what a particular concept is
useful for in certain situations, and extrapolate from the presented
examples to other situations and contexts, that might arise in their
programs.

While the concepts and theories are general and applicable to most
programming languages, the code examples are provided using the
JavaScript language. JavaScript is not the most natural language for
purely functional programming, but it's a simple, and ubiquitous
language. These properties should allow the reader to quickly experiment
with the concepts and get feedback on their code. Familiarity with
JavaScript is not strictly required to read this book, though it never
teaches the language, the underlying semantics that are used thorough
are explained.
