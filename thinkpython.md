---
author:
- Allen B. Downey
title: Think Python
---

\[chapter\]

9pt 9pt 0.5em

3 Think Python\
How to Think Like a Computer Scientist

2nd Edition, Version 2.4.0

3 Think Python\
How to Think Like a Computer Scientist

2nd Edition, Version 2.4.0

Allen Downey\

Green Tea Press

Needham, Massachusetts

Copyright © 2015 Allen Downey.

Green Tea Press\
9 Washburn Ave\
Needham MA 02492

Permission is granted to copy, distribute, and/or modify this document
under the terms of the Creative Commons Attribution-NonCommercial 3.0
Unported License, which is available at
<http://creativecommons.org/licenses/by-nc/3.0/>.

The original form of this book is LaTeX source code. Compiling this
LaTeX source has the effect of generating a device-independent
representation of a textbook, which can be converted to other formats
and printed.

The LaTeX source for this book is available from
<http://www.thinkpython2.com>

Think Python: How to Think Like a Computer Scientist

Allen B. Downey

2nd Edition, Version 2.4.0

Preface
=======

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex \*The strange history of this
book

In January 1999 I was preparing to teach an introductory programming
class in Java. I had taught it three times and I was getting frustrated.
The failure rate in the class was too high and, even for students who
succeeded, the overall level of achievement was too low.

One of the problems I saw was the books. They were too big, with too
much unnecessary detail about Java, and not enough high-level guidance
about how to program. And they all suffered from the trap door effect:
they would start out easy, proceed gradually, and then somewhere around
Chapter 5 the bottom would fall out. The students would get too much new
material, too fast, and I would spend the rest of the semester picking
up the pieces.

Two weeks before the first day of classes, I decided to write my own
book. My goals were:

-   Keep it short. It is better for students to read 10 pages than not
    read 50 pages.

-   Be careful with vocabulary. I tried to minimize jargon and define
    each term at first use.

-   Build gradually. To avoid trap doors, I took the most difficult
    topics and split them into a series of small steps.

-   Focus on programming, not the programming language. I included the
    minimum useful subset of Java and left out the rest.

I needed a title, so on a whim I chose *How to Think Like a Computer
Scientist*.

My first version was rough, but it worked. Students did the reading, and
they understood enough that I could spend class time on the hard topics,
the interesting topics and (most important) letting the students
practice.

I released the book under the GNU Free Documentation License, which
allows users to copy, modify, and distribute the book.

What happened next is the cool part. Jeff Elkner, a high school teacher
in Virginia, adopted my book and translated it into Python. He sent me a
copy of his translation, and I had the unusual experience of learning
Python by reading my own book. As Green Tea Press, I published the first
Python version in 2001.

In 2003 I started teaching at Olin College and I got to teach Python for
the first time. The contrast with Java was striking. Students struggled
less, learned more, worked on more interesting projects, and generally
had a lot more fun.

Since then I've continued to develop the book, correcting errors,
improving some of the examples and adding material, especially
exercises.

The result is this book, now with the less grandiose title *Think
Python*. Some of the changes are:

-   I added a section about debugging at the end of each chapter. These
    sections present general techniques for finding and avoiding bugs,
    and warnings about Python pitfalls.

-   I added more exercises, ranging from short tests of understanding to
    a few substantial projects. Most exercises include a link to my
    solution.

-   I added a series of case studies---longer examples with exercises,
    solutions, and discussion.

-   I expanded the discussion of program development plans and basic
    design patterns.

-   I added appendices about debugging and analysis of algorithms.

The second edition of *Think Python* has these new features:

-   The book and all supporting code have been updated to Python 3.

-   I added a few sections, and more details on the web, to help
    beginners get started running Python in a browser, so you don't have
    to deal with installing Python until you want to.

-   For Chapter [\[turtle\]](#turtle){reference-type="ref"
    reference="turtle"} I switched from my own turtle graphics package,
    called Swampy, to a more standard Python module, ` turtle`, which is
    easier to install and more powerful.

-   I added a new chapter called "The Goodies", which introduces some
    additional Python features that are not strictly necessary, but
    sometimes handy.

I hope you enjoy working with this book, and that it helps you learn to
program and think like a computer scientist, at least a little bit.

Allen B. Downey\
Olin College\
section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex \*Acknowledgments

Many thanks to Jeff Elkner, who translated my Java book into Python,
which got this project started and introduced me to what has turned out
to be my favorite language.

Thanks also to Chris Meyers, who contributed several sections to *How to
Think Like a Computer Scientist*.

Thanks to the Free Software Foundation for developing the GNU Free
Documentation License, which helped make my collaboration with Jeff and
Chris possible, and Creative Commons for the license I am using now.

Thanks to the editors at Lulu who worked on *How to Think Like a
Computer Scientist*.

Thanks to the editors at O'Reilly Media who worked on *Think Python*.

Thanks to all the students who worked with earlier versions of this book
and all the contributors (listed below) who sent in corrections and
suggestions.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex \*Contributor List

More than 100 sharp-eyed and thoughtful readers have sent in suggestions
and corrections over the past few years. Their contributions, and
enthusiasm for this project, have been a huge help.

If you have a suggestion or correction, please send email to
`feedback@thinkpython.com`. If I make a change based on your feedback, I
will add you to the contributor list (unless you ask to be omitted).

If you include at least part of the sentence the error appears in, that
makes it easy for me to search. Page and section numbers are fine, too,
but not quite as easy to work with. Thanks!

-   Lloyd Hugh Allen sent in a correction to Section 8.4.

-   Yvon Boulianne sent in a correction of a semantic error in
    Chapter 5.

-   Fred Bremmer submitted a correction in Section 2.1.

-   Jonah Cohen wrote the Perl scripts to convert the LaTeX source for
    this book into beautiful HTML.

-   Michael Conlon sent in a grammar correction in Chapter 2 and an
    improvement in style in Chapter 1, and he initiated discussion on
    the technical aspects of interpreters.

-   Benoît Girard sent in a correction to a humorous mistake in Section
    5.6.

-   Courtney Gleason and Katherine Smith wrote `horsebet.py`, which was
    used as a case study in an earlier version of the book. Their
    program can now be found on the website.

-   Lee Harr submitted more corrections than we have room to list here,
    and indeed he should be listed as one of the principal editors of
    the text.

-   James Kaylin is a student using the text. He has submitted numerous
    corrections.

-   David Kershaw fixed the broken `catTwice` function in Section 3.10.

-   Eddie Lam has sent in numerous corrections to Chapters 1, 2, and 3.
    He also fixed the Makefile so that it creates an index the first
    time it is run and helped us set up a versioning scheme.

-   Man-Yong Lee sent in a correction to the example code in Section
    2.4.

-   David Mayo pointed out that the word "unconsciously\" in Chapter 1
    needed to be changed to "subconsciously\".

-   Chris McAloon sent in several corrections to Sections 3.9 and 3.10.

-   Matthew J. Moelter has been a long-time contributor who sent in
    numerous corrections and suggestions to the book.

-   Simon Dicon Montford reported a missing function definition and
    several typos in Chapter 3. He also found errors in the `increment`
    function in Chapter 13.

-   John Ouzts corrected the definition of "return value\" in Chapter 3.

-   Kevin Parks sent in valuable comments and suggestions as to how to
    improve the distribution of the book.

-   David Pool sent in a typo in the glossary of Chapter 1, as well as
    kind words of encouragement.

-   Michael Schmitt sent in a correction to the chapter on files and
    exceptions.

-   Robin Shaw pointed out an error in Section 13.1, where the printTime
    function was used in an example without being defined.

-   Paul Sleigh found an error in Chapter 7 and a bug in Jonah Cohen's
    Perl script that generates HTML from LaTeX.

-   Craig T. Snydal is testing the text in a course at Drew University.
    He has contributed several valuable suggestions and corrections.

-   Ian Thomas and his students are using the text in a programming
    course. They are the first ones to test the chapters in the latter
    half of the book, and they have made numerous corrections and
    suggestions.

-   Keith Verheyden sent in a correction in Chapter 3.

-   Peter Winstanley let us know about a longstanding error in our Latin
    in Chapter 3.

-   Chris Wrobel made corrections to the code in the chapter on file I/O
    and exceptions.

-   Moshe Zadka has made invaluable contributions to this project. In
    addition to writing the first draft of the chapter on Dictionaries,
    he provided continual guidance in the early stages of the book.

-   Christoph Zwerschke sent several corrections and pedagogic
    suggestions, and explained the difference between *gleich* and
    *selbe*.

-   James Mayer sent us a whole slew of spelling and typographical
    errors, including two in the contributor list.

-   Hayden McAfee caught a potentially confusing inconsistency between
    two examples.

-   Angel Arnal is part of an international team of translators working
    on the Spanish version of the text. He has also found several errors
    in the English version.

-   Tauhidul Hoque and Lex Berezhny created the illustrations in Chapter
    1 and improved many of the other illustrations.

-   Dr. Michele Alzetta caught an error in Chapter 8 and sent some
    interesting pedagogic comments and suggestions about Fibonacci and
    Old Maid.

-   Andy Mitchell caught a typo in Chapter 1 and a broken example in
    Chapter 2.

-   Kalin Harvey suggested a clarification in Chapter 7 and caught some
    typos.

-   Christopher P. Smith caught several typos and helped us update the
    book for Python 2.2.

-   David Hutchins caught a typo in the Foreword.

-   Gregor Lingl is teaching Python at a high school in Vienna, Austria.
    He is working on a German translation of the book, and he caught a
    couple of bad errors in Chapter 5.

-   Julie Peters caught a typo in the Preface.

-   Florin Oprina sent in an improvement in `makeTime`, a correction in
    `printTime`, and a nice typo.

-   D. J. Webre suggested a clarification in Chapter 3.

-   Ken found a fistful of errors in Chapters 8, 9 and 11.

-   Ivo Wever caught a typo in Chapter 5 and suggested a clarification
    in Chapter 3.

-   Curtis Yanko suggested a clarification in Chapter 2.

-   Ben Logan sent in a number of typos and problems with translating
    the book into HTML.

-   Jason Armstrong saw the missing word in Chapter 2.

-   Louis Cordier noticed a spot in Chapter 16 where the code didn't
    match the text.

-   Brian Cain suggested several clarifications in Chapters 2 and 3.

-   Rob Black sent in a passel of corrections, including some changes
    for Python 2.2.

-   Jean-Philippe Rey at École Centrale Paris sent a number of patches,
    including some updates for Python 2.2 and other thoughtful
    improvements.

-   Jason Mader at George Washington University made a number of useful
    suggestions and corrections.

-   Jan Gundtofte-Bruun reminded us that "a error" is an error.

-   Abel David and Alexis Dinno reminded us that the plural of "matrix"
    is "matrices", not "matrixes". This error was in the book for years,
    but two readers with the same initials reported it on the same day.
    Weird.

-   Charles Thayer encouraged us to get rid of the semi-colons we had
    put at the ends of some statements and to clean up our use of
    "argument" and "parameter".

-   Roger Sperberg pointed out a twisted piece of logic in Chapter 3.

-   Sam Bull pointed out a confusing paragraph in Chapter 2.

-   Andrew Cheung pointed out two instances of "use before def".

-   C. Corey Capel spotted the missing word in the Third Theorem of
    Debugging and a typo in Chapter 4.

-   Alessandra helped clear up some Turtle confusion.

-   Wim Champagne found a brain-o in a dictionary example.

-   Douglas Wright pointed out a problem with floor division in `arc`.

-   Jared Spindor found some jetsam at the end of a sentence.

-   Lin Peiheng sent a number of very helpful suggestions.

-   Ray Hagtvedt sent in two errors and a not-quite-error.

-   Torsten Hübsch pointed out an inconsistency in Swampy.

-   Inga Petuhhov corrected an example in Chapter 14.

-   Arne Babenhauserheide sent several helpful corrections.

-   Mark E. Casida is is good at spotting repeated words.

-   Scott Tyler filled in a that was missing. And then sent in a heap of
    corrections.

-   Gordon Shephard sent in several corrections, all in separate emails.

-   Andrew Turner `spot`ted an error in Chapter 8.

-   Adam Hobart fixed a problem with floor division in `arc`.

-   Daryl Hammond and Sarah Zimmerman pointed out that I served up
    `math.pi` too early. And Zim spotted a typo.

-   George Sass found a bug in a Debugging section.

-   Brian Bingham suggested
    Exercise [\[exrotatepairs\]](#exrotatepairs){reference-type="ref"
    reference="exrotatepairs"}.

-   Leah Engelbert-Fenton pointed out that I used `tuple` as a variable
    name, contrary to my own advice. And then found a bunch of typos and
    a "use before def".

-   Joe Funke spotted a typo.

-   Chao-chao Chen found an inconsistency in the Fibonacci example.

-   Jeff Paine knows the difference between space and spam.

-   Lubos Pintes sent in a typo.

-   Gregg Lind and Abigail Heithoff suggested
    Exercise [\[checksum\]](#checksum){reference-type="ref"
    reference="checksum"}.

-   Max Hailperin has sent in a number of corrections and suggestions.
    Max is one of the authors of the extraordinary *Concrete
    Abstractions*, which you might want to read when you are done with
    this book.

-   Chotipat Pornavalai found an error in an error message.

-   Stanislaw Antol sent a list of very helpful suggestions.

-   Eric Pashman sent a number of corrections for Chapters 4--11.

-   Miguel Azevedo found some typos.

-   Jianhua Liu sent in a long list of corrections.

-   Nick King found a missing word.

-   Martin Zuther sent a long list of suggestions.

-   Adam Zimmerman found an inconsistency in my instance of an
    "instance" and several other errors.

-   Ratnakar Tiwari suggested a footnote explaining degenerate
    triangles.

-   Anurag Goel suggested another solution for `is_abecedarian` and sent
    some additional corrections. And he knows how to spell Jane Austen.

-   Kelli Kratzer spotted one of the typos.

-   Mark Griffiths pointed out a confusing example in Chapter 3.

-   Roydan Ongie found an error in my Newton's method.

-   Patryk Wolowiec helped me with a problem in the HTML version.

-   Mark Chonofsky told me about a new keyword in Python 3.

-   Russell Coleman helped me with my geometry.

-   Nam Nguyen found a typo and pointed out that I used the Decorator
    pattern but didn't mention it by name.

-   Stéphane Morin sent in several corrections and suggestions.

-   Paul Stoop corrected a typo in `uses_only`.

-   Eric Bronner pointed out a confusion in the discussion of the order
    of operations.

-   Alexandros Gezerlis set a new standard for the number and quality of
    suggestions he submitted. We are deeply grateful!

-   Gray Thomas knows his right from his left.

-   Giovanni Escobar Sosa sent a long list of corrections and
    suggestions.

-   Daniel Neilson corrected an error about the order of operations.

-   Will McGinnis pointed out that `polyline` was defined differently in
    two places.

-   Frank Hecker pointed out an exercise that was under-specified, and
    some broken links.

-   Animesh B helped me clean up a confusing example.

-   Martin Caspersen found two round-off errors.

-   Gregor Ulm sent several corrections and suggestions.

-   Dimitrios Tsirigkas suggested I clarify an exercise.

-   Carlos Tafur sent a page of corrections and suggestions.

-   Martin Nordsletten found a bug in an exercise solution.

-   Sven Hoexter pointed out that a variable named `input` shadows a
    build-in function.

-   Stephen Gregory pointed out the problem with `cmp` in Python 3.

-   Ishwar Bhat corrected my statement of Fermat's last theorem.

-   Andrea Zanella translated the book into Italian, and sent a number
    of corrections along the way.

-   Many, many thanks to Melissa Lewis and Luciano Ramalho for excellent
    comments and suggestions on the second edition.

-   Thanks to Harry Percival from PythonAnywhere for his help getting
    people started running Python in a browser.

-   Xavier Van Aubel made several useful corrections in the second
    edition.

-   William Murray corrected my definition of floor division.

-   Per Starbäck brought me up to date on universal newlines in
    Python 3.

-   Laurent Rosenfeld and Mihaela Rotaru translated this book into
    French. Along the way, they sent many corrections and suggestions.

    In addition, people who spotted typos or made corrections include
    Czeslaw Czapla, Dale Wilson, Francesco Carlo Cimini, Richard Fursa,
    Brian McGhie, Lokesh Kumar Makani, Matthew Shultz, Viet Le, Victor
    Simeone, Lars O.D. Christensen, Swarup Sahoo, Alix Etienne, Kuang
    He, Wei Huang, Karen Barber, and Eric Ransom.

The way of the program
======================

The goal of this book is to teach you to think like a computer
scientist. This way of thinking combines some of the best features of
mathematics, engineering, and natural science. Like mathematicians,
computer scientists use formal languages to denote ideas (specifically
computations). Like engineers, they design things, assembling components
into systems and evaluating tradeoffs among alternatives. Like
scientists, they observe the behavior of complex systems, form
hypotheses, and test predictions.

The single most important skill for a computer scientist is **problem
solving**. Problem solving means the ability to formulate problems,
think creatively about solutions, and express a solution clearly and
accurately. As it turns out, the process of learning to program is an
excellent opportunity to practice problem-solving skills. That's why
this chapter is called, "The way of the program".

On one level, you will be learning to program, a useful skill by itself.
On another level, you will use programming as a means to an end. As we
go along, that end will become clearer.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex What is a program?

A **program** is a sequence of instructions that specifies how to
perform a computation. The computation might be something mathematical,
such as solving a system of equations or finding the roots of a
polynomial, but it can also be a symbolic computation, such as searching
and replacing text in a document or something graphical, like processing
an image or playing a video.

The details look different in different languages, but a few basic
instructions appear in just about every language:

input:

:   Get data from the keyboard, a file, the network, or some other
    device.

output:

:   Display data on the screen, save it in a file, send it over the
    network, etc.

math:

:   Perform basic mathematical operations like addition and
    multiplication.

conditional execution:

:   Check for certain conditions and run the appropriate code.

repetition:

:   Perform some action repeatedly, usually with some variation.

Believe it or not, that's pretty much all there is to it. Every program
you've ever used, no matter how complicated, is made up of instructions
that look pretty much like these. So you can think of programming as the
process of breaking a large, complex task into smaller and smaller
subtasks until the subtasks are simple enough to be performed with one
of these basic instructions.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Running Python

One of the challenges of getting started with Python is that you might
have to install Python and related software on your computer. If you are
familiar with your operating system, and especially if you are
comfortable with the command-line interface, you will have no trouble
installing Python. But for beginners, it can be painful to learn about
system administration and programming at the same time.

To avoid that problem, I recommend that you start out running Python in
a browser. Later, when you are comfortable with Python, I'll make
suggestions for installing Python on your computer.

There are a number of web pages you can use to run Python. If you
already have a favorite, go ahead and use it. Otherwise I recommend
PythonAnywhere. I provide detailed instructions for getting started at
<http://tinyurl.com/thinkpython2e>.

There are two versions of Python, called Python 2 and Python 3. They are
very similar, so if you learn one, it is easy to switch to the other. In
fact, there are only a few differences you will encounter as a beginner.
This book is written for Python 3, but I include some notes about Python
2.

The Python **interpreter** is a program that reads and executes Python
code. Depending on your environment, you might start the interpreter by
clicking on an icon, or by typing `python` on a command line. When it
starts, you should see output like this:

    Python 3.4.0 (default, Jun 19 2015, 14:20:21) 
    [GCC 4.8.2] on linux
    Type "help", "copyright", "credits" or "license" for more information.
    >>> 

The first three lines contain information about the interpreter and the
operating system it's running on, so it might be different for you. But
you should check that the version number, which is `3.4.0` in this
example, begins with 3, which indicates that you are running Python 3.
If it begins with 2, you are running (you guessed it) Python 2.

The last line is a **prompt** that indicates that the interpreter is
ready for you to enter code. If you type a line of code and hit Enter,
the interpreter displays the result:

    >>> 1 + 1
    2

Now you're ready to get started. From here on, I assume that you know
how to start the Python interpreter and run code.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex The first program
[\[hello\]]{#hello label="hello"}

Traditionally, the first program you write in a new language is called
"Hello, World!" because all it does is display the words "Hello,
World!". In Python, it looks like this:

    >>> print('Hello, World!')

This is an example of a **print statement**, although it doesn't
actually print anything on paper. It displays a result on the screen. In
this case, the result is the words

    Hello, World!

The quotation marks in the program mark the beginning and end of the
text to be displayed; they don't appear in the result.

The parentheses indicate that `print` is a function. We'll get to
functions in Chapter [4](#funcchap){reference-type="ref"
reference="funcchap"}.

In Python 2, the print statement is slightly different; it is not a
function, so it doesn't use parentheses.

    >>> print 'Hello, World!'

This distinction will make more sense soon, but that's enough to get
started.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Arithmetic operators

After "Hello, World", the next step is arithmetic. Python provides
**operators**, which are special symbols that represent computations
like addition and multiplication.

The operators `+`, `-`, and `` perform addition, subtraction, and
multiplication, as in the following examples:

    >>> 40 + 2
    42
    >>> 43 - 1
    42
    >>> 6 * 7
    42

The operator `/` performs division:

    >>> 84 / 2
    42.0

You might wonder why the result is `42.0` instead of `42`. I'll explain
in the next section.

Finally, the operator `*` performs exponentiation; that is, it raises a
number to a power:

    >>> 6**2 + 6
    42

In some other languages, `^` is used for exponentiation, but in Python
it is a bitwise operator called XOR. If you are not familiar with
bitwise operators, the result will surprise you:

    >>> 6 ^ 2
    4

I won't cover bitwise operators in this book, but you can read about
them at <http://wiki.python.org/moin/BitwiseOperators>.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Values and types

A **value** is one of the basic things a program works with, like a
letter or a number. Some values we have seen so far are `2`, `42.0`, and
`'Hello, World!'`.

These values belong to different **types**: `2` is an **integer**,
`42.0` is a **floating-point number**, and `'Hello, World!'` is a
**string**, so-called because the letters it contains are strung
together.

If you are not sure what type a value has, the interpreter can tell you:

    >>> type(2)
    <class 'int'>
    >>> type(42.0)
    <class 'float'>
    >>> type('Hello, World!')
    <class 'str'>

In these results, the word "class" is used in the sense of a category; a
type is a category of values.

Not surprisingly, integers belong to the type `int`, strings belong to
`str` and floating-point numbers belong to `float`.

What about values like `'2'` and `'42.0'`? They look like numbers, but
they are in quotation marks like strings.

    >>> type('2')
    <class 'str'>
    >>> type('42.0')
    <class 'str'>

They're strings.

When you type a large integer, you might be tempted to use commas
between groups of digits, as in `1,000,000`. This is not a legal
*integer* in Python, but it is legal:

    >>> 1,000,000
    (1, 0, 0)

That's not what we expected at all! Python interprets ` 1,000,000` as a
comma-separated sequence of integers. We'll learn more about this kind
of sequence later.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Formal and natural languages

**Natural languages** are the languages people speak, such as English,
Spanish, and French. They were not designed by people (although people
try to impose some order on them); they evolved naturally.

**Formal languages** are languages that are designed by people for
specific applications. For example, the notation that mathematicians use
is a formal language that is particularly good at denoting relationships
among numbers and symbols. Chemists use a formal language to represent
the chemical structure of molecules. And most importantly:

> **Programming languages are formal languages that have been designed
> to express computations.**

Formal languages tend to have strict **syntax** rules that govern the
structure of statements. For example, in mathematics the statement
$3 + 3 = 6$ has correct syntax, but $3 + = 3 \$ 6$ does not. In
chemistry $H_2O$ is a syntactically correct formula, but $_2Zz$ is not.

Syntax rules come in two flavors, pertaining to **tokens** and
structure. Tokens are the basic elements of the language, such as words,
numbers, and chemical elements. One of the problems with $3 += 3 \$ 6$
is that $\$$ is not a legal token in mathematics (at least as far as I
know). Similarly, $_2Zz$ is not legal because there is no element with
the abbreviation $Zz$.

The second type of syntax rule pertains to the way tokens are combined.
The equation $3 +/ 3$ is illegal because even though $+$ and $/$ are
legal tokens, you can't have one right after the other. Similarly, in a
chemical formula the subscript comes after the element name, not before.

This is @ well-structured Engli\$h sentence with invalid t\*kens in it.
This sentence all valid tokens has, but invalid structure with.

When you read a sentence in English or a statement in a formal language,
you have to figure out the structure (although in a natural language you
do this subconsciously). This process is called **parsing**.

Although formal and natural languages have many features in
common---tokens, structure, and syntax---there are some differences:

ambiguity:

:   Natural languages are full of ambiguity, which people deal with by
    using contextual clues and other information. Formal languages are
    designed to be nearly or completely unambiguous, which means that
    any statement has exactly one meaning, regardless of context.

redundancy:

:   In order to make up for ambiguity and reduce misunderstandings,
    natural languages employ lots of redundancy. As a result, they are
    often verbose. Formal languages are less redundant and more concise.

literalness:

:   Natural languages are full of idiom and metaphor. If I say, "The
    penny dropped", there is probably no penny and nothing dropping
    (this idiom means that someone understood something after a period
    of confusion). Formal languages mean exactly what they say.

Because we all grow up speaking natural languages, it is sometimes hard
to adjust to formal languages. The difference between formal and natural
language is like the difference between poetry and prose, but more so:

Poetry:

:   Words are used for their sounds as well as for their meaning, and
    the whole poem together creates an effect or emotional response.
    Ambiguity is not only common but often deliberate.

Prose:

:   The literal meaning of words is more important, and the structure
    contributes more meaning. Prose is more amenable to analysis than
    poetry but still often ambiguous.

Programs:

:   The meaning of a computer program is unambiguous and literal, and
    can be understood entirely by analysis of the tokens and structure.

Formal languages are more dense than natural languages, so it takes
longer to read them. Also, the structure is important, so it is not
always best to read from top to bottom, left to right. Instead, learn to
parse the program in your head, identifying the tokens and interpreting
the structure. Finally, the details matter. Small errors in spelling and
punctuation, which you can get away with in natural languages, can make
a big difference in a formal language.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Debugging

Programmers make mistakes. For whimsical reasons, programming errors are
called **bugs** and the process of tracking them down is called
**debugging**.

Programming, and especially debugging, sometimes brings out strong
emotions. If you are struggling with a difficult bug, you might feel
angry, despondent, or embarrassed.

There is evidence that people naturally respond to computers as if they
were people. When they work well, we think of them as teammates, and
when they are obstinate or rude, we respond to them the same way we
respond to rude, obstinate people (Reeves and Nass, *The Media Equation:
How People Treat Computers, Television, and New Media Like Real People
and Places*).

Preparing for these reactions might help you deal with them. One
approach is to think of the computer as an employee with certain
strengths, like speed and precision, and particular weaknesses, like
lack of empathy and inability to grasp the big picture.

Your job is to be a good manager: find ways to take advantage of the
strengths and mitigate the weaknesses. And find ways to use your
emotions to engage with the problem, without letting your reactions
interfere with your ability to work effectively.

Learning to debug can be frustrating, but it is a valuable skill that is
useful for many activities beyond programming. At the end of each
chapter there is a section, like this one, with my suggestions for
debugging. I hope they help!

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Glossary

problem solving:

:   The process of formulating a problem, finding a solution, and
    expressing it.

high-level language:

:   A programming language like Python that is designed to be easy for
    humans to read and write.

low-level language:

:   A programming language that is designed to be easy for a computer to
    run; also called "machine language" or "assembly language".

portability:

:   A property of a program that can run on more than one kind of
    computer.

interpreter:

:   A program that reads another program and executes it

prompt:

:   Characters displayed by the interpreter to indicate that it is ready
    to take input from the user.

program:

:   A set of instructions that specifies a computation.

print statement:

:   An instruction that causes the Python interpreter to display a value
    on the screen.

operator:

:   A special symbol that represents a simple computation like addition,
    multiplication, or string concatenation.

value:

:   One of the basic units of data, like a number or string, that a
    program manipulates.

type:

:   A category of values. The types we have seen so far are integers
    (type `int`), floating-point numbers (type ` float`), and strings
    (type `str`).

integer:

:   A type that represents whole numbers.

floating-point:

:   A type that represents numbers with fractional parts.

string:

:   A type that represents sequences of characters.

natural language:

:   Any one of the languages that people speak that evolved naturally.

formal language:

:   Any one of the languages that people have designed for specific
    purposes, such as representing mathematical ideas or computer
    programs; all programming languages are formal languages.

token:

:   One of the basic elements of the syntactic structure of a program,
    analogous to a word in a natural language.

syntax:

:   The rules that govern the structure of a program.

parse:

:   To examine a program and analyze the syntactic structure.

bug:

:   An error in a program.

debugging:

:   The process of finding and correcting bugs.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

It is a good idea to read this book in front of a computer so you can
try out the examples as you go.

Whenever you are experimenting with a new feature, you should try to
make mistakes. For example, in the "Hello, world!" program, what happens
if you leave out one of the quotation marks? What if you leave out both?
What if you spell `print` wrong?

This kind of experiment helps you remember what you read; it also helps
when you are programming, because you get to know what the error
messages mean. It is better to make mistakes now and on purpose than
later and accidentally.

1.  In a print statement, what happens if you leave out one of the
    parentheses, or both?

2.  If you are trying to print a string, what happens if you leave out
    one of the quotation marks, or both?

3.  You can use a minus sign to make a negative number like `-2`. What
    happens if you put a plus sign before a number? What about `2++2`?

4.  In math notation, leading zeros are ok, as in `09`. What happens if
    you try this in Python? What about `011`?

5.  What happens if you have two values with no operator between them?

Start the Python interpreter and use it as a calculator.

1.  How many seconds are there in 42 minutes 42 seconds?

2.  How many miles are there in 10 kilometers? Hint: there are 1.61
    kilometers in a mile.

3.  If you run a 10 kilometer race in 42 minutes 42 seconds, what is
    your average pace (time per mile in minutes and seconds)? What is
    your average speed in miles per hour?

Variables, expressions and statements
=====================================

One of the most powerful features of a programming language is the
ability to manipulate **variables**. A variable is a name that refers to
a value.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Assignment statements
[\[variables\]]{#variables label="variables"}

An **assignment statement** creates a new variable and gives it a value:

    >>> message = 'And now for something completely different'
    >>> n = 17
    >>> pi = 3.1415926535897932

This example makes three assignments. The first assigns a string to a
new variable named `message`; the second gives the integer `17` to `n`;
the third assigns the (approximate) value of $\pi$ to `pi`.

A common way to represent variables on paper is to write the name with
an arrow pointing to its value. This kind of figure is called a **state
diagram** because it shows what state each of the variables is in (think
of it as the variable's state of mind).
Figure [3.1](#fig.state2){reference-type="ref" reference="fig.state2"}
shows the result of the previous example.

![State diagram.[]{label="fig.state2"}](figs/state2.pdf){#fig.state2}

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Variable names

Programmers generally choose names for their variables that are
meaningful---they document what the variable is used for.

Variable names can be as long as you like. They can contain both letters
and numbers, but they can't begin with a number. It is legal to use
uppercase letters, but it is conventional to use only lower case for
variables names.

The underscore character, `_`, can appear in a name. It is often used in
names with multiple words, such as `your_name` or
`airspeed_of_unladen_swallow`.

If you give a variable an illegal name, you get a syntax error:

    >>> 76trombones = 'big parade'
    SyntaxError: invalid syntax
    >>> more@ = 1000000
    SyntaxError: invalid syntax
    >>> class = 'Advanced Theoretical Zymurgy'
    SyntaxError: invalid syntax

`76trombones` is illegal because it begins with a number. `more@` is
illegal because it contains an illegal character, ` @`. But what's wrong
with `class`?

It turns out that `class` is one of Python's **keywords**. The
interpreter uses keywords to recognize the structure of the program, and
they cannot be used as variable names.

Python 3 has these keywords:

    False      class      finally    is         return
    None       continue   for        lambda     try
    True       def        from       nonlocal   while
    and        del        global     not        with
    as         elif       if         or         yield
    assert     else       import     pass
    break      except     in         raise

You don't have to memorize this list. In most development environments,
keywords are displayed in a different color; if you try to use one as a
variable name, you'll know.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Expressions and statements

An **expression** is a combination of values, variables, and operators.
A value all by itself is considered an expression, and so is a variable,
so the following are all legal expressions:

    >>> 42
    42
    >>> n
    17
    >>> n + 25
    42

When you type an expression at the prompt, the interpreter **evaluates**
it, which means that it finds the value of the expression. In this
example, `n` has the value 17 and `n + 25` has the value 42.

A **statement** is a unit of code that has an effect, like creating a
variable or displaying a value.

    >>> n = 17
    >>> print(n)

The first line is an assignment statement that gives a value to `n`. The
second line is a print statement that displays the value of `n`.

When you type a statement, the interpreter **executes** it, which means
that it does whatever the statement says. In general, statements don't
have values.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Script mode

So far we have run Python in **interactive mode**, which means that you
interact directly with the interpreter. Interactive mode is a good way
to get started, but if you are working with more than a few lines of
code, it can be clumsy.

The alternative is to save code in a file called a **script** and then
run the interpreter in **script mode** to execute the script. By
convention, Python scripts have names that end with `.py`.

If you know how to create and run a script on your computer, you are
ready to go. Otherwise I recommend using PythonAnywhere again. I have
posted instructions for running in script mode at
<http://tinyurl.com/thinkpython2e>.

Because Python provides both modes, you can test bits of code in
interactive mode before you put them in a script. But there are
differences between interactive mode and script mode that can be
confusing.

For example, if you are using Python as a calculator, you might type

    >>> miles = 26.2
    >>> miles * 1.61
    42.182

The first line assigns a value to `miles`, but it has no visible effect.
The second line is an expression, so the interpreter evaluates it and
displays the result. It turns out that a marathon is about 42
kilometers.

But if you type the same code into a script and run it, you get no
output at all. In script mode an expression, all by itself, has no
visible effect. Python evaluates the expression, but it doesn't display
the result. To display the result, you need a `print` statement like
this:

    miles = 26.2
    print(miles * 1.61)

This behavior can be confusing at first. To check your understanding,
type the following statements in the Python interpreter and see what
they do:

    5
    x = 5
    x + 1

Now put the same statements in a script and run it. What is the output?
Modify the script by transforming each expression into a print statement
and then run it again.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Order of operations

When an expression contains more than one operator, the order of
evaluation depends on the **order of operations**. For mathematical
operators, Python follows mathematical convention. The acronym
**PEMDAS** is a useful way to remember the rules:

-   **P**arentheses have the highest precedence and can be used to force
    an expression to evaluate in the order you want. Since expressions
    in parentheses are evaluated first, `2 * (3-1)` is 4, and
    `(1+1)**(5-2)` is 8. You can also use parentheses to make an
    expression easier to read, as in `(minute * 100) / 60`, even if it
    doesn't change the result.

-   **E**xponentiation has the next highest precedence, so `1 + 2**3` is
    9, not 27, and `2 * 3**2` is 18, not 36.

-   **M**ultiplication and **D**ivision have higher precedence than
    **A**ddition and **S**ubtraction. So `2*3-1` is 5, not 4, and
    `6+4/2` is 8, not 5.

-   Operators with the same precedence are evaluated from left to right
    (except exponentiation). So in the expression `degrees / 2 * pi`,
    the division happens first and the result is multiplied by `pi`. To
    divide by $2 \pi$, you can use parentheses or write
    `degrees / 2 / pi`.

I don't work very hard to remember the precedence of operators. If I
can't tell by looking at the expression, I use parentheses to make it
obvious.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex String operations

In general, you can't perform mathematical operations on strings, even
if the strings look like numbers, so the following are illegal:

    'chinese'-'food'    'eggs'/'easy'    'third'*'a charm'

But there are two exceptions, `+` and ``.

The `+` operator performs **string concatenation**, which means it joins
the strings by linking them end-to-end. For example:

    >>> first = 'throat'
    >>> second = 'warbler'
    >>> first + second
    throatwarbler

The `` operator also works on strings; it performs repetition. For
example, `'Spam'*3` is `'SpamSpamSpam'`. If one of the values is a
string, the other has to be an integer.

This use of `+` and `` makes sense by analogy with addition and
multiplication. Just as `4*3` is equivalent to `4+4+4`, we expect
`'Spam'*3` to be the same as `'Spam'+'Spam'+'Spam'`, and it is. On the
other hand, there is a significant way in which string concatenation and
repetition are different from integer addition and multiplication. Can
you think of a property that addition has that string concatenation does
not?

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Comments

As programs get bigger and more complicated, they get more difficult to
read. Formal languages are dense, and it is often difficult to look at a
piece of code and figure out what it is doing, or why.

For this reason, it is a good idea to add notes to your programs to
explain in natural language what the program is doing. These notes are
called **comments**, and they start with the `#` symbol:

    # compute the percentage of the hour that has elapsed
    percentage = (minute * 100) / 60

In this case, the comment appears on a line by itself. You can also put
comments at the end of a line:

    percentage = (minute * 100) / 60     # percentage of an hour

Everything from the `#` to the end of the line is ignored---it has no
effect on the execution of the program.

Comments are most useful when they document non-obvious features of the
code. It is reasonable to assume that the reader can figure out *what*
the code does; it is more useful to explain *why*.

This comment is redundant with the code and useless:

    v = 5     # assign 5 to v

This comment contains useful information that is not in the code:

    v = 5     # velocity in meters/second. 

Good variable names can reduce the need for comments, but long names can
make complex expressions hard to read, so there is a tradeoff.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Debugging

Three kinds of errors can occur in a program: syntax errors, runtime
errors, and semantic errors. It is useful to distinguish between them in
order to track them down more quickly.

Syntax error:

:   "Syntax" refers to the structure of a program and the rules about
    that structure. For example, parentheses have to come in matching
    pairs, so `(1 + 2)` is legal, but `8)` is a **syntax error**.

    If there is a syntax error anywhere in your program, Python displays
    an error message and quits, and you will not be able to run the
    program. During the first few weeks of your programming career, you
    might spend a lot of time tracking down syntax errors. As you gain
    experience, you will make fewer errors and find them faster.

Runtime error:

:   The second type of error is a runtime error, so called because the
    error does not appear until after the program has started running.
    These errors are also called **exceptions** because they usually
    indicate that something exceptional (and bad) has happened.

    Runtime errors are rare in the simple programs you will see in the
    first few chapters, so it might be a while before you encounter one.

Semantic error:

:   The third type of error is "semantic", which means related to
    meaning. If there is a semantic error in your program, it will run
    without generating error messages, but it will not do the right
    thing. It will do something else. Specifically, it will do what you
    told it to do.

    Identifying semantic errors can be tricky because it requires you to
    work backward by looking at the output of the program and trying to
    figure out what it is doing.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Glossary

variable:

:   A name that refers to a value.

assignment:

:   A statement that assigns a value to a variable.

state diagram:

:   A graphical representation of a set of variables and the values they
    refer to.

keyword:

:   A reserved word that is used to parse a program; you cannot use
    keywords like `if`, `def`, and `while` as variable names.

operand:

:   One of the values on which an operator operates.

expression:

:   A combination of variables, operators, and values that represents a
    single result.

evaluate:

:   To simplify an expression by performing the operations in order to
    yield a single value.

statement:

:   A section of code that represents a command or action. So far, the
    statements we have seen are assignments and print statements.

execute:

:   To run a statement and do what it says.

interactive mode:

:   A way of using the Python interpreter by typing code at the prompt.

script mode:

:   A way of using the Python interpreter to read code from a script and
    run it.

script:

:   A program stored in a file.

order of operations:

:   Rules governing the order in which expressions involving multiple
    operators and operands are evaluated.

concatenate:

:   To join two operands end-to-end.

comment:

:   Information in a program that is meant for other programmers (or
    anyone reading the source code) and has no effect on the execution
    of the program.

syntax error:

:   An error in a program that makes it impossible to parse (and
    therefore impossible to interpret).

exception:

:   An error that is detected while the program is running.

semantics:

:   The meaning of a program.

semantic error:

:   An error in a program that makes it do something other than what the
    programmer intended.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

Repeating my advice from the previous chapter, whenever you learn a new
feature, you should try it out in interactive mode and make errors on
purpose to see what goes wrong.

-   We've seen that `n = 42` is legal. What about `42 = n`?

-   How about `x = y = 1`?

-   In some languages every statement ends with a semi-colon, `;`. What
    happens if you put a semi-colon at the end of a Python statement?

-   What if you put a period at the end of a statement?

-   In math notation you can multiply $x$ and $y$ like this: $x y$. What
    happens if you try that in Python?

Practice using the Python interpreter as a calculator:

1.  The volume of a sphere with radius $r$ is $\frac{4}{3} \pi r^3$.
    What is the volume of a sphere with radius 5?

2.  Suppose the cover price of a book is \$24.95, but bookstores get a
    40% discount. Shipping costs \$3 for the first copy and 75 cents for
    each additional copy. What is the total wholesale cost for 60
    copies?

3.  If I leave my house at 6:52 am and run 1 mile at an easy pace (8:15
    per mile), then 3 miles at tempo (7:12 per mile) and 1 mile at easy
    pace again, what time do I get home for breakfast?

Functions {#funcchap}
=========

In the context of programming, a **function** is a named sequence of
statements that performs a computation. When you define a function, you
specify the name and the sequence of statements. Later, you can "call"
the function by name.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Function calls
[\[functionchap\]]{#functionchap label="functionchap"}

We have already seen one example of a **function call**:

    >>> type(42)
    <class 'int'>

The name of the function is `type`. The expression in parentheses is
called the **argument** of the function. The result, for this function,
is the type of the argument.

It is common to say that a function "takes" an argument and "returns" a
result. The result is also called the **return value**.

Python provides functions that convert values from one type to another.
The `int` function takes any value and converts it to an integer, if it
can, or complains otherwise:

    >>> int('32')
    32
    >>> int('Hello')
    ValueError: invalid literal for int(): Hello

`int` can convert floating-point values to integers, but it doesn't
round off; it chops off the fraction part:

    >>> int(3.99999)
    3
    >>> int(-2.3)
    -2

`float` converts integers and strings to floating-point numbers:

    >>> float(32)
    32.0
    >>> float('3.14159')
    3.14159

Finally, `str` converts its argument to a string:

    >>> str(32)
    '32'
    >>> str(3.14159)
    '3.14159'

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Math functions

Python has a math module that provides most of the familiar mathematical
functions. A **module** is a file that contains a collection of related
functions.

Before we can use the functions in a module, we have to import it with
an **import statement**:

    >>> import math

This statement creates a **module object** named math. If you display
the module object, you get some information about it:

    >>> math
    <module 'math' (built-in)>

The module object contains the functions and variables defined in the
module. To access one of the functions, you have to specify the name of
the module and the name of the function, separated by a dot (also known
as a period). This format is called **dot notation**.

    >>> ratio = signal_power / noise_power
    >>> decibels = 10 * math.log10(ratio)

    >>> radians = 0.7
    >>> height = math.sin(radians)

The first example uses `math.log10` to compute a signal-to-noise ratio
in decibels (assuming that `signal_power` and `noise_power` are
defined). The math module also provides `log`, which computes logarithms
base `e`.

The second example finds the sine of `radians`. The variable name
`radians` is a hint that `sin` and the other trigonometric functions
(`cos`, `tan`, etc.) take arguments in radians. To convert from degrees
to radians, divide by 180 and multiply by $\pi$:

    >>> degrees = 45
    >>> radians = degrees / 180.0 * math.pi
    >>> math.sin(radians)
    0.707106781187

The expression `math.pi` gets the variable `pi` from the math module.
Its value is a floating-point approximation of $\pi$, accurate to about
15 digits.

If you know trigonometry, you can check the previous result by comparing
it to the square root of two, divided by two:

    >>> math.sqrt(2) / 2.0
    0.707106781187

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Composition

So far, we have looked at the elements of a program---variables,
expressions, and statements---in isolation, without talking about how to
combine them.

One of the most useful features of programming languages is their
ability to take small building blocks and **compose** them. For example,
the argument of a function can be any kind of expression, including
arithmetic operators:

    x = math.sin(degrees / 360.0 * 2 * math.pi)

And even function calls:

    x = math.exp(math.log(x+1))

Almost anywhere you can put a value, you can put an arbitrary
expression, with one exception: the left side of an assignment statement
has to be a variable name. Any other expression on the left side is a
syntax error (we will see exceptions to this rule later).

    >>> minutes = hours * 60                 # right
    >>> hours * 60 = minutes                 # wrong!
    SyntaxError: can't assign to operator

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Adding new functions

So far, we have only been using the functions that come with Python, but
it is also possible to add new functions. A **function definition**
specifies the name of a new function and the sequence of statements that
run when the function is called.

Here is an example:

    def print_lyrics():
        print("I'm a lumberjack, and I'm okay.")
        print("I sleep all night and I work all day.")

`def` is a keyword that indicates that this is a function definition.
The name of the function is `print_lyrics`. The rules for function names
are the same as for variable names: letters, numbers and underscore are
legal, but the first character can't be a number. You can't use a
keyword as the name of a function, and you should avoid having a
variable and a function with the same name.

The empty parentheses after the name indicate that this function doesn't
take any arguments.

The first line of the function definition is called the **header**; the
rest is called the **body**. The header has to end with a colon and the
body has to be indented. By convention, indentation is always four
spaces. The body can contain any number of statements.

The strings in the print statements are enclosed in double quotes.
Single quotes and double quotes do the same thing; most people use
single quotes except in cases like this where a single quote (which is
also an apostrophe) appears in the string.

All quotation marks (single and double) must be "straight quotes",
usually located next to Enter on the keyboard. "Curly quotes", like the
ones in this sentence, are not legal in Python.

If you type a function definition in interactive mode, the interpreter
prints dots (`...`) to let you know that the definition isn't complete:

    >>> def print_lyrics():
    ...     print("I'm a lumberjack, and I'm okay.")
    ...     print("I sleep all night and I work all day.")
    ...

To end the function, you have to enter an empty line.

Defining a function creates a **function object**, which has type
`function`:

    >>> print(print_lyrics)
    <function print_lyrics at 0xb7e99e9c>
    >>> type(print_lyrics)
    <class 'function'>

The syntax for calling the new function is the same as for built-in
functions:

    >>> print_lyrics()
    I'm a lumberjack, and I'm okay.
    I sleep all night and I work all day.

Once you have defined a function, you can use it inside another
function. For example, to repeat the previous refrain, we could write a
function called `repeat_lyrics`:

    def repeat_lyrics():
        print_lyrics()
        print_lyrics()

And then call `repeat_lyrics`:

    >>> repeat_lyrics()
    I'm a lumberjack, and I'm okay.
    I sleep all night and I work all day.
    I'm a lumberjack, and I'm okay.
    I sleep all night and I work all day.

But that's not really how the song goes.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Definitions and uses

Pulling together the code fragments from the previous section, the whole
program looks like this:

    def print_lyrics():
        print("I'm a lumberjack, and I'm okay.")
        print("I sleep all night and I work all day.")

    def repeat_lyrics():
        print_lyrics()
        print_lyrics()

    repeat_lyrics()

This program contains two function definitions: `print_lyrics` and
`repeat_lyrics`. Function definitions get executed just like other
statements, but the effect is to create function objects. The statements
inside the function do not run until the function is called, and the
function definition generates no output.

As you might expect, you have to create a function before you can run
it. In other words, the function definition has to run before the
function gets called.

As an exercise, move the last line of this program to the top, so the
function call appears before the definitions. Run the program and see
what error message you get.

Now move the function call back to the bottom and move the definition of
`print_lyrics` after the definition of `repeat_lyrics`. What happens
when you run this program?

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Flow of execution

To ensure that a function is defined before its first use, you have to
know the order statements run in, which is called the **flow of
execution**.

Execution always begins at the first statement of the program.
Statements are run one at a time, in order from top to bottom.

Function definitions do not alter the flow of execution of the program,
but remember that statements inside the function don't run until the
function is called.

A function call is like a detour in the flow of execution. Instead of
going to the next statement, the flow jumps to the body of the function,
runs the statements there, and then comes back to pick up where it left
off.

That sounds simple enough, until you remember that one function can call
another. While in the middle of one function, the program might have to
run the statements in another function. Then, while running that new
function, the program might have to run yet another function!

Fortunately, Python is good at keeping track of where it is, so each
time a function completes, the program picks up where it left off in the
function that called it. When it gets to the end of the program, it
terminates.

In summary, when you read a program, you don't always want to read from
top to bottom. Sometimes it makes more sense if you follow the flow of
execution.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Parameters and arguments
[\[parameters\]]{#parameters label="parameters"}

Some of the functions we have seen require arguments. For example, when
you call `math.sin` you pass a number as an argument. Some functions
take more than one argument: `math.pow` takes two, the base and the
exponent.

Inside the function, the arguments are assigned to variables called
**parameters**. Here is a definition for a function that takes an
argument:

    def print_twice(bruce):
        print(bruce)
        print(bruce)

This function assigns the argument to a parameter named `bruce`. When
the function is called, it prints the value of the parameter (whatever
it is) twice.

This function works with any value that can be printed.

    >>> print_twice('Spam')
    Spam
    Spam
    >>> print_twice(42)
    42
    42
    >>> print_twice(math.pi)
    3.14159265359
    3.14159265359

The same rules of composition that apply to built-in functions also
apply to programmer-defined functions, so we can use any kind of
expression as an argument for `print_twice`:

    >>> print_twice('Spam '*4)
    Spam Spam Spam Spam
    Spam Spam Spam Spam
    >>> print_twice(math.cos(math.pi))
    -1.0
    -1.0

The argument is evaluated before the function is called, so in the
examples the expressions `'Spam '*4` and `math.cos(math.pi)` are only
evaluated once.

You can also use a variable as an argument:

    >>> michael = 'Eric, the half a bee.'
    >>> print_twice(michael)
    Eric, the half a bee.
    Eric, the half a bee.

The name of the variable we pass as an argument (`michael`) has nothing
to do with the name of the parameter (`bruce`). It doesn't matter what
the value was called back home (in the caller); here in `print_twice`,
we call everybody `bruce`.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Variables and parameters are
local

When you create a variable inside a function, it is **local**, which
means that it only exists inside the function. For example:

    def cat_twice(part1, part2):
        cat = part1 + part2
        print_twice(cat)

This function takes two arguments, concatenates them, and prints the
result twice. Here is an example that uses it:

    >>> line1 = 'Bing tiddle '
    >>> line2 = 'tiddle bang.'
    >>> cat_twice(line1, line2)
    Bing tiddle tiddle bang.
    Bing tiddle tiddle bang.

When `cat_twice` terminates, the variable `cat` is destroyed. If we try
to print it, we get an exception:

    >>> print(cat)
    NameError: name 'cat' is not defined

Parameters are also local. For example, outside `print_twice`, there is
no such thing as `bruce`.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Stack diagrams
[\[stackdiagram\]]{#stackdiagram label="stackdiagram"}

To keep track of which variables can be used where, it is sometimes
useful to draw a **stack diagram**. Like state diagrams, stack diagrams
show the value of each variable, but they also show the function each
variable belongs to.

Each function is represented by a **frame**. A frame is a box with the
name of a function beside it and the parameters and variables of the
function inside it. The stack diagram for the previous example is shown
in Figure [4.1](#fig.stack){reference-type="ref" reference="fig.stack"}.

![Stack diagram.[]{label="fig.stack"}](figs/stack.pdf){#fig.stack}

The frames are arranged in a stack that indicates which function called
which, and so on. In this example, `print_twice` was called by
`cat_twice`, and `cat_twice` was called by `__main__`, which is a
special name for the topmost frame. When you create a variable outside
of any function, it belongs to `__main__`.

Each parameter refers to the same value as its corresponding argument.
So, `part1` has the same value as `line1`, `part2` has the same value as
`line2`, and `bruce` has the same value as `cat`.

If an error occurs during a function call, Python prints the name of the
function, the name of the function that called it, and the name of the
function that called *that*, all the way back to `__main__`.

For example, if you try to access `cat` from within `print_twice`, you
get a `NameError`:

    Traceback (innermost last):
      File "test.py", line 13, in __main__
        cat_twice(line1, line2)
      File "test.py", line 5, in cat_twice
        print_twice(cat)
      File "test.py", line 9, in print_twice
        print(cat)
    NameError: name 'cat' is not defined

This list of functions is called a **traceback**. It tells you what
program file the error occurred in, and what line, and what functions
were executing at the time. It also shows the line of code that caused
the error.

The order of the functions in the traceback is the same as the order of
the frames in the stack diagram. The function that is currently running
is at the bottom.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Fruitful functions and void
functions

Some of the functions we have used, such as the math functions, return
results; for lack of a better name, I call them **fruitful functions**.
Other functions, like `print_twice`, perform an action but don't return
a value. They are called **void functions**.

When you call a fruitful function, you almost always want to do
something with the result; for example, you might assign it to a
variable or use it as part of an expression:

    x = math.cos(radians)
    golden = (math.sqrt(5) + 1) / 2

When you call a function in interactive mode, Python displays the
result:

    >>> math.sqrt(5)
    2.2360679774997898

But in a script, if you call a fruitful function all by itself, the
return value is lost forever!

    math.sqrt(5)

This script computes the square root of 5, but since it doesn't store or
display the result, it is not very useful.

Void functions might display something on the screen or have some other
effect, but they don't have a return value. If you assign the result to
a variable, you get a special value called `None`.

    >>> result = print_twice('Bing')
    Bing
    Bing
    >>> print(result)
    None

The value `None` is not the same as the string `'None'`. It is a special
value that has its own type:

    >>> type(None)
    <class 'NoneType'>

The functions we have written so far are all void. We will start writing
fruitful functions in a few chapters.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Why functions?

It may not be clear why it is worth the trouble to divide a program into
functions. There are several reasons:

-   Creating a new function gives you an opportunity to name a group of
    statements, which makes your program easier to read and debug.

-   Functions can make a program smaller by eliminating repetitive code.
    Later, if you make a change, you only have to make it in one place.

-   Dividing a long program into functions allows you to debug the parts
    one at a time and then assemble them into a working whole.

-   Well-designed functions are often useful for many programs. Once you
    write and debug one, you can reuse it.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Debugging

One of the most important skills you will acquire is debugging. Although
it can be frustrating, debugging is one of the most intellectually rich,
challenging, and interesting parts of programming.

In some ways debugging is like detective work. You are confronted with
clues and you have to infer the processes and events that led to the
results you see.

Debugging is also like an experimental science. Once you have an idea
about what is going wrong, you modify your program and try again. If
your hypothesis was correct, you can predict the result of the
modification, and you take a step closer to a working program. If your
hypothesis was wrong, you have to come up with a new one. As Sherlock
Holmes pointed out, "When you have eliminated the impossible, whatever
remains, however improbable, must be the truth." (A. Conan Doyle, *The
Sign of Four*)

For some people, programming and debugging are the same thing. That is,
programming is the process of gradually debugging a program until it
does what you want. The idea is that you should start with a working
program and make small modifications, debugging them as you go.

For example, Linux is an operating system that contains millions of
lines of code, but it started out as a simple program Linus Torvalds
used to explore the Intel 80386 chip. According to Larry Greenfield,
"One of Linus's earlier projects was a program that would switch between
printing AAAA and BBBB. This later evolved to Linux." (*The Linux Users'
Guide* Beta Version 1).

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Glossary

function:

:   A named sequence of statements that performs some useful operation.
    Functions may or may not take arguments and may or may not produce a
    result.

function definition:

:   A statement that creates a new function, specifying its name,
    parameters, and the statements it contains.

function object:

:   A value created by a function definition. The name of the function
    is a variable that refers to a function object.

header:

:   The first line of a function definition.

body:

:   The sequence of statements inside a function definition.

parameter:

:   A name used inside a function to refer to the value passed as an
    argument.

function call:

:   A statement that runs a function. It consists of the function name
    followed by an argument list in parentheses.

argument:

:   A value provided to a function when the function is called. This
    value is assigned to the corresponding parameter in the function.

local variable:

:   A variable defined inside a function. A local variable can only be
    used inside its function.

return value:

:   The result of a function. If a function call is used as an
    expression, the return value is the value of the expression.

fruitful function:

:   A function that returns a value.

void function:

:   A function that always returns `None`.

`None`:

:   A special value returned by void functions.

module:

:   A file that contains a collection of related functions and other
    definitions.

import statement:

:   A statement that reads a module file and creates a module object.

module object:

:   A value created by an `import` statement that provides access to the
    values defined in a module.

dot notation:

:   The syntax for calling a function in another module by specifying
    the module name followed by a dot (period) and the function name.

composition:

:   Using an expression as part of a larger expression, or a statement
    as part of a larger statement.

flow of execution:

:   The order statements run in.

stack diagram:

:   A graphical representation of a stack of functions, their variables,
    and the values they refer to.

frame:

:   A box in a stack diagram that represents a function call. It
    contains the local variables and parameters of the function.

traceback:

:   A list of the functions that are executing, printed when an
    exception occurs.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

Write a function named `right_justify` that takes a string named `s` as
a parameter and prints the string with enough leading spaces so that the
last letter of the string is in column 70 of the display.

    >>> right_justify('monty')
                                                                     monty

Hint: Use string concatenation and repetition. Also, Python provides a
built-in function called `len` that returns the length of a string, so
the value of `len('monty')` is 5.

A function object is a value you can assign to a variable or pass as an
argument. For example, `do_twice` is a function that takes a function
object as an argument and calls it twice:

    def do_twice(f):
        f()
        f()

Here's an example that uses `do_twice` to call a function named
`print_spam` twice.

    def print_spam():
        print('spam')

    do_twice(print_spam)

1.  Type this example into a script and test it.

2.  Modify `do_twice` so that it takes two arguments, a function object
    and a value, and calls the function twice, passing the value as an
    argument.

3.  Copy the definition of `print_twice` from earlier in this chapter to
    your script.

4.  Use the modified version of `do_twice` to call `print_twice` twice,
    passing `'spam'` as an argument.

5.  Define a new function called `do_four` that takes a function object
    and a value and calls the function four times, passing the value as
    a parameter. There should be only two statements in the body of this
    function, not four.

Solution: <http://thinkpython2.com/code/do_four.py>.

Note: This exercise should be done using only the statements and other
features we have learned so far.

1.  Write a function that draws a grid like the following:

        + - - - - + - - - - +
        |         |         |
        |         |         |
        |         |         |
        |         |         |
        + - - - - + - - - - +
        |         |         |
        |         |         |
        |         |         |
        |         |         |
        + - - - - + - - - - +

    Hint: to print more than one value on a line, you can print a
    comma-separated sequence of values:

        print('+', '-')

    By default, `print` advances to the next line, but you can override
    that behavior and put a space at the end, like this:

        print('+', end=' ')
        print('-')

    The output of these statements is `'+ -'` on the same line. The
    output from the next print statement would begin on the next line.

2.  Write a function that draws a similar grid with four rows and four
    columns.

Solution: <http://thinkpython2.com/code/grid.py>. Credit: This exercise
is based on an exercise in Oualline, *Practical C Programming, Third
Edition*, O'Reilly Media, 1997.

Case study: interface design {#turtlechap}
============================

This chapter presents a case study that demonstrates a process for
designing functions that work together.

It introduces the `turtle` module, which allows you to create images
using turtle graphics. The `turtle` module is included in most Python
installations, but if you are running Python using PythonAnywhere, you
won't be able to run the turtle examples (at least you couldn't when I
wrote this).

If you have already installed Python on your computer, you should be
able to run the examples. Otherwise, now is a good time to install. I
have posted instructions at <http://tinyurl.com/thinkpython2e>.

Code examples from this chapter are available from
<http://thinkpython2.com/code/polygon.py>.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex The turtle module
[\[turtle\]]{#turtle label="turtle"}

To check whether you have the `turtle` module, open the Python
interpreter and type

    >>> import turtle
    >>> bob = turtle.Turtle()

When you run this code, it should create a new window with small arrow
that represents the turtle. Close the window.

Create a file named `mypolygon.py` and type in the following code:

    import turtle
    bob = turtle.Turtle()
    print(bob)
    turtle.mainloop()

The `turtle` module (with a lowercase 't') provides a function called
`Turtle` (with an uppercase 'T') that creates a Turtle object, which we
assign to a variable named `bob`. Printing `bob` displays something
like:

    <turtle.Turtle object at 0xb7bfbf4c>

This means that `bob` refers to an object with type `Turtle` as defined
in module `turtle`.

`mainloop` tells the window to wait for the user to do something,
although in this case there's not much for the user to do except close
the window.

Once you create a Turtle, you can call a **method** to move it around
the window. A method is similar to a function, but it uses slightly
different syntax. For example, to move the turtle forward:

    bob.fd(100)

The method, `fd`, is associated with the turtle object we're calling
`bob`. Calling a method is like making a request: you are asking `bob`
to move forward.

The argument of `fd` is a distance in pixels, so the actual size depends
on your display.

Other methods you can call on a Turtle are `bk` to move backward, `lt`
for left turn, and `rt` right turn. The argument for `lt` and `rt` is an
angle in degrees.

Also, each Turtle is holding a pen, which is either down or up; if the
pen is down, the Turtle leaves a trail when it moves. The methods `pu`
and `pd` stand for "pen up" and "pen down".

To draw a right angle, add these lines to the program (after creating
`bob` and before calling `mainloop`):

    bob.fd(100)
    bob.lt(90)
    bob.fd(100)

When you run this program, you should see `bob` move east and then
north, leaving two line segments behind.

Now modify the program to draw a square. Don't go on until you've got it
working!

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Simple repetition
[\[repetition\]]{#repetition label="repetition"}

Chances are you wrote something like this:

    bob.fd(100)
    bob.lt(90)

    bob.fd(100)
    bob.lt(90)

    bob.fd(100)
    bob.lt(90)

    bob.fd(100)

We can do the same thing more concisely with a `for` statement. Add this
example to `mypolygon.py` and run it again:

    for i in range(4):
        print('Hello!')

You should see something like this:

    Hello!
    Hello!
    Hello!
    Hello!

This is the simplest use of the `for` statement; we will see more later.
But that should be enough to let you rewrite your square-drawing
program. Don't go on until you do.

Here is a `for` statement that draws a square:

    for i in range(4):
        bob.fd(100)
        bob.lt(90)

The syntax of a `for` statement is similar to a function definition. It
has a header that ends with a colon and an indented body. The body can
contain any number of statements.

A `for` statement is also called a **loop** because the flow of
execution runs through the body and then loops back to the top. In this
case, it runs the body four times.

This version is actually a little different from the previous
square-drawing code because it makes another turn after drawing the last
side of the square. The extra turn takes more time, but it simplifies
the code if we do the same thing every time through the loop. This
version also has the effect of leaving the turtle back in the starting
position, facing in the starting direction.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

The following is a series of exercises using the `turtle` module. They
are meant to be fun, but they have a point, too. While you are working
on them, think about what the point is.

The following sections have solutions to the exercises, so don't look
until you have finished (or at least tried).

1.  Write a function called `square` that takes a parameter named `t`,
    which is a turtle. It should use the turtle to draw a square.

    Write a function call that passes `bob` as an argument to `square`,
    and then run the program again.

2.  Add another parameter, named `length`, to `square`. Modify the body
    so length of the sides is `length`, and then modify the function
    call to provide a second argument. Run the program again. Test your
    program with a range of values for ` length`.

3.  Make a copy of `square` and change the name to ` polygon`. Add
    another parameter named `n` and modify the body so it draws an
    n-sided regular polygon. Hint: The exterior angles of an n-sided
    regular polygon are $360/n$ degrees.

4.  Write a function called `circle` that takes a turtle, `t`, and
    radius, `r`, as parameters and that draws an approximate circle by
    calling `polygon` with an appropriate length and number of sides.
    Test your function with a range of values of `r`.

    Hint: figure out the circumference of the circle and make sure that
    `length * n = circumference`.

5.  Make a more general version of `circle` called `arc` that takes an
    additional parameter `angle`, which determines what fraction of a
    circle to draw. `angle` is in units of degrees, so when `angle=360`,
    `arc` should draw a complete circle.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Encapsulation

The first exercise asks you to put your square-drawing code into a
function definition and then call the function, passing the turtle as a
parameter. Here is a solution:

    def square(t):
        for i in range(4):
            t.fd(100)
            t.lt(90)

    square(bob)

The innermost statements, `fd` and `lt` are indented twice to show that
they are inside the `for` loop, which is inside the function definition.
The next line, `square(bob)`, is flush with the left margin, which
indicates the end of both the `for` loop and the function definition.

Inside the function, `t` refers to the same turtle `bob`, so `t.lt(90)`
has the same effect as `bob.lt(90)`. In that case, why not call the
parameter `bob`? The idea is that `t` can be any turtle, not just `bob`,
so you could create a second turtle and pass it as an argument to
`square`:

    alice = turtle.Turtle()
    square(alice)

Wrapping a piece of code up in a function is called **encapsulation**.
One of the benefits of encapsulation is that it attaches a name to the
code, which serves as a kind of documentation. Another advantage is that
if you re-use the code, it is more concise to call a function twice than
to copy and paste the body!

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Generalization

The next step is to add a `length` parameter to `square`. Here is a
solution:

    def square(t, length):
        for i in range(4):
            t.fd(length)
            t.lt(90)

    square(bob, 100)

Adding a parameter to a function is called **generalization** because it
makes the function more general: in the previous version, the square is
always the same size; in this version it can be any size.

The next step is also a generalization. Instead of drawing squares,
`polygon` draws regular polygons with any number of sides. Here is a
solution:

    def polygon(t, n, length):
        angle = 360 / n
        for i in range(n):
            t.fd(length)
            t.lt(angle)

    polygon(bob, 7, 70)

This example draws a 7-sided polygon with side length 70.

If you are using Python 2, the value of `angle` might be off because of
integer division. A simple solution is to compute `angle = 360.0 / n`.
Because the numerator is a floating-point number, the result is floating
point.

When a function has more than a few numeric arguments, it is easy to
forget what they are, or what order they should be in. In that case it
is often a good idea to include the names of the parameters in the
argument list:

    polygon(bob, n=7, length=70)

These are called **keyword arguments** because they include the
parameter names as "keywords" (not to be confused with Python keywords
like `while` and `def`).

This syntax makes the program more readable. It is also a reminder about
how arguments and parameters work: when you call a function, the
arguments are assigned to the parameters.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Interface design

The next step is to write `circle`, which takes a radius, `r`, as a
parameter. Here is a simple solution that uses `polygon` to draw a
50-sided polygon:

    import math

    def circle(t, r):
        circumference = 2 * math.pi * r
        n = 50
        length = circumference / n
        polygon(t, n, length)

The first line computes the circumference of a circle with radius `r`
using the formula $2 \pi r$. Since we use `math.pi`, we have to import
`math`. By convention, `import` statements are usually at the beginning
of the script.

`n` is the number of line segments in our approximation of a circle, so
`length` is the length of each segment. Thus, `polygon` draws a 50-sided
polygon that approximates a circle with radius `r`.

One limitation of this solution is that `n` is a constant, which means
that for very big circles, the line segments are too long, and for small
circles, we waste time drawing very small segments. One solution would
be to generalize the function by taking `n` as a parameter. This would
give the user (whoever calls `circle`) more control, but the interface
would be less clean.

The **interface** of a function is a summary of how it is used: what are
the parameters? What does the function do? And what is the return value?
An interface is "clean" if it allows the caller to do what they want
without dealing with unnecessary details.

In this example, `r` belongs in the interface because it specifies the
circle to be drawn. `n` is less appropriate because it pertains to the
details of *how* the circle should be rendered.

Rather than clutter up the interface, it is better to choose an
appropriate value of `n` depending on `circumference`:

    def circle(t, r):
        circumference = 2 * math.pi * r
        n = int(circumference / 3) + 3
        length = circumference / n
        polygon(t, n, length)

Now the number of segments is an integer near `circumference/3`, so the
length of each segment is approximately 3, which is small enough that
the circles look good, but big enough to be efficient, and acceptable
for any size circle.

Adding 3 to `n` guarantees that the polygon has at least 3 sides.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Refactoring
[\[refactoring\]]{#refactoring label="refactoring"}

When I wrote `circle`, I was able to re-use `polygon` because a
many-sided polygon is a good approximation of a circle. But `arc` is not
as cooperative; we can't use `polygon` or `circle` to draw an arc.

One alternative is to start with a copy of `polygon` and transform it
into `arc`. The result might look like this:

    def arc(t, r, angle):
        arc_length = 2 * math.pi * r * angle / 360
        n = int(arc_length / 3) + 1
        step_length = arc_length / n
        step_angle = angle / n
        
        for i in range(n):
            t.fd(step_length)
            t.lt(step_angle)

The second half of this function looks like `polygon`, but we can't
re-use `polygon` without changing the interface. We could generalize
`polygon` to take an angle as a third argument, but then `polygon` would
no longer be an appropriate name! Instead, let's call the more general
function `polyline`:

    def polyline(t, n, length, angle):
        for i in range(n):
            t.fd(length)
            t.lt(angle)

Now we can rewrite `polygon` and `arc` to use `polyline`:

    def polygon(t, n, length):
        angle = 360.0 / n
        polyline(t, n, length, angle)

    def arc(t, r, angle):
        arc_length = 2 * math.pi * r * angle / 360
        n = int(arc_length / 3) + 1
        step_length = arc_length / n
        step_angle = float(angle) / n
        polyline(t, n, step_length, step_angle)

Finally, we can rewrite `circle` to use `arc`:

    def circle(t, r):
        arc(t, r, 360)

This process---rearranging a program to improve interfaces and
facilitate code re-use---is called **refactoring**. In this case, we
noticed that there was similar code in `arc` and `polygon`, so we
"factored it out" into `polyline`.

If we had planned ahead, we might have written `polyline` first and
avoided refactoring, but often you don't know enough at the beginning of
a project to design all the interfaces. Once you start coding, you
understand the problem better. Sometimes refactoring is a sign that you
have learned something.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex A development plan

A **development plan** is a process for writing programs. The process we
used in this case study is "encapsulation and generalization". The steps
of this process are:

1.  Start by writing a small program with no function definitions.

2.  Once you get the program working, identify a coherent piece of it,
    encapsulate the piece in a function and give it a name.

3.  Generalize the function by adding appropriate parameters.

4.  Repeat steps 1--3 until you have a set of working functions. Copy
    and paste working code to avoid retyping (and re-debugging).

5.  Look for opportunities to improve the program by refactoring. For
    example, if you have similar code in several places, consider
    factoring it into an appropriately general function.

This process has some drawbacks---we will see alternatives later---but
it can be useful if you don't know ahead of time how to divide the
program into functions. This approach lets you design as you go along.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex docstring
[\[docstring\]]{#docstring label="docstring"}

A **docstring** is a string at the beginning of a function that explains
the interface ("doc" is short for "documentation"). Here is an example:

    def polyline(t, n, length, angle):
        """Draws n line segments with the given length and
        angle (in degrees) between them.  t is a turtle.
        """    
        for i in range(n):
            t.fd(length)
            t.lt(angle)

By convention, all docstrings are triple-quoted strings, also known as
multiline strings because the triple quotes allow the string to span
more than one line.

It is terse, but it contains the essential information someone would
need to use this function. It explains concisely what the function does
(without getting into the details of how it does it). It explains what
effect each parameter has on the behavior of the function and what type
each parameter should be (if it is not obvious).

Writing this kind of documentation is an important part of interface
design. A well-designed interface should be simple to explain; if you
have a hard time explaining one of your functions, maybe the interface
could be improved.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Debugging

An interface is like a contract between a function and a caller. The
caller agrees to provide certain parameters and the function agrees to
do certain work.

For example, `polyline` requires four arguments: `t` has to be a Turtle;
`n` has to be an integer; `length` should be a positive number; and
` angle` has to be a number, which is understood to be in degrees.

These requirements are called **preconditions** because they are
supposed to be true before the function starts executing. Conversely,
conditions at the end of the function are **postconditions**.
Postconditions include the intended effect of the function (like drawing
line segments) and any side effects (like moving the Turtle or making
other changes).

Preconditions are the responsibility of the caller. If the caller
violates a (properly documented!) precondition and the function doesn't
work correctly, the bug is in the caller, not the function.

If the preconditions are satisfied and the postconditions are not, the
bug is in the function. If your pre- and postconditions are clear, they
can help with debugging.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Glossary

method:

:   A function that is associated with an object and called using dot
    notation.

loop:

:   A part of a program that can run repeatedly.

encapsulation:

:   The process of transforming a sequence of statements into a function
    definition.

generalization:

:   The process of replacing something unnecessarily specific (like a
    number) with something appropriately general (like a variable or
    parameter).

keyword argument:

:   An argument that includes the name of the parameter as a "keyword".

interface:

:   A description of how to use a function, including the name and
    descriptions of the arguments and return value.

refactoring:

:   The process of modifying a working program to improve function
    interfaces and other qualities of the code.

development plan:

:   A process for writing programs.

docstring:

:   A string that appears at the top of a function definition to
    document the function's interface.

precondition:

:   A requirement that should be satisfied by the caller before a
    function starts.

postcondition:

:   A requirement that should be satisfied by the function before it
    ends.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

Download the code in this chapter from
<http://thinkpython2.com/code/polygon.py>.

1.  Draw a stack diagram that shows the state of the program while
    executing `circle(bob, radius)`. You can do the arithmetic by hand
    or add `print` statements to the code.

2.  The version of `arc` in
    Section [\[refactoring\]](#refactoring){reference-type="ref"
    reference="refactoring"} is not very accurate because the linear
    approximation of the circle is always outside the true circle. As a
    result, the Turtle ends up a few pixels away from the correct
    destination. My solution shows a way to reduce the effect of this
    error. Read the code and see if it makes sense to you. If you draw a
    diagram, you might see how it works.

![Turtle
flowers.[]{label="fig.flowers"}](figs/flowers.pdf){#fig.flowers}

Write an appropriately general set of functions that can draw flowers as
in Figure [5.1](#fig.flowers){reference-type="ref"
reference="fig.flowers"}.

Solution: <http://thinkpython2.com/code/flower.py>, also requires
<http://thinkpython2.com/code/polygon.py>.

![Turtle pies.[]{label="fig.pies"}](figs/pies.pdf){#fig.pies}

Write an appropriately general set of functions that can draw shapes as
in Figure [5.2](#fig.pies){reference-type="ref" reference="fig.pies"}.

Solution: <http://thinkpython2.com/code/pie.py>.

The letters of the alphabet can be constructed from a moderate number of
basic elements, like vertical and horizontal lines and a few curves.
Design an alphabet that can be drawn with a minimal number of basic
elements and then write functions that draw the letters.

You should write one function for each letter, with names `draw_a`,
`draw_b`, etc., and put your functions in a file named `letters.py`. You
can download a "turtle typewriter" from
<http://thinkpython2.com/code/typewriter.py> to help you test your code.

You can get a solution from <http://thinkpython2.com/code/letters.py>;
it also requires <http://thinkpython2.com/code/polygon.py>.

Read about spirals at <http://en.wikipedia.org/wiki/Spiral>; then write
a program that draws an Archimedian spiral (or one of the other kinds).
Solution: <http://thinkpython2.com/code/spiral.py>.

Conditionals and recursion
==========================

The main topic of this chapter is the `if` statement, which executes
different code depending on the state of the program. But first I want
to introduce two new operators: floor division and modulus.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Floor division and modulus

The **floor division** operator, `//`, divides two numbers and rounds
down to an integer. For example, suppose the run time of a movie is 105
minutes. You might want to know how long that is in hours. Conventional
division returns a floating-point number:

    >>> minutes = 105
    >>> minutes / 60
    1.75

But we don't normally write hours with decimal points. Floor division
returns the integer number of hours, rounding down:

    >>> minutes = 105
    >>> hours = minutes // 60
    >>> hours
    1

To get the remainder, you could subtract off one hour in minutes:

    >>> remainder = minutes - hours * 60
    >>> remainder
    45

An alternative is to use the **modulus operator**, `%`, which divides
two numbers and returns the remainder.

    >>> remainder = minutes % 60
    >>> remainder
    45

The modulus operator is more useful than it seems. For example, you can
check whether one number is divisible by another---if `x % y` is zero,
then `x` is divisible by `y`.

Also, you can extract the right-most digit or digits from a number. For
example, `x % 10` yields the right-most digit of `x` (in base 10).
Similarly `x % 100` yields the last two digits.

If you are using Python 2, division works differently. The division
operator, `/`, performs floor division if both operands are integers,
and floating-point division if either operand is a `float`.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Boolean expressions

A **boolean expression** is an expression that is either true or false.
The following examples use the operator `==`, which compares two
operands and produces `True` if they are equal and `False` otherwise:

    >>> 5 == 5
    True
    >>> 5 == 6
    False

`True` and `False` are special values that belong to the type `bool`;
they are not strings:

    >>> type(True)
    <class 'bool'>
    >>> type(False)
    <class 'bool'>

The `==` operator is one of the **relational operators**; the others
are:

          x != y               # x is not equal to y
          x > y                # x is greater than y
          x < y                # x is less than y
          x >= y               # x is greater than or equal to y
          x <= y               # x is less than or equal to y

Although these operations are probably familiar to you, the Python
symbols are different from the mathematical symbols. A common error is
to use a single equal sign (`=`) instead of a double equal sign (`==`).
Remember that `=` is an assignment operator and `==` is a relational
operator. There is no such thing as `=<` or `=>`.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Logical operators

There are three **logical operators**: `and`, ` or`, and `not`. The
semantics (meaning) of these operators is similar to their meaning in
English. For example, `x > 0 and x < 10` is true only if `x` is greater
than 0 *and* less than 10.

`n%2 == 0 or n%3 == 0` is true if *either or both* of the conditions is
true, that is, if the number is divisible by 2 *or* 3.

Finally, the `not` operator negates a boolean expression, so
`not (x > y)` is true if `x > y` is false, that is, if `x` is less than
or equal to `y`.

Strictly speaking, the operands of the logical operators should be
boolean expressions, but Python is not very strict. Any nonzero number
is interpreted as `True`:

    >>> 42 and True
    True

This flexibility can be useful, but there are some subtleties to it that
might be confusing. You might want to avoid it (unless you know what you
are doing).

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Conditional execution
[\[conditional.execution\]]{#conditional.execution
label="conditional.execution"}

In order to write useful programs, we almost always need the ability to
check conditions and change the behavior of the program accordingly.
**Conditional statements** give us this ability. The simplest form is
the `if` statement:

    if x > 0:
        print('x is positive')

The boolean expression after `if` is called the **condition**. If it is
true, the indented statement runs. If not, nothing happens.

`if` statements have the same structure as function definitions: a
header followed by an indented body. Statements like this are called
**compound statements**.

There is no limit on the number of statements that can appear in the
body, but there has to be at least one. Occasionally, it is useful to
have a body with no statements (usually as a place keeper for code you
haven't written yet). In that case, you can use the `pass` statement,
which does nothing.

    if x < 0:
        pass          # TODO: need to handle negative values!

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Alternative execution
[\[alternative.execution\]]{#alternative.execution
label="alternative.execution"}

A second form of the `if` statement is "alternative execution", in which
there are two possibilities and the condition determines which one runs.
The syntax looks like this:

    if x % 2 == 0:
        print('x is even')
    else:
        print('x is odd')

If the remainder when `x` is divided by 2 is 0, then we know that `x` is
even, and the program displays an appropriate message. If the condition
is false, the second set of statements runs. Since the condition must be
true or false, exactly one of the alternatives will run. The
alternatives are called **branches**, because they are branches in the
flow of execution.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Chained conditionals

Sometimes there are more than two possibilities and we need more than
two branches. One way to express a computation like that is a **chained
conditional**:

    if x < y:
        print('x is less than y')
    elif x > y:
        print('x is greater than y')
    else:
        print('x and y are equal')

`elif` is an abbreviation of "else if". Again, exactly one branch will
run. There is no limit on the number of ` elif` statements. If there is
an `else` clause, it has to be at the end, but there doesn't have to be
one.

    if choice == 'a':
        draw_a()
    elif choice == 'b':
        draw_b()
    elif choice == 'c':
        draw_c()

Each condition is checked in order. If the first is false, the next is
checked, and so on. If one of them is true, the corresponding branch
runs and the statement ends. Even if more than one condition is true,
only the first true branch runs.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Nested conditionals

One conditional can also be nested within another. We could have written
the example in the previous section like this:

    if x == y:
        print('x and y are equal')
    else:
        if x < y:
            print('x is less than y')
        else:
            print('x is greater than y')

The outer conditional contains two branches. The first branch contains a
simple statement. The second branch contains another `if` statement,
which has two branches of its own. Those two branches are both simple
statements, although they could have been conditional statements as
well.

Although the indentation of the statements makes the structure apparent,
**nested conditionals** become difficult to read very quickly. It is a
good idea to avoid them when you can.

Logical operators often provide a way to simplify nested conditional
statements. For example, we can rewrite the following code using a
single conditional:

    if 0 < x:
        if x < 10:
            print('x is a positive single-digit number.')

The `print` statement runs only if we make it past both conditionals, so
we can get the same effect with the `and` operator:

    if 0 < x and x < 10:
        print('x is a positive single-digit number.')

For this kind of condition, Python provides a more concise option:

    if 0 < x < 10:
        print('x is a positive single-digit number.')

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Recursion
[\[recursion\]]{#recursion label="recursion"}

It is legal for one function to call another; it is also legal for a
function to call itself. It may not be obvious why that is a good thing,
but it turns out to be one of the most magical things a program can do.
For example, look at the following function:

    def countdown(n):
        if n <= 0:
            print('Blastoff!')
        else:
            print(n)
            countdown(n-1)

If `n` is 0 or negative, it outputs the word, "Blastoff!" Otherwise, it
outputs `n` and then calls a function named
` countdown`---itself---passing `n-1` as an argument.

What happens if we call this function like this?

    >>> countdown(3)

The execution of `countdown` begins with `n=3`, and since `n` is greater
than 0, it outputs the value 3, and then calls itself\...

> The execution of `countdown` begins with `n=2`, and since `n` is
> greater than 0, it outputs the value 2, and then calls itself\...
>
> > The execution of `countdown` begins with `n=1`, and since `n` is
> > greater than 0, it outputs the value 1, and then calls itself\...
> >
> > > The execution of `countdown` begins with `n=0`, and since ` n` is
> > > not greater than 0, it outputs the word, "Blastoff!" and then
> > > returns.
> >
> > The `countdown` that got `n=1` returns.
>
> The `countdown` that got `n=2` returns.

The `countdown` that got `n=3` returns.

And then you're back in `__main__`. So, the total output looks like
this:

    3
    2
    1
    Blastoff!

A function that calls itself is **recursive**; the process of executing
it is called **recursion**.

As another example, we can write a function that prints a string `n`
times.

    def print_n(s, n):
        if n <= 0:
            return
        print(s)
        print_n(s, n-1)

If `n <= 0` the **return statement** exits the function. The flow of
execution immediately returns to the caller, and the remaining lines of
the function don't run.

The rest of the function is similar to `countdown`: it displays `s` and
then calls itself to display `s` $n-1$ additional times. So the number
of lines of output is `1 + (n - 1)`, which adds up to `n`.

For simple examples like this, it is probably easier to use a ` for`
loop. But we will see examples later that are hard to write with a `for`
loop and easy to write with recursion, so it is good to start early.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Stack diagrams for recursive
functions [\[recursive.stack\]]{#recursive.stack
label="recursive.stack"}

In Section [\[stackdiagram\]](#stackdiagram){reference-type="ref"
reference="stackdiagram"}, we used a stack diagram to represent the
state of a program during a function call. The same kind of diagram can
help interpret a recursive function.

Every time a function gets called, Python creates a frame to contain the
function's local variables and parameters. For a recursive function,
there might be more than one frame on the stack at the same time.

Figure [6.1](#fig.stack2){reference-type="ref" reference="fig.stack2"}
shows a stack diagram for `countdown` called with `n = 3`.

![Stack diagram.[]{label="fig.stack2"}](figs/stack2.pdf){#fig.stack2}

As usual, the top of the stack is the frame for `__main__`. It is empty
because we did not create any variables in `__main__` or pass any
arguments to it.

The four `countdown` frames have different values for the parameter `n`.
The bottom of the stack, where `n=0`, is called the **base case**. It
does not make a recursive call, so there are no more frames.

As an exercise, draw a stack diagram for `print_n` called with
`s = 'Hello'` and `n=2`. Then write a function called `do_n` that takes
a function object and a number, `n`, as arguments, and that calls the
given function `n` times.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Infinite recursion

If a recursion never reaches a base case, it goes on making recursive
calls forever, and the program never terminates. This is known as
**infinite recursion**, and it is generally not a good idea. Here is a
minimal program with an infinite recursion:

    def recurse():
        recurse()

In most programming environments, a program with infinite recursion does
not really run forever. Python reports an error message when the maximum
recursion depth is reached:

      File "<stdin>", line 2, in recurse
      File "<stdin>", line 2, in recurse
      File "<stdin>", line 2, in recurse
                      .   
                      .
                      .
      File "<stdin>", line 2, in recurse
    RuntimeError: Maximum recursion depth exceeded

This traceback is a little bigger than the one we saw in the previous
chapter. When the error occurs, there are 1000 `recurse` frames on the
stack!

If you encounter an infinite recursion by accident, review your function
to confirm that there is a base case that does not make a recursive
call. And if there is a base case, check whether you are guaranteed to
reach it.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Keyboard input

The programs we have written so far accept no input from the user. They
just do the same thing every time.

Python provides a built-in function called `input` that stops the
program and waits for the user to type something. When the user presses
Return or Enter, the program resumes and `input` returns what the user
typed as a string. In Python 2, the same function is called `raw_input`.

    >>> text = input()
    What are you waiting for?
    >>> text
    'What are you waiting for?'

Before getting input from the user, it is a good idea to print a prompt
telling the user what to type. `input` can take a prompt as an argument:

    >>> name = input('What...is your name?\n')
    What...is your name?
    Arthur, King of the Britons!
    >>> name
    'Arthur, King of the Britons!'

The sequence `\n` at the end of the prompt represents a **newline**,
which is a special character that causes a line break. That's why the
user's input appears below the prompt.

If you expect the user to type an integer, you can try to convert the
return value to `int`:

    >>> prompt = 'What...is the airspeed velocity of an unladen swallow?\n'
    >>> speed = input(prompt)
    What...is the airspeed velocity of an unladen swallow?
    42
    >>> int(speed)
    42

But if the user types something other than a string of digits, you get
an error:

    >>> speed = input(prompt)
    What...is the airspeed velocity of an unladen swallow?
    What do you mean, an African or a European swallow?
    >>> int(speed)
    ValueError: invalid literal for int() with base 10

We will see how to handle this kind of error later.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Debugging
[\[whitespace\]]{#whitespace label="whitespace"}

When a syntax or runtime error occurs, the error message contains a lot
of information, but it can be overwhelming. The most useful parts are
usually:

-   What kind of error it was, and

-   Where it occurred.

Syntax errors are usually easy to find, but there are a few gotchas.
Whitespace errors can be tricky because spaces and tabs are invisible
and we are used to ignoring them.

    >>> x = 5
    >>>  y = 6
      File "<stdin>", line 1
        y = 6
        ^
    IndentationError: unexpected indent

In this example, the problem is that the second line is indented by one
space. But the error message points to `y`, which is misleading. In
general, error messages indicate where the problem was discovered, but
the actual error might be earlier in the code, sometimes on a previous
line.

The same is true of runtime errors. Suppose you are trying to compute a
signal-to-noise ratio in decibels. The formula is
$SNR_{db} = 10 \log_{10} (P_{signal} / P_{noise})$. In Python, you might
write something like this:

    import math
    signal_power = 9
    noise_power = 10
    ratio = signal_power // noise_power
    decibels = 10 * math.log10(ratio)
    print(decibels)

When you run this program, you get an exception:

    Traceback (most recent call last):
      File "snr.py", line 5, in ?
        decibels = 10 * math.log10(ratio)
    ValueError: math domain error

The error message indicates line 5, but there is nothing wrong with that
line. To find the real error, it might be useful to print the value of
`ratio`, which turns out to be 0. The problem is in line 4, which uses
floor division instead of floating-point division.

You should take the time to read error messages carefully, but don't
assume that everything they say is correct.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Glossary

floor division:

:   An operator, denoted `//`, that divides two numbers and rounds down
    (toward negative infinity) to an integer.

modulus operator:

:   An operator, denoted with a percent sign (`%`), that works on
    integers and returns the remainder when one number is divided by
    another.

boolean expression:

:   An expression whose value is either `True` or `False`.

relational operator:

:   One of the operators that compares its operands: `==`, `!=`, `>`,
    `<`, `>=`, and `<=`.

logical operator:

:   One of the operators that combines boolean expressions: `and`, `or`,
    and `not`.

conditional statement:

:   A statement that controls the flow of execution depending on some
    condition.

condition:

:   The boolean expression in a conditional statement that determines
    which branch runs.

compound statement:

:   A statement that consists of a header and a body. The header ends
    with a colon (:). The body is indented relative to the header.

branch:

:   One of the alternative sequences of statements in a conditional
    statement.

chained conditional:

:   A conditional statement with a series of alternative branches.

nested conditional:

:   A conditional statement that appears in one of the branches of
    another conditional statement.

return statement:

:   A statement that causes a function to end immediately and return to
    the caller.

recursion:

:   The process of calling the function that is currently executing.

base case:

:   A conditional branch in a recursive function that does not make a
    recursive call.

infinite recursion:

:   A recursion that doesn't have a base case, or never reaches it.
    Eventually, an infinite recursion causes a runtime error.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

The `time` module provides a function, also named `time`, that returns
the current Greenwich Mean Time in "the epoch", which is an arbitrary
time used as a reference point. On UNIX systems, the epoch is 1 January
1970.

    >>> import time
    >>> time.time()
    1437746094.5735958

Write a script that reads the current time and converts it to a time of
day in hours, minutes, and seconds, plus the number of days since the
epoch.

Fermat's Last Theorem says that there are no positive integers $a$, $b$,
and $c$ such that

$$a^n + b^n = c^n$$ for any values of $n$ greater than 2.

1.  Write a function named `check_fermat` that takes four
    parameters---`a`, `b`, `c` and `n`---and checks to see if Fermat's
    theorem holds. If $n$ is greater than 2 and

    $$a^n + b^n = c^n$$ the program should print, "Holy smokes, Fermat
    was wrong!" Otherwise the program should print, "No, that doesn't
    work."

2.  Write a function that prompts the user to input values for `a`, `b`,
    `c` and `n`, converts them to integers, and uses `check_fermat` to
    check whether they violate Fermat's theorem.

If you are given three sticks, you may or may not be able to arrange
them in a triangle. For example, if one of the sticks is 12 inches long
and the other two are one inch long, you will not be able to get the
short sticks to meet in the middle. For any three lengths, there is a
simple test to see if it is possible to form a triangle:

> If any of the three lengths is greater than the sum of the other two,
> then you cannot form a triangle. Otherwise, you can. (If the sum of
> two lengths equals the third, they form what is called a "degenerate"
> triangle.)

1.  Write a function named `is_triangle` that takes three integers as
    arguments, and that prints either "Yes" or "No", depending on
    whether you can or cannot form a triangle from sticks with the given
    lengths.

2.  Write a function that prompts the user to input three stick lengths,
    converts them to integers, and uses `is_triangle` to check whether
    sticks with the given lengths can form a triangle.

What is the output of the following program? Draw a stack diagram that
shows the state of the program when it prints the result.

    def recurse(n, s):
        if n == 0:
            print(s)
        else:
            recurse(n-1, n+s)

    recurse(3, 0)

1.  What would happen if you called this function like this:
    ` recurse(-1, 0)`?

2.  Write a docstring that explains everything someone would need to
    know in order to use this function (and nothing else).

The following exercises use the `turtle` module, described in
Chapter [5](#turtlechap){reference-type="ref" reference="turtlechap"}:

Read the following function and see if you can figure out what it does
(see the examples in Chapter [5](#turtlechap){reference-type="ref"
reference="turtlechap"}). Then run it and see if you got it right.

    def draw(t, length, n):
        if n == 0:
            return
        angle = 50
        t.fd(length*n)
        t.lt(angle)
        draw(t, length, n-1)
        t.rt(2*angle)
        draw(t, length, n-1)
        t.lt(angle)
        t.bk(length*n)

![A Koch curve.[]{label="fig.koch"}](figs/koch.pdf){#fig.koch}

The Koch curve is a fractal that looks something like
Figure [6.2](#fig.koch){reference-type="ref" reference="fig.koch"}. To
draw a Koch curve with length $x$, all you have to do is

1.  Draw a Koch curve with length $x/3$.

2.  Turn left 60 degrees.

3.  Draw a Koch curve with length $x/3$.

4.  Turn right 120 degrees.

5.  Draw a Koch curve with length $x/3$.

6.  Turn left 60 degrees.

7.  Draw a Koch curve with length $x/3$.

The exception is if $x$ is less than 3: in that case, you can just draw
a straight line with length $x$.

1.  Write a function called `koch` that takes a turtle and a length as
    parameters, and that uses the turtle to draw a Koch curve with the
    given length.

2.  Write a function called `snowflake` that draws three Koch curves to
    make the outline of a snowflake.

    Solution: <http://thinkpython2.com/code/koch.py>.

3.  The Koch curve can be generalized in several ways. See
    <http://en.wikipedia.org/wiki/Koch_snowflake> for examples and
    implement your favorite.

Fruitful functions {#fruitchap}
==================

Many of the Python functions we have used, such as the math functions,
produce return values. But the functions we've written are all void:
they have an effect, like printing a value or moving a turtle, but they
don't have a return value. In this chapter you will learn to write
fruitful functions.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Return values

Calling the function generates a return value, which we usually assign
to a variable or use as part of an expression.

    e = math.exp(1.0)
    height = radius * math.sin(radians)

The functions we have written so far are void. Speaking casually, they
have no return value; more precisely, their return value is `None`.

In this chapter, we are (finally) going to write fruitful functions. The
first example is `area`, which returns the area of a circle with the
given radius:

    def area(radius):
        a = math.pi * radius**2
        return a

We have seen the `return` statement before, but in a fruitful function
the `return` statement includes an expression. This statement means:
"Return immediately from this function and use the following expression
as a return value." The expression can be arbitrarily complicated, so we
could have written this function more concisely:

    def area(radius):
        return math.pi * radius**2

On the other hand, **temporary variables** like `a` can make debugging
easier.

Sometimes it is useful to have multiple return statements, one in each
branch of a conditional:

    def absolute_value(x):
        if x < 0:
            return -x
        else:
            return x

Since these `return` statements are in an alternative conditional, only
one runs.

As soon as a return statement runs, the function terminates without
executing any subsequent statements. Code that appears after a `return`
statement, or any other place the flow of execution can never reach, is
called **dead code**.

In a fruitful function, it is a good idea to ensure that every possible
path through the program hits a `return` statement. For example:

    def absolute_value(x):
        if x < 0:
            return -x
        if x > 0:
            return x

This function is incorrect because if `x` happens to be 0, neither
condition is true, and the function ends without hitting a `return`
statement. If the flow of execution gets to the end of a function, the
return value is `None`, which is not the absolute value of 0.

    >>> print(absolute_value(0))
    None

By the way, Python provides a built-in function called `abs` that
computes absolute values.

As an exercise, write a `compare` function that takes two values, `x`
and `y`, and returns `1` if `x > y`, `0` if `x == y`, and `-1` if
`x < y`.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Incremental development
[\[incremental.development\]]{#incremental.development
label="incremental.development"}

As you write larger functions, you might find yourself spending more
time debugging.

To deal with increasingly complex programs, you might want to try a
process called **incremental development**. The goal of incremental
development is to avoid long debugging sessions by adding and testing
only a small amount of code at a time.

As an example, suppose you want to find the distance between two points,
given by the coordinates $(x_1, y_1)$ and $(x_2, y_2)$. By the
Pythagorean theorem, the distance is:

$$\mathrm{distance} = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$ The first
step is to consider what a `distance` function should look like in
Python. In other words, what are the inputs (parameters) and what is the
output (return value)?

In this case, the inputs are two points, which you can represent using
four numbers. The return value is the distance represented by a
floating-point value.

Immediately you can write an outline of the function:

    def distance(x1, y1, x2, y2):
        return 0.0

Obviously, this version doesn't compute distances; it always returns
zero. But it is syntactically correct, and it runs, which means that you
can test it before you make it more complicated.

To test the new function, call it with sample arguments:

    >>> distance(1, 2, 4, 6)
    0.0

I chose these values so that the horizontal distance is 3 and the
vertical distance is 4; that way, the result is 5, the hypotenuse of a
3-4-5 right triangle. When testing a function, it is useful to know the
right answer.

At this point we have confirmed that the function is syntactically
correct, and we can start adding code to the body. A reasonable next
step is to find the differences $x_2 - x_1$ and $y_2 - y_1$. The next
version stores those values in temporary variables and prints them.

    def distance(x1, y1, x2, y2):
        dx = x2 - x1
        dy = y2 - y1
        print('dx is', dx)
        print('dy is', dy)
        return 0.0

If the function is working, it should display `dx is 3` and `dy is 4`.
If so, we know that the function is getting the right arguments and
performing the first computation correctly. If not, there are only a few
lines to check.

Next we compute the sum of squares of `dx` and `dy`:

    def distance(x1, y1, x2, y2):
        dx = x2 - x1
        dy = y2 - y1
        dsquared = dx**2 + dy**2
        print('dsquared is: ', dsquared)
        return 0.0

Again, you would run the program at this stage and check the output
(which should be 25). Finally, you can use `math.sqrt` to compute and
return the result:

    def distance(x1, y1, x2, y2):
        dx = x2 - x1
        dy = y2 - y1
        dsquared = dx**2 + dy**2
        result = math.sqrt(dsquared)
        return result

If that works correctly, you are done. Otherwise, you might want to
print the value of `result` before the return statement.

The final version of the function doesn't display anything when it runs;
it only returns a value. The `print` statements we wrote are useful for
debugging, but once you get the function working, you should remove
them. Code like that is called **scaffolding** because it is helpful for
building the program but is not part of the final product.

When you start out, you should add only a line or two of code at a time.
As you gain more experience, you might find yourself writing and
debugging bigger chunks. Either way, incremental development can save
you a lot of debugging time.

The key aspects of the process are:

1.  Start with a working program and make small incremental changes. At
    any point, if there is an error, you should have a good idea where
    it is.

2.  Use variables to hold intermediate values so you can display and
    check them.

3.  Once the program is working, you might want to remove some of the
    scaffolding or consolidate multiple statements into compound
    expressions, but only if it does not make the program difficult to
    read.

As an exercise, use incremental development to write a function called
`hypotenuse` that returns the length of the hypotenuse of a right
triangle given the lengths of the other two legs as arguments. Record
each stage of the development process as you go.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Composition

As you should expect by now, you can call one function from within
another. As an example, we'll write a function that takes two points,
the center of the circle and a point on the perimeter, and computes the
area of the circle.

Assume that the center point is stored in the variables `xc` and `yc`,
and the perimeter point is in `xp` and `yp`. The first step is to find
the radius of the circle, which is the distance between the two points.
We just wrote a function, ` distance`, that does that:

    radius = distance(xc, yc, xp, yp)

The next step is to find the area of a circle with that radius; we just
wrote that, too:

    result = area(radius)

Encapsulating these steps in a function, we get:

    def circle_area(xc, yc, xp, yp):
        radius = distance(xc, yc, xp, yp)
        result = area(radius)
        return result

The temporary variables `radius` and `result` are useful for development
and debugging, but once the program is working, we can make it more
concise by composing the function calls:

    def circle_area(xc, yc, xp, yp):
        return area(distance(xc, yc, xp, yp))

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Boolean functions
[\[boolean\]]{#boolean label="boolean"}

Functions can return booleans, which is often convenient for hiding
complicated tests inside functions. For example:

    def is_divisible(x, y):
        if x % y == 0:
            return True
        else:
            return False

It is common to give boolean functions names that sound like yes/no
questions; `is_divisible` returns either `True` or `False` to indicate
whether `x` is divisible by `y`.

Here is an example:

    >>> is_divisible(6, 4)
    False
    >>> is_divisible(6, 3)
    True

The result of the `==` operator is a boolean, so we can write the
function more concisely by returning it directly:

    def is_divisible(x, y):
        return x % y == 0

Boolean functions are often used in conditional statements:

    if is_divisible(x, y):
        print('x is divisible by y')

It might be tempting to write something like:

    if is_divisible(x, y) == True:
        print('x is divisible by y')

But the extra comparison is unnecessary.

As an exercise, write a function `is_between(x, y, z)` that returns
`True` if $x \le y \le z$ or `False` otherwise.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex More recursion
[\[more.recursion\]]{#more.recursion label="more.recursion"}

We have only covered a small subset of Python, but you might be
interested to know that this subset is a *complete* programming
language, which means that anything that can be computed can be
expressed in this language. Any program ever written could be rewritten
using only the language features you have learned so far (actually, you
would need a few commands to control devices like the mouse, disks,
etc., but that's all).

Proving that claim is a nontrivial exercise first accomplished by Alan
Turing, one of the first computer scientists (some would argue that he
was a mathematician, but a lot of early computer scientists started as
mathematicians). Accordingly, it is known as the Turing Thesis. For a
more complete (and accurate) discussion of the Turing Thesis, I
recommend Michael Sipser's book *Introduction to the Theory of
Computation*.

To give you an idea of what you can do with the tools you have learned
so far, we'll evaluate a few recursively defined mathematical functions.
A recursive definition is similar to a circular definition, in the sense
that the definition contains a reference to the thing being defined. A
truly circular definition is not very useful:

vorpal:

:   An adjective used to describe something that is vorpal.

If you saw that definition in the dictionary, you might be annoyed. On
the other hand, if you looked up the definition of the factorial
function, denoted with the symbol $!$, you might get something like
this: $$\begin{aligned}
&&  0! = 1 \\
&&  n! = n (n-1)!\end{aligned}$$ This definition says that the factorial
of 0 is 1, and the factorial of any other value, $n$, is $n$ multiplied
by the factorial of $n-1$.

So $3!$ is 3 times $2!$, which is 2 times $1!$, which is 1 times $0!$.
Putting it all together, $3!$ equals 3 times 2 times 1 times 1, which is
6.

If you can write a recursive definition of something, you can write a
Python program to evaluate it. The first step is to decide what the
parameters should be. In this case it should be clear that `factorial`
takes an integer:

    def factorial(n):

If the argument happens to be 0, all we have to do is return 1:

    def factorial(n):
        if n == 0:
            return 1

Otherwise, and this is the interesting part, we have to make a recursive
call to find the factorial of $n-1$ and then multiply it by $n$:

    def factorial(n):
        if n == 0:
            return 1
        else:
            recurse = factorial(n-1)
            result = n * recurse
            return result

The flow of execution for this program is similar to the flow of
` countdown` in Section [\[recursion\]](#recursion){reference-type="ref"
reference="recursion"}. If we call `factorial` with the value 3:

Since 3 is not 0, we take the second branch and calculate the factorial
of `n-1`\...

> Since 2 is not 0, we take the second branch and calculate the
> factorial of `n-1`\...
>
> > Since 1 is not 0, we take the second branch and calculate the
> > factorial of `n-1`\...
> >
> > > Since 0 equals 0, we take the first branch and return 1 without
> > > making any more recursive calls.
> >
> > The return value, 1, is multiplied by $n$, which is 1, and the
> > result is returned.
>
> The return value, 1, is multiplied by $n$, which is 2, and the result
> is returned.

The return value (2) is multiplied by $n$, which is 3, and the result,
6, becomes the return value of the function call that started the whole
process.

Figure [7.1](#fig.stack3){reference-type="ref" reference="fig.stack3"}
shows what the stack diagram looks like for this sequence of function
calls.

![Stack diagram.[]{label="fig.stack3"}](figs/stack3.pdf){#fig.stack3}

The return values are shown being passed back up the stack. In each
frame, the return value is the value of `result`, which is the product
of `n` and `recurse`.

In the last frame, the local variables `recurse` and `result` do not
exist, because the branch that creates them does not run.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Leap of faith

Following the flow of execution is one way to read programs, but it can
quickly become overwhelming. An alternative is what I call the "leap of
faith". When you come to a function call, instead of following the flow
of execution, you *assume* that the function works correctly and returns
the right result.

In fact, you are already practicing this leap of faith when you use
built-in functions. When you call `math.cos` or `math.exp`, you don't
examine the bodies of those functions. You just assume that they work
because the people who wrote the built-in functions were good
programmers.

The same is true when you call one of your own functions. For example,
in Section [\[boolean\]](#boolean){reference-type="ref"
reference="boolean"}, we wrote a function called `is_divisible` that
determines whether one number is divisible by another. Once we have
convinced ourselves that this function is correct---by examining the
code and testing---we can use the function without looking at the body
again.

The same is true of recursive programs. When you get to the recursive
call, instead of following the flow of execution, you should assume that
the recursive call works (returns the correct result) and then ask
yourself, "Assuming that I can find the factorial of $n-1$, can I
compute the factorial of $n$?" It is clear that you can, by multiplying
by $n$.

Of course, it's a bit strange to assume that the function works
correctly when you haven't finished writing it, but that's why it's
called a leap of faith!

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex One more example
[\[one.more.example\]]{#one.more.example label="one.more.example"}

After `factorial`, the most common example of a recursively defined
mathematical function is `fibonacci`, which has the following definition
(see <http://en.wikipedia.org/wiki/Fibonacci_number>): $$\begin{aligned}
&& \mathrm{fibonacci}(0) = 0 \\
&& \mathrm{fibonacci}(1) = 1 \\
&& \mathrm{fibonacci}(n) = \mathrm{fibonacci}(n-1) + \mathrm{fibonacci}(n-2)\end{aligned}$$
Translated into Python, it looks like this:

    def fibonacci(n):
        if n == 0:
            return 0
        elif  n == 1:
            return 1
        else:
            return fibonacci(n-1) + fibonacci(n-2)

If you try to follow the flow of execution here, even for fairly small
values of $n$, your head explodes. But according to the leap of faith,
if you assume that the two recursive calls work correctly, then it is
clear that you get the right result by adding them together.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Checking types
[\[guardian\]]{#guardian label="guardian"}

What happens if we call `factorial` and give it 1.5 as an argument?

    >>> factorial(1.5)
    RuntimeError: Maximum recursion depth exceeded

It looks like an infinite recursion. How can that be? The function has a
base case---when `n == 0`. But if `n` is not an integer, we can *miss*
the base case and recurse forever.

In the first recursive call, the value of `n` is 0.5. In the next, it is
-0.5. From there, it gets smaller (more negative), but it will never be
0.

We have two choices. We can try to generalize the `factorial` function
to work with floating-point numbers, or we can make ` factorial` check
the type of its argument. The first option is called the gamma function
and it's a little beyond the scope of this book. So we'll go for the
second.

We can use the built-in function `isinstance` to verify the type of the
argument. While we're at it, we can also make sure the argument is
positive:

    def factorial(n):
        if not isinstance(n, int):
            print('Factorial is only defined for integers.')
            return None
        elif n < 0:
            print('Factorial is not defined for negative integers.')
            return None
        elif n == 0:
            return 1
        else:
            return n * factorial(n-1)

The first base case handles nonintegers; the second handles negative
integers. In both cases, the program prints an error message and returns
`None` to indicate that something went wrong:

    >>> print(factorial('fred'))
    Factorial is only defined for integers.
    None
    >>> print(factorial(-2))
    Factorial is not defined for negative integers.
    None

If we get past both checks, we know that $n$ is a non-negative integer,
so we can prove that the recursion terminates.

This program demonstrates a pattern sometimes called a **guardian**. The
first two conditionals act as guardians, protecting the code that
follows from values that might cause an error. The guardians make it
possible to prove the correctness of the code.

In Section [\[raise\]](#raise){reference-type="ref" reference="raise"}
we will see a more flexible alternative to printing an error message:
raising an exception.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Debugging
[\[factdebug\]]{#factdebug label="factdebug"}

Breaking a large program into smaller functions creates natural
checkpoints for debugging. If a function is not working, there are three
possibilities to consider:

-   There is something wrong with the arguments the function is getting;
    a precondition is violated.

-   There is something wrong with the function; a postcondition is
    violated.

-   There is something wrong with the return value or the way it is
    being used.

To rule out the first possibility, you can add a `print` statement at
the beginning of the function and display the values of the parameters
(and maybe their types). Or you can write code that checks the
preconditions explicitly.

If the parameters look good, add a `print` statement before each
`return` statement and display the return value. If possible, check the
result by hand. Consider calling the function with values that make it
easy to check the result (as in
Section [\[incremental.development\]](#incremental.development){reference-type="ref"
reference="incremental.development"}).

If the function seems to be working, look at the function call to make
sure the return value is being used correctly (or used at all!).

Adding print statements at the beginning and end of a function can help
make the flow of execution more visible. For example, here is a version
of `factorial` with print statements:

    def factorial(n):
        space = ' ' * (4 * n)
        print(space, 'factorial', n)
        if n == 0:
            print(space, 'returning 1')
            return 1
        else:
            recurse = factorial(n-1)
            result = n * recurse
            print(space, 'returning', result)
            return result

`space` is a string of space characters that controls the indentation of
the output. Here is the result of `factorial(4)` :

                     factorial 4
                 factorial 3
             factorial 2
         factorial 1
     factorial 0
     returning 1
         returning 1
             returning 2
                 returning 6
                     returning 24

If you are confused about the flow of execution, this kind of output can
be helpful. It takes some time to develop effective scaffolding, but a
little bit of scaffolding can save a lot of debugging.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Glossary

temporary variable:

:   A variable used to store an intermediate value in a complex
    calculation.

dead code:

:   Part of a program that can never run, often because it appears after
    a `return` statement.

incremental development:

:   A program development plan intended to avoid debugging by adding and
    testing only a small amount of code at a time.

scaffolding:

:   Code that is used during program development but is not part of the
    final version.

guardian:

:   A programming pattern that uses a conditional statement to check for
    and handle circumstances that might cause an error.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

Draw a stack diagram for the following program. What does the program
print?

    def b(z):
        prod = a(z, z)
        print(z, prod)
        return prod

    def a(x, y):
        x = x + 1
        return x * y

    def c(x, y, z):
        total = x + y + z
        square = b(total)**2
        return square

    x = 1
    y = x + 1
    print(c(x, y+3, x+y))

[\[ackermann\]]{#ackermann label="ackermann"}

The Ackermann function, $A(m, n)$, is defined:

$$\begin{aligned}
A(m, n) = \begin{cases} 
              n+1 & \mbox{if } m = 0 \\ 
        A(m-1, 1) & \mbox{if } m > 0 \mbox{ and } n = 0 \\ 
A(m-1, A(m, n-1)) & \mbox{if } m > 0 \mbox{ and } n > 0.
\end{cases} \end{aligned}$$ See
<http://en.wikipedia.org/wiki/Ackermann_function>. Write a function
named `ack` that evaluates the Ackermann function. Use your function to
evaluate `ack(3, 4)`, which should be 125. What happens for larger
values of `m` and `n`? Solution:
<http://thinkpython2.com/code/ackermann.py>.

[\[palindrome\]]{#palindrome label="palindrome"}

A palindrome is a word that is spelled the same backward and forward,
like "noon" and "redivider". Recursively, a word is a palindrome if the
first and last letters are the same and the middle is a palindrome.

The following are functions that take a string argument and return the
first, last, and middle letters:

    def first(word):
        return word[0]

    def last(word):
        return word[-1]

    def middle(word):
        return word[1:-1]

We'll see how they work in Chapter [9](#strings){reference-type="ref"
reference="strings"}.

1.  Type these functions into a file named `palindrome.py` and test them
    out. What happens if you call `middle` with a string with two
    letters? One letter? What about the empty string, which is written
    `''` and contains no letters?

2.  Write a function called `is_palindrome` that takes a string argument
    and returns `True` if it is a palindrome and `False` otherwise.
    Remember that you can use the built-in function `len` to check the
    length of a string.

Solution: <http://thinkpython2.com/code/palindrome_soln.py>.

A number, $a$, is a power of $b$ if it is divisible by $b$ and $a/b$ is
a power of $b$. Write a function called `is_power` that takes parameters
`a` and `b` and returns `True` if `a` is a power of `b`. Note: you will
have to think about the base case.

The greatest common divisor (GCD) of $a$ and $b$ is the largest number
that divides both of them with no remainder.

One way to find the GCD of two numbers is based on the observation that
if $r$ is the remainder when $a$ is divided by $b$, then $gcd(a,
b) = gcd(b, r)$. As a base case, we can use $gcd(a, 0) = a$.

Write a function called `gcd` that takes parameters `a` and `b` and
returns their greatest common divisor.

Credit: This exercise is based on an example from Abelson and Sussman's
*Structure and Interpretation of Computer Programs*.

Iteration
=========

This chapter is about iteration, which is the ability to run a block of
statements repeatedly. We saw a kind of iteration, using recursion, in
Section [\[recursion\]](#recursion){reference-type="ref"
reference="recursion"}. We saw another kind, using a `for` loop, in
Section [\[repetition\]](#repetition){reference-type="ref"
reference="repetition"}. In this chapter we'll see yet another kind,
using a `while` statement. But first I want to say a little more about
variable assignment.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Reassignment

As you may have discovered, it is legal to make more than one assignment
to the same variable. A new assignment makes an existing variable refer
to a new value (and stop referring to the old value).

    >>> x = 5
    >>> x
    5
    >>> x = 7
    >>> x
    7

The first time we display `x`, its value is 5; the second time, its
value is 7.

Figure [8.1](#fig.assign2){reference-type="ref" reference="fig.assign2"}
shows what **reassignment** looks like in a state diagram.

At this point I want to address a common source of confusion. Because
Python uses the equal sign (`=`) for assignment, it is tempting to
interpret a statement like `a = b` as a mathematical proposition of
equality; that is, the claim that `a` and `b` are equal. But this
interpretation is wrong.

First, equality is a symmetric relationship and assignment is not. For
example, in mathematics, if $a=7$ then $7=a$. But in Python, the
statement `a = 7` is legal and `7 = a` is not.

Also, in mathematics, a proposition of equality is either true or false
for all time. If $a=b$ now, then $a$ will always equal $b$. In Python,
an assignment statement can make two variables equal, but they don't
have to stay that way:

    >>> a = 5
    >>> b = a    # a and b are now equal
    >>> a = 3    # a and b are no longer equal
    >>> b
    5

The third line changes the value of `a` but does not change the value of
`b`, so they are no longer equal.

Reassigning variables is often useful, but you should use it with
caution. If the values of variables change frequently, it can make the
code difficult to read and debug.

![State diagram.[]{label="fig.assign2"}](figs/assign2.pdf){#fig.assign2}

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Updating variables
[\[update\]]{#update label="update"}

A common kind of reassignment is an **update**, where the new value of
the variable depends on the old.

    >>> x = x + 1

This means "get the current value of `x`, add one, and then update `x`
with the new value."

If you try to update a variable that doesn't exist, you get an error,
because Python evaluates the right side before it assigns a value to
`x`:

    >>> x = x + 1
    NameError: name 'x' is not defined

Before you can update a variable, you have to **initialize** it, usually
with a simple assignment:

    >>> x = 0
    >>> x = x + 1

Updating a variable by adding 1 is called an **increment**; subtracting
1 is called a **decrement**.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex The `while` statement

Computers are often used to automate repetitive tasks. Repeating
identical or similar tasks without making errors is something that
computers do well and people do poorly. In a computer program,
repetition is also called **iteration**.

We have already seen two functions, `countdown` and `print_n`, that
iterate using recursion. Because iteration is so common, Python provides
language features to make it easier. One is the `for` statement we saw
in Section [\[repetition\]](#repetition){reference-type="ref"
reference="repetition"}. We'll get back to that later.

Another is the `while` statement. Here is a version of ` countdown` that
uses a `while` statement:

    def countdown(n):
        while n > 0:
            print(n)
            n = n - 1
        print('Blastoff!')

You can almost read the `while` statement as if it were English. It
means, "While `n` is greater than 0, display the value of `n` and then
decrement `n`. When you get to 0, display the word `Blastoff!`"

More formally, here is the flow of execution for a `while` statement:

1.  Determine whether the condition is true or false.

2.  If false, exit the `while` statement and continue execution at the
    next statement.

3.  If the condition is true, run the body and then go back to step 1.

This type of flow is called a loop because the third step loops back
around to the top.

The body of the loop should change the value of one or more variables so
that the condition becomes false eventually and the loop terminates.
Otherwise the loop will repeat forever, which is called an **infinite
loop**. An endless source of amusement for computer scientists is the
observation that the directions on shampoo, "Lather, rinse, repeat", are
an infinite loop.

In the case of `countdown`, we can prove that the loop terminates: if
`n` is zero or negative, the loop never runs. Otherwise, `n` gets
smaller each time through the loop, so eventually we have to get to 0.

For some other loops, it is not so easy to tell. For example:

    def sequence(n):
        while n != 1:
            print(n)
            if n % 2 == 0:        # n is even
                n = n / 2
            else:                 # n is odd
                n = n*3 + 1

The condition for this loop is `n != 1`, so the loop will continue until
`n` is `1`, which makes the condition false.

Each time through the loop, the program outputs the value of `n` and
then checks whether it is even or odd. If it is even, `n` is divided by
2. If it is odd, the value of `n` is replaced with `n*3 + 1`. For
example, if the argument passed to `sequence` is 3, the resulting values
of `n` are 3, 10, 5, 16, 8, 4, 2, 1.

Since `n` sometimes increases and sometimes decreases, there is no
obvious proof that `n` will ever reach 1, or that the program
terminates. For some particular values of `n`, we can prove termination.
For example, if the starting value is a power of two, `n` will be even
every time through the loop until it reaches 1. The previous example
ends with such a sequence, starting with 16.

The hard question is whether we can prove that this program terminates
for *all* positive values of `n`. So far, no one has been able to prove
it *or* disprove it! (See
<http://en.wikipedia.org/wiki/Collatz_conjecture>.)

As an exercise, rewrite the function `print_n` from
Section [\[recursion\]](#recursion){reference-type="ref"
reference="recursion"} using iteration instead of recursion.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex `break`

Sometimes you don't know it's time to end a loop until you get half way
through the body. In that case you can use the `break` statement to jump
out of the loop.

For example, suppose you want to take input from the user until they
type `done`. You could write:

    while True:
        line = input('> ')
        if line == 'done':
            break
        print(line)

    print('Done!')

The loop condition is `True`, which is always true, so the loop runs
until it hits the break statement.

Each time through, it prompts the user with an angle bracket. If the
user types `done`, the `break` statement exits the loop. Otherwise the
program echoes whatever the user types and goes back to the top of the
loop. Here's a sample run:

    > not done
    not done
    > done
    Done!

This way of writing `while` loops is common because you can check the
condition anywhere in the loop (not just at the top) and you can express
the stop condition affirmatively ("stop when this happens") rather than
negatively ("keep going until that happens").

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Square roots
[\[squareroot\]]{#squareroot label="squareroot"}

Loops are often used in programs that compute numerical results by
starting with an approximate answer and iteratively improving it.

For example, one way of computing square roots is Newton's method.
Suppose that you want to know the square root of $a$. If you start with
almost any estimate, $x$, you can compute a better estimate with the
following formula:

$$y = \frac{x + a/x}{2}$$ For example, if $a$ is 4 and $x$ is 3:

    >>> a = 4
    >>> x = 3
    >>> y = (x + a/x) / 2
    >>> y
    2.16666666667

The result is closer to the correct answer ($\sqrt{4} = 2$). If we
repeat the process with the new estimate, it gets even closer:

    >>> x = y
    >>> y = (x + a/x) / 2
    >>> y
    2.00641025641

After a few more updates, the estimate is almost exact:

    >>> x = y
    >>> y = (x + a/x) / 2
    >>> y
    2.00001024003
    >>> x = y
    >>> y = (x + a/x) / 2
    >>> y
    2.00000000003

In general we don't know ahead of time how many steps it takes to get to
the right answer, but we know when we get there because the estimate
stops changing:

    >>> x = y
    >>> y = (x + a/x) / 2
    >>> y
    2.0
    >>> x = y
    >>> y = (x + a/x) / 2
    >>> y
    2.0

When `y == x`, we can stop. Here is a loop that starts with an initial
estimate, `x`, and improves it until it stops changing:

    while True:
        print(x)
        y = (x + a/x) / 2
        if y == x:
            break
        x = y

For most values of `a` this works fine, but in general it is dangerous
to test `float` equality. Floating-point values are only approximately
right: most rational numbers, like $1/3$, and irrational numbers, like
$\sqrt{2}$, can't be represented exactly with a `float`.

Rather than checking whether `x` and `y` are exactly equal, it is safer
to use the built-in function `abs` to compute the absolute value, or
magnitude, of the difference between them:

        if abs(y-x) < epsilon:
            break

Where `epsilon` has a value like `0.0000001` that determines how close
is close enough.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Algorithms

Newton's method is an example of an **algorithm**: it is a mechanical
process for solving a category of problems (in this case, computing
square roots).

To understand what an algorithm is, it might help to start with
something that is not an algorithm. When you learned to multiply
single-digit numbers, you probably memorized the multiplication table.
In effect, you memorized 100 specific solutions. That kind of knowledge
is not algorithmic.

But if you were "lazy", you might have learned a few tricks. For
example, to find the product of $n$ and 9, you can write $n-1$ as the
first digit and $10-n$ as the second digit. This trick is a general
solution for multiplying any single-digit number by 9. That's an
algorithm!

Similarly, the techniques you learned for addition with carrying,
subtraction with borrowing, and long division are all algorithms. One of
the characteristics of algorithms is that they do not require any
intelligence to carry out. They are mechanical processes where each step
follows from the last according to a simple set of rules.

Executing algorithms is boring, but designing them is interesting,
intellectually challenging, and a central part of computer science.

Some of the things that people do naturally, without difficulty or
conscious thought, are the hardest to express algorithmically.
Understanding natural language is a good example. We all do it, but so
far no one has been able to explain *how* we do it, at least not in the
form of an algorithm.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Debugging
[\[bisectbug\]]{#bisectbug label="bisectbug"}

As you start writing bigger programs, you might find yourself spending
more time debugging. More code means more chances to make an error and
more places for bugs to hide.

One way to cut your debugging time is "debugging by bisection". For
example, if there are 100 lines in your program and you check them one
at a time, it would take 100 steps.

Instead, try to break the problem in half. Look at the middle of the
program, or near it, for an intermediate value you can check. Add a
`print` statement (or something else that has a verifiable effect) and
run the program.

If the mid-point check is incorrect, there must be a problem in the
first half of the program. If it is correct, the problem is in the
second half.

Every time you perform a check like this, you halve the number of lines
you have to search. After six steps (which is fewer than 100), you would
be down to one or two lines of code, at least in theory.

In practice it is not always clear what the "middle of the program" is
and not always possible to check it. It doesn't make sense to count
lines and find the exact midpoint. Instead, think about places in the
program where there might be errors and places where it is easy to put a
check. Then choose a spot where you think the chances are about the same
that the bug is before or after the check.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Glossary

reassignment:

:   Assigning a new value to a variable that already exists.

update:

:   An assignment where the new value of the variable depends on the
    old.

initialization:

:   An assignment that gives an initial value to a variable that will be
    updated.

increment:

:   An update that increases the value of a variable (often by one).

decrement:

:   An update that decreases the value of a variable.

iteration:

:   Repeated execution of a set of statements using either a recursive
    function call or a loop.

infinite loop:

:   A loop in which the terminating condition is never satisfied.

algorithm:

:   A general process for solving a category of problems.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

Copy the loop from
Section [\[squareroot\]](#squareroot){reference-type="ref"
reference="squareroot"} and encapsulate it in a function called `mysqrt`
that takes `a` as a parameter, chooses a reasonable value of `x`, and
returns an estimate of the square root of `a`.

To test it, write a function named `test_square_root` that prints a
table like this:

    a   mysqrt(a)     math.sqrt(a)  diff
    -   ---------     ------------  ----
    1.0 1.0           1.0           0.0
    2.0 1.41421356237 1.41421356237 2.22044604925e-16
    3.0 1.73205080757 1.73205080757 0.0
    4.0 2.0           2.0           0.0
    5.0 2.2360679775  2.2360679775  0.0
    6.0 2.44948974278 2.44948974278 0.0
    7.0 2.64575131106 2.64575131106 0.0
    8.0 2.82842712475 2.82842712475 4.4408920985e-16
    9.0 3.0           3.0           0.0

The first column is a number, $a$; the second column is the square root
of $a$ computed with `mysqrt`; the third column is the square root
computed by `math.sqrt`; the fourth column is the absolute value of the
difference between the two estimates.

The built-in function `eval` takes a string and evaluates it using the
Python interpreter. For example:

    >>> eval('1 + 2 * 3')
    7
    >>> import math
    >>> eval('math.sqrt(5)')
    2.2360679774997898
    >>> eval('type(math.pi)')
    <class 'float'>

Write a function called `eval_loop` that iteratively prompts the user,
takes the resulting input and evaluates it using `eval`, and prints the
result.

It should continue until the user enters `'done'`, and then return the
value of the last expression it evaluated.

The mathematician Srinivasa Ramanujan found an infinite series that can
be used to generate a numerical approximation of $1 / \pi$:

$$\frac{1}{\pi} = \frac{2\sqrt{2}}{9801} 
\sum^\infty_{k=0} \frac{(4k)!(1103+26390k)}{(k!)^4 396^{4k}}$$

Write a function called `estimate_pi` that uses this formula to compute
and return an estimate of $\pi$. It should use a `while` loop to compute
terms of the summation until the last term is smaller than `1e-15`
(which is Python notation for $10^{-15}$). You can check the result by
comparing it to `math.pi`.

Solution: <http://thinkpython2.com/code/pi.py>.

Strings
=======

Strings are not like integers, floats, and booleans. A string is a
**sequence**, which means it is an ordered collection of other values.
In this chapter you'll see how to access the characters that make up a
string, and you'll learn about some of the methods strings provide.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex A string is a sequence

A string is a sequence of characters. You can access the characters one
at a time with the bracket operator:

    >>> fruit = 'banana'
    >>> letter = fruit[1]

The second statement selects character number 1 from ` fruit` and
assigns it to `letter`.

The expression in brackets is called an **index**. The index indicates
which character in the sequence you want (hence the name).

But you might not get what you expect:

    >>> letter
    'a'

For most people, the first letter of `'banana'` is `b`, not `a`. But for
computer scientists, the index is an offset from the beginning of the
string, and the offset of the first letter is zero.

    >>> letter = fruit[0]
    >>> letter
    'b'

So `b` is the 0th letter ("zero-eth") of `'banana'`, ` a` is the 1th
letter ("one-eth"), and `n` is the 2th letter ("two-eth").

As an index you can use an expression that contains variables and
operators:

    >>> i = 1
    >>> fruit[i]
    'a'
    >>> fruit[i+1]
    'n'

But the value of the index has to be an integer. Otherwise you get:

    >>> letter = fruit[1.5]
    TypeError: string indices must be integers

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex `len`

`len` is a built-in function that returns the number of characters in a
string:

    >>> fruit = 'banana'
    >>> len(fruit)
    6

To get the last letter of a string, you might be tempted to try
something like this:

    >>> length = len(fruit)
    >>> last = fruit[length]
    IndexError: string index out of range

The reason for the `IndexError` is that there is no letter in
` ’banana’` with the index 6. Since we started counting at zero, the six
letters are numbered 0 to 5. To get the last character, you have to
subtract 1 from `length`:

    >>> last = fruit[length-1]
    >>> last
    'a'

Or you can use negative indices, which count backward from the end of
the string. The expression `fruit[-1]` yields the last letter,
`fruit[-2]` yields the second to last, and so on.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Traversal with a `for` loop
[\[for\]]{#for label="for"}

A lot of computations involve processing a string one character at a
time. Often they start at the beginning, select each character in turn,
do something to it, and continue until the end. This pattern of
processing is called a **traversal**. One way to write a traversal is
with a `while` loop:

    index = 0
    while index < len(fruit):
        letter = fruit[index]
        print(letter)
        index = index + 1

This loop traverses the string and displays each letter on a line by
itself. The loop condition is `index < len(fruit)`, so when `index` is
equal to the length of the string, the condition is false, and the body
of the loop doesn't run. The last character accessed is the one with the
index `len(fruit)-1`, which is the last character in the string.

As an exercise, write a function that takes a string as an argument and
displays the letters backward, one per line.

Another way to write a traversal is with a `for` loop:

    for letter in fruit:
        print(letter)

Each time through the loop, the next character in the string is assigned
to the variable `letter`. The loop continues until no characters are
left.

The following example shows how to use concatenation (string addition)
and a `for` loop to generate an abecedarian series (that is, in
alphabetical order). In Robert McCloskey's book *Make Way for
Ducklings*, the names of the ducklings are Jack, Kack, Lack, Mack, Nack,
Ouack, Pack, and Quack. This loop outputs these names in order:

    prefixes = 'JKLMNOPQ'
    suffix = 'ack'

    for letter in prefixes:
        print(letter + suffix)

The output is:

    Jack
    Kack
    Lack
    Mack
    Nack
    Oack
    Pack
    Qack

Of course, that's not quite right because "Ouack" and "Quack" are
misspelled. As an exercise, modify the program to fix this error.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex String slices
[\[slice\]]{#slice label="slice"}

A segment of a string is called a **slice**. Selecting a slice is
similar to selecting a character:

    >>> s = 'Monty Python'
    >>> s[0:5]
    'Monty'
    >>> s[6:12]
    'Python'

The operator `[n:m]` returns the part of the string from the "n-eth"
character to the "m-eth" character, including the first but excluding
the last. This behavior is counterintuitive, but it might help to
imagine the indices pointing *between* the characters, as in
Figure [9.1](#fig.banana){reference-type="ref" reference="fig.banana"}.

![Slice indices.[]{label="fig.banana"}](figs/banana.pdf){#fig.banana}

If you omit the first index (before the colon), the slice starts at the
beginning of the string. If you omit the second index, the slice goes to
the end of the string:

    >>> fruit = 'banana'
    >>> fruit[:3]
    'ban'
    >>> fruit[3:]
    'ana'

If the first index is greater than or equal to the second the result is
an **empty string**, represented by two quotation marks:

    >>> fruit = 'banana'
    >>> fruit[3:3]
    ''

An empty string contains no characters and has length 0, but other than
that, it is the same as any other string.

Continuing this example, what do you think `fruit[:]` means? Try it and
see.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Strings are immutable

It is tempting to use the `[]` operator on the left side of an
assignment, with the intention of changing a character in a string. For
example:

    >>> greeting = 'Hello, world!'
    >>> greeting[0] = 'J'
    TypeError: 'str' object does not support item assignment

The "object" in this case is the string and the "item" is the character
you tried to assign. For now, an object is the same thing as a value,
but we will refine that definition later
(Section [\[equivalence\]](#equivalence){reference-type="ref"
reference="equivalence"}).

The reason for the error is that strings are **immutable**, which means
you can't change an existing string. The best you can do is create a new
string that is a variation on the original:

    >>> greeting = 'Hello, world!'
    >>> new_greeting = 'J' + greeting[1:]
    >>> new_greeting
    'Jello, world!'

This example concatenates a new first letter onto a slice of `greeting`.
It has no effect on the original string.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Searching [\[find\]]{#find
label="find"}

What does the following function do?

    def find(word, letter):
        index = 0
        while index < len(word):
            if word[index] == letter:
                return index
            index = index + 1
        return -1

In a sense, `find` is the inverse of the `[]` operator. Instead of
taking an index and extracting the corresponding character, it takes a
character and finds the index where that character appears. If the
character is not found, the function returns ` -1`.

This is the first example we have seen of a `return` statement inside a
loop. If `word[index] == letter`, the function breaks out of the loop
and returns immediately.

If the character doesn't appear in the string, the program exits the
loop normally and returns `-1`.

This pattern of computation---traversing a sequence and returning when
we find what we are looking for---is called a **search**.

As an exercise, modify `find` so that it has a third parameter, the
index in `word` where it should start looking.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Looping and counting
[\[counter\]]{#counter label="counter"}

The following program counts the number of times the letter `a` appears
in a string:

    word = 'banana'
    count = 0
    for letter in word:
        if letter == 'a':
            count = count + 1
    print(count)

This program demonstrates another pattern of computation called a
**counter**. The variable `count` is initialized to 0 and then
incremented each time an `a` is found. When the loop exits, `count`
contains the result---the total number of `a`'s.

As an exercise, encapsulate this code in a function named ` count`, and
generalize it so that it accepts the string and the letter as arguments.

Then rewrite the function so that instead of traversing the string, it
uses the three-parameter version of ` find` from the previous section.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex String methods
[\[optional\]]{#optional label="optional"}

Strings provide methods that perform a variety of useful operations. A
method is similar to a function---it takes arguments and returns a
value---but the syntax is different. For example, the method `upper`
takes a string and returns a new string with all uppercase letters.

Instead of the function syntax `upper(word)`, it uses the method syntax
`word.upper()`.

    >>> word = 'banana'
    >>> new_word = word.upper()
    >>> new_word
    'BANANA'

This form of dot notation specifies the name of the method, ` upper`,
and the name of the string to apply the method to, ` word`. The empty
parentheses indicate that this method takes no arguments.

A method call is called an **invocation**; in this case, we would say
that we are invoking `upper` on `word`.

As it turns out, there is a string method named `find` that is
remarkably similar to the function we wrote:

    >>> word = 'banana'
    >>> index = word.find('a')
    >>> index
    1

In this example, we invoke `find` on `word` and pass the letter we are
looking for as a parameter.

Actually, the `find` method is more general than our function; it can
find substrings, not just characters:

    >>> word.find('na')
    2

By default, `find` starts at the beginning of the string, but it can
take a second argument, the index where it should start:

    >>> word.find('na', 3)
    4

This is an example of an **optional argument**; `find` can also take a
third argument, the index where it should stop:

    >>> name = 'bob'
    >>> name.find('b', 1, 2)
    -1

This search fails because `b` does not appear in the index range from
`1` to `2`, not including ` 2`. Searching up to, but not including, the
second index makes `find` consistent with the slice operator.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex The `in` operator
[\[inboth\]]{#inboth label="inboth"}

The word `in` is a boolean operator that takes two strings and returns
`True` if the first appears as a substring in the second:

    >>> 'a' in 'banana'
    True
    >>> 'seed' in 'banana'
    False

For example, the following function prints all the letters from `word1`
that also appear in `word2`:

    def in_both(word1, word2):
        for letter in word1:
            if letter in word2:
                print(letter)

With well-chosen variable names, Python sometimes reads like English.
You could read this loop, "for (each) letter in (the first) word, if
(the) letter (appears) in (the second) word, print (the) letter."

Here's what you get if you compare apples and oranges:

    >>> in_both('apples', 'oranges')
    a
    e
    s

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex String comparison

The relational operators work on strings. To see if two strings are
equal:

    if word == 'banana':
        print('All right, bananas.')

Other relational operations are useful for putting words in alphabetical
order:

    if word < 'banana':
        print('Your word, ' + word + ', comes before banana.')
    elif word > 'banana':
        print('Your word, ' + word + ', comes after banana.')
    else:
        print('All right, bananas.')

Python does not handle uppercase and lowercase letters the same way
people do. All the uppercase letters come before all the lowercase
letters, so:

    Your word, Pineapple, comes before banana.

A common way to address this problem is to convert strings to a standard
format, such as all lowercase, before performing the comparison. Keep
that in mind in case you have to defend yourself against a man armed
with a Pineapple.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Debugging

When you use indices to traverse the values in a sequence, it is tricky
to get the beginning and end of the traversal right. Here is a function
that is supposed to compare two words and return `True` if one of the
words is the reverse of the other, but it contains two errors:

    def is_reverse(word1, word2):
        if len(word1) != len(word2):
            return False
        
        i = 0
        j = len(word2)

        while j > 0:
            if word1[i] != word2[j]:
                return False
            i = i+1
            j = j-1

        return True

The first `if` statement checks whether the words are the same length.
If not, we can return `False` immediately. Otherwise, for the rest of
the function, we can assume that the words are the same length. This is
an example of the guardian pattern in
Section [\[guardian\]](#guardian){reference-type="ref"
reference="guardian"}.

`i` and `j` are indices: `i` traverses `word1` forward while `j`
traverses `word2` backward. If we find two letters that don't match, we
can return `False` immediately. If we get through the whole loop and all
the letters match, we return `True`.

If we test this function with the words "pots" and "stop", we expect the
return value `True`, but we get an IndexError:

    >>> is_reverse('pots', 'stop')
    ...
      File "reverse.py", line 15, in is_reverse
        if word1[i] != word2[j]:
    IndexError: string index out of range

For debugging this kind of error, my first move is to print the values
of the indices immediately before the line where the error appears.

        while j > 0:
            print(i, j)        # print here
            
            if word1[i] != word2[j]:
                return False
            i = i+1
            j = j-1

Now when I run the program again, I get more information:

    >>> is_reverse('pots', 'stop')
    0 4
    ...
    IndexError: string index out of range

The first time through the loop, the value of `j` is 4, which is out of
range for the string `'pots'`. The index of the last character is 3, so
the initial value for `j` should be `len(word2)-1`.

If I fix that error and run the program again, I get:

    >>> is_reverse('pots', 'stop')
    0 3
    1 2
    2 1
    True

This time we get the right answer, but it looks like the loop only ran
three times, which is suspicious. To get a better idea of what is
happening, it is useful to draw a state diagram. During the first
iteration, the frame for `is_reverse` is shown in
Figure [9.2](#fig.state4){reference-type="ref" reference="fig.state4"}.

![State diagram.[]{label="fig.state4"}](figs/state4.pdf){#fig.state4}

I took some license by arranging the variables in the frame and adding
dotted lines to show that the values of `i` and `j` indicate characters
in `word1` and `word2`.

Starting with this diagram, run the program on paper, changing the
values of `i` and `j` during each iteration. Find and fix the second
error in this function. [\[isreverse\]]{#isreverse label="isreverse"}

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Glossary

object:

:   Something a variable can refer to. For now, you can use "object" and
    "value" interchangeably.

sequence:

:   An ordered collection of values where each value is identified by an
    integer index.

item:

:   One of the values in a sequence.

index:

:   An integer value used to select an item in a sequence, such as a
    character in a string. In Python indices start from 0.

slice:

:   A part of a string specified by a range of indices.

empty string:

:   A string with no characters and length 0, represented by two
    quotation marks.

immutable:

:   The property of a sequence whose items cannot be changed.

traverse:

:   To iterate through the items in a sequence, performing a similar
    operation on each.

search:

:   A pattern of traversal that stops when it finds what it is looking
    for.

counter:

:   A variable used to count something, usually initialized to zero and
    then incremented.

invocation:

:   A statement that calls a method.

optional argument:

:   A function or method argument that is not required.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

Read the documentation of the string methods at
<http://docs.python.org/3/library/stdtypes.html#string-methods>. You
might want to experiment with some of them to make sure you understand
how they work. `strip` and `replace` are particularly useful.

The documentation uses a syntax that might be confusing. For example, in
`find(sub[, start[, end]])`, the brackets indicate optional arguments.
So `sub` is required, but `start` is optional, and if you include
`start`, then `end` is optional.

There is a string method called `count` that is similar to the function
in Section [\[counter\]](#counter){reference-type="ref"
reference="counter"}. Read the documentation of this method and write an
invocation that counts the number of `a`'s in `'banana'`.

A string slice can take a third index that specifies the "step size";
that is, the number of spaces between successive characters. A step size
of 2 means every other character; 3 means every third, etc.

    >>> fruit = 'banana'
    >>> fruit[0:5:2]
    'bnn'

A step size of -1 goes through the word backwards, so the slice `[::-1]`
generates a reversed string.

Use this idiom to write a one-line version of `is_palindrome` from
Exercise [\[palindrome\]](#palindrome){reference-type="ref"
reference="palindrome"}.

The following functions are all *intended* to check whether a string
contains any lowercase letters, but at least some of them are wrong. For
each function, describe what the function actually does (assuming that
the parameter is a string).

    def any_lowercase1(s):
        for c in s:
            if c.islower():
                return True
            else:
                return False

    def any_lowercase2(s):
        for c in s:
            if 'c'.islower():
                return 'True'
            else:
                return 'False'

    def any_lowercase3(s):
        for c in s:
            flag = c.islower()
        return flag

    def any_lowercase4(s):
        flag = False
        for c in s:
            flag = flag or c.islower()
        return flag

    def any_lowercase5(s):
        for c in s:
            if not c.islower():
                return False
        return True

[\[exrotate\]]{#exrotate label="exrotate"} A Caesar cypher is a weak
form of encryption that involves "rotating" each letter by a fixed
number of places. To rotate a letter means to shift it through the
alphabet, wrapping around to the beginning if necessary, so 'A' rotated
by 3 is 'D' and 'Z' rotated by 1 is 'A'.

To rotate a word, rotate each letter by the same amount. For example,
"cheer" rotated by 7 is "jolly" and "melon" rotated by -10 is "cubed".
In the movie *2001: A Space Odyssey*, the ship computer is called HAL,
which is IBM rotated by -1.

Write a function called `rotate_word` that takes a string and an integer
as parameters, and returns a new string that contains the letters from
the original string rotated by the given amount.

You might want to use the built-in function `ord`, which converts a
character to a numeric code, and `chr`, which converts numeric codes to
characters. Letters of the alphabet are encoded in alphabetical order,
so for example:

    >>> ord('c') - ord('a')
    2

Because `'c'` is the two-eth letter of the alphabet. But beware: the
numeric codes for upper case letters are different.

Potentially offensive jokes on the Internet are sometimes encoded in
ROT13, which is a Caesar cypher with rotation 13. If you are not easily
offended, find and decode some of them. Solution:
<http://thinkpython2.com/code/rotate.py>.

Case study: word play {#wordplay}
=====================

This chapter presents the second case study, which involves solving word
puzzles by searching for words that have certain properties. For
example, we'll find the longest palindromes in English and search for
words whose letters appear in alphabetical order. And I will present
another program development plan: reduction to a previously solved
problem.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Reading word lists
[\[wordlist\]]{#wordlist label="wordlist"}

For the exercises in this chapter we need a list of English words. There
are lots of word lists available on the Web, but the one most suitable
for our purpose is one of the word lists collected and contributed to
the public domain by Grady Ward as part of the Moby lexicon project (see
<http://wikipedia.org/wiki/Moby_Project>). It is a list of 113,809
official crosswords; that is, words that are considered valid in
crossword puzzles and other word games. In the Moby collection, the
filename is `113809of.fic`; you can download a copy, with the simpler
name `words.txt`, from <http://thinkpython2.com/code/words.txt>.

This file is in plain text, so you can open it with a text editor, but
you can also read it from Python. The built-in function `open` takes the
name of the file as a parameter and returns a **file object** you can
use to read the file.

    >>> fin = open('words.txt')

`fin` is a common name for a file object used for input. The file object
provides several methods for reading, including `readline`, which reads
characters from the file until it gets to a newline and returns the
result as a string:

    >>> fin.readline()
    'aa\n'

The first word in this particular list is "aa", which is a kind of lava.
The sequence `\n` represents the newline character that separates this
word from the next.

The file object keeps track of where it is in the file, so if you call
`readline` again, you get the next word:

    >>> fin.readline()
    'aah\n'

The next word is "aah", which is a perfectly legitimate word, so stop
looking at me like that. Or, if it's the newline character that's
bothering you, we can get rid of it with the string method `strip`:

    >>> line = fin.readline()
    >>> word = line.strip()
    >>> word
    'aahed'

You can also use a file object as part of a `for` loop. This program
reads `words.txt` and prints each word, one per line:

    fin = open('words.txt')
    for line in fin:
        word = line.strip()
        print(word)

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

There are solutions to these exercises in the next section. You should
at least attempt each one before you read the solutions.

Write a program that reads `words.txt` and prints only the words with
more than 20 characters (not counting whitespace).

In 1939 Ernest Vincent Wright published a 50,000 word novel called
*Gadsby* that does not contain the letter "e". Since "e" is the most
common letter in English, that's not easy to do.

In fact, it is difficult to construct a solitary thought without using
that most common symbol. It is slow going at first, but with caution and
hours of training you can gradually gain facility.

All right, I'll stop now.

Write a function called `has_no_e` that returns `True` if the given word
doesn't have the letter "e" in it.

Write a program that reads `words.txt` and prints only the words that
have no "e". Compute the percentage of words in the list that have no
"e".

Write a function named `avoids` that takes a word and a string of
forbidden letters, and that returns `True` if the word doesn't use any
of the forbidden letters.

Write a program that prompts the user to enter a string of forbidden
letters and then prints the number of words that don't contain any of
them. Can you find a combination of 5 forbidden letters that excludes
the smallest number of words?

Write a function named `uses_only` that takes a word and a string of
letters, and that returns `True` if the word contains only letters in
the list. Can you make a sentence using only the letters `acefhlo`?
Other than "Hoe alfalfa"?

Write a function named `uses_all` that takes a word and a string of
required letters, and that returns `True` if the word uses all the
required letters at least once. How many words are there that use all
the vowels `aeiou`? How about `aeiouy`?

Write a function called `is_abecedarian` that returns `True` if the
letters in a word appear in alphabetical order (double letters are ok).
How many abecedarian words are there?

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Search [\[search\]]{#search
label="search"}

All of the exercises in the previous section have something in common;
they can be solved with the search pattern we saw in
Section [\[find\]](#find){reference-type="ref" reference="find"}. The
simplest example is:

    def has_no_e(word):
        for letter in word:
            if letter == 'e':
                return False
        return True

The `for` loop traverses the characters in `word`. If we find the letter
"e", we can immediately return `False`; otherwise we have to go to the
next letter. If we exit the loop normally, that means we didn't find an
"e", so we return `True`.

You could write this function more concisely using the `in` operator,
but I started with this version because it demonstrates the logic of the
search pattern.

`avoids` is a more general version of `has_no_e` but it has the same
structure:

    def avoids(word, forbidden):
        for letter in word:
            if letter in forbidden:
                return False
        return True

We can return `False` as soon as we find a forbidden letter; if we get
to the end of the loop, we return `True`.

`uses_only` is similar except that the sense of the condition is
reversed:

    def uses_only(word, available):
        for letter in word: 
            if letter not in available:
                return False
        return True

Instead of a list of forbidden letters, we have a list of available
letters. If we find a letter in `word` that is not in `available`, we
can return `False`.

`uses_all` is similar except that we reverse the role of the word and
the string of letters:

    def uses_all(word, required):
        for letter in required: 
            if letter not in word:
                return False
        return True

Instead of traversing the letters in `word`, the loop traverses the
required letters. If any of the required letters do not appear in the
word, we can return `False`.

If you were really thinking like a computer scientist, you would have
recognized that `uses_all` was an instance of a previously solved
problem, and you would have written:

    def uses_all(word, required):
        return uses_only(required, word)

This is an example of a program development plan called **reduction to a
previously solved problem**, which means that you recognize the problem
you are working on as an instance of a solved problem and apply an
existing solution.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Looping with indices

I wrote the functions in the previous section with `for` loops because I
only needed the characters in the strings; I didn't have to do anything
with the indices.

For `is_abecedarian` we have to compare adjacent letters, which is a
little tricky with a `for` loop:

    def is_abecedarian(word):
        previous = word[0]
        for c in word:
            if c < previous:
                return False
            previous = c
        return True

An alternative is to use recursion:

    def is_abecedarian(word):
        if len(word) <= 1:
            return True
        if word[0] > word[1]:
            return False
        return is_abecedarian(word[1:])

Another option is to use a `while` loop:

    def is_abecedarian(word):
        i = 0
        while i < len(word)-1:
            if word[i+1] < word[i]:
                return False
            i = i+1
        return True

The loop starts at `i=0` and ends when `i=len(word)-1`. Each time
through the loop, it compares the $i$th character (which you can think
of as the current character) to the $i+1$th character (which you can
think of as the next).

If the next character is less than (alphabetically before) the current
one, then we have discovered a break in the abecedarian trend, and we
return `False`.

If we get to the end of the loop without finding a fault, then the word
passes the test. To convince yourself that the loop ends correctly,
consider an example like `'flossy'`. The length of the word is 6, so the
last time the loop runs is when `i` is 4, which is the index of the
second-to-last character. On the last iteration, it compares the
second-to-last character to the last, which is what we want.

Here is a version of `is_palindrome` (see
Exercise [\[palindrome\]](#palindrome){reference-type="ref"
reference="palindrome"}) that uses two indices; one starts at the
beginning and goes up; the other starts at the end and goes down.

    def is_palindrome(word):
        i = 0
        j = len(word)-1

        while i<j:
            if word[i] != word[j]:
                return False
            i = i+1
            j = j-1

        return True

Or we could reduce to a previously solved problem and write:

    def is_palindrome(word):
        return is_reverse(word, word)

Using `is_reverse` from
Section [\[isreverse\]](#isreverse){reference-type="ref"
reference="isreverse"}.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Debugging

Testing programs is hard. The functions in this chapter are relatively
easy to test because you can check the results by hand. Even so, it is
somewhere between difficult and impossible to choose a set of words that
test for all possible errors.

Taking `has_no_e` as an example, there are two obvious cases to check:
words that have an 'e' should return `False`, and words that don't
should return `True`. You should have no trouble coming up with one of
each.

Within each case, there are some less obvious subcases. Among the words
that have an "e", you should test words with an "e" at the beginning,
the end, and somewhere in the middle. You should test long words, short
words, and very short words, like the empty string. The empty string is
an example of a **special case**, which is one of the non-obvious cases
where errors often lurk.

In addition to the test cases you generate, you can also test your
program with a word list like `words.txt`. By scanning the output, you
might be able to catch errors, but be careful: you might catch one kind
of error (words that should not be included, but are) and not another
(words that should be included, but aren't).

In general, testing can help you find bugs, but it is not easy to
generate a good set of test cases, and even if you do, you can't be sure
your program is correct. According to a legendary computer scientist:

> Program testing can be used to show the presence of bugs, but never to
> show their absence!
>
> --- Edsger W. Dijkstra

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Glossary

file object:

:   A value that represents an open file.

reduction to a previously solved problem:

:   A way of solving a problem by expressing it as an instance of a
    previously solved problem.

special case:

:   A test case that is atypical or non-obvious (and less likely to be
    handled correctly).

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

This question is based on a Puzzler that was broadcast on the radio
program *Car Talk* (<http://www.cartalk.com/content/puzzlers>):

> Give me a word with three consecutive double letters. I'll give you a
> couple of words that almost qualify, but don't. For example, the word
> committee, c-o-m-m-i-t-t-e-e. It would be great except for the 'i'
> that sneaks in there. Or Mississippi: M-i-s-s-i-s-s-i-p-p-i. If you
> could take out those i's it would work. But there is a word that has
> three consecutive pairs of letters and to the best of my knowledge
> this may be the only word. Of course there are probably 500 more but I
> can only think of one. What is the word?

Write a program to find it. Solution:
<http://thinkpython2.com/code/cartalk1.py>.

Here's another *Car Talk* Puzzler
(<http://www.cartalk.com/content/puzzlers>):

> "I was driving on the highway the other day and I happened to notice
> my odometer. Like most odometers, it shows six digits, in whole miles
> only. So, if my car had 300,000 miles, for example, I'd see
> 3-0-0-0-0-0.
>
> "Now, what I saw that day was very interesting. I noticed that the
> last 4 digits were palindromic; that is, they read the same forward as
> backward. For example, 5-4-4-5 is a palindrome, so my odometer could
> have read 3-1-5-4-4-5.
>
> "One mile later, the last 5 numbers were palindromic. For example, it
> could have read 3-6-5-4-5-6. One mile after that, the middle 4 out of
> 6 numbers were palindromic. And you ready for this? One mile later,
> all 6 were palindromic!
>
> "The question is, what was on the odometer when I first looked?"

Write a Python program that tests all the six-digit numbers and prints
any numbers that satisfy these requirements. Solution:
<http://thinkpython2.com/code/cartalk2.py>.

Here's another *Car Talk* Puzzler you can solve with a search
(<http://www.cartalk.com/content/puzzlers>):

> "Recently I had a visit with my mom and we realized that the two
> digits that make up my age when reversed resulted in her age. For
> example, if she's 73, I'm 37. We wondered how often this has happened
> over the years but we got sidetracked with other topics and we never
> came up with an answer.
>
> "When I got home I figured out that the digits of our ages have been
> reversible six times so far. I also figured out that if we're lucky it
> would happen again in a few years, and if we're really lucky it would
> happen one more time after that. In other words, it would have
> happened 8 times over all. So the question is, how old am I now?"

Write a Python program that searches for solutions to this Puzzler.
Hint: you might find the string method `zfill` useful.

Solution: <http://thinkpython2.com/code/cartalk3.py>.

Lists
=====

This chapter presents one of Python's most useful built-in types, lists.
You will also learn more about objects and what can happen when you have
more than one name for the same object.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex A list is a sequence
[\[sequence\]]{#sequence label="sequence"}

Like a string, a **list** is a sequence of values. In a string, the
values are characters; in a list, they can be any type. The values in a
list are called **elements** or sometimes **items**.

There are several ways to create a new list; the simplest is to enclose
the elements in square brackets (`[` and `]`):

    [10, 20, 30, 40]
    ['crunchy frog', 'ram bladder', 'lark vomit']

The first example is a list of four integers. The second is a list of
three strings. The elements of a list don't have to be the same type.
The following list contains a string, a float, an integer, and (lo!)
another list:

    ['spam', 2.0, 5, [10, 20]]

A list within another list is **nested**.

A list that contains no elements is called an empty list; you can create
one with empty brackets, `[]`.

As you might expect, you can assign list values to variables:

    >>> cheeses = ['Cheddar', 'Edam', 'Gouda']
    >>> numbers = [42, 123]
    >>> empty = []
    >>> print(cheeses, numbers, empty)
    ['Cheddar', 'Edam', 'Gouda'] [42, 123] []

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Lists are mutable
[\[mutable\]]{#mutable label="mutable"}

The syntax for accessing the elements of a list is the same as for
accessing the characters of a string---the bracket operator. The
expression inside the brackets specifies the index. Remember that the
indices start at 0:

    >>> cheeses[0]
    'Cheddar'

Unlike strings, lists are mutable. When the bracket operator appears on
the left side of an assignment, it identifies the element of the list
that will be assigned.

    >>> numbers = [42, 123]
    >>> numbers[1] = 5
    >>> numbers
    [42, 5]

The one-eth element of `numbers`, which used to be 123, is now 5.

Figure [11.1](#fig.liststate){reference-type="ref"
reference="fig.liststate"} shows the state diagram for ` cheeses`,
`numbers` and `empty`.

![State
diagram.[]{label="fig.liststate"}](figs/liststate.pdf){#fig.liststate}

Lists are represented by boxes with the word "list" outside and the
elements of the list inside. `cheeses` refers to a list with three
elements indexed 0, 1 and 2. `numbers` contains two elements; the
diagram shows that the value of the second element has been reassigned
from 123 to 5. `empty` refers to a list with no elements.

List indices work the same way as string indices:

-   Any integer expression can be used as an index.

-   If you try to read or write an element that does not exist, you get
    an `IndexError`.

-   If an index has a negative value, it counts backward from the end of
    the list.

The `in` operator also works on lists.

    >>> cheeses = ['Cheddar', 'Edam', 'Gouda']
    >>> 'Edam' in cheeses
    True
    >>> 'Brie' in cheeses
    False

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Traversing a list

The most common way to traverse the elements of a list is with a `for`
loop. The syntax is the same as for strings:

    for cheese in cheeses:
        print(cheese)

This works well if you only need to read the elements of the list. But
if you want to write or update the elements, you need the indices. A
common way to do that is to combine the built-in functions `range` and
`len`:

    for i in range(len(numbers)):
        numbers[i] = numbers[i] * 2

This loop traverses the list and updates each element. `len` returns the
number of elements in the list. `range` returns a list of indices from 0
to $n-1$, where $n$ is the length of the list. Each time through the
loop `i` gets the index of the next element. The assignment statement in
the body uses `i` to read the old value of the element and to assign the
new value.

A `for` loop over an empty list never runs the body:

    for x in []:
        print('This never happens.')

Although a list can contain another list, the nested list still counts
as a single element. The length of this list is four:

    ['spam', 1, ['Brie', 'Roquefort', 'Pol le Veq'], [1, 2, 3]]

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex List operations

The `+` operator concatenates lists:

    >>> a = [1, 2, 3]
    >>> b = [4, 5, 6]
    >>> c = a + b
    >>> c
    [1, 2, 3, 4, 5, 6]

The `` operator repeats a list a given number of times:

    >>> [0] * 4
    [0, 0, 0, 0]
    >>> [1, 2, 3] * 3
    [1, 2, 3, 1, 2, 3, 1, 2, 3]

The first example repeats `[0]` four times. The second example repeats
the list `[1, 2, 3]` three times.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex List slices

The slice operator also works on lists:

    >>> t = ['a', 'b', 'c', 'd', 'e', 'f']
    >>> t[1:3]
    ['b', 'c']
    >>> t[:4]
    ['a', 'b', 'c', 'd']
    >>> t[3:]
    ['d', 'e', 'f']

If you omit the first index, the slice starts at the beginning. If you
omit the second, the slice goes to the end. So if you omit both, the
slice is a copy of the whole list.

    >>> t[:]
    ['a', 'b', 'c', 'd', 'e', 'f']

Since lists are mutable, it is often useful to make a copy before
performing operations that modify lists.

A slice operator on the left side of an assignment can update multiple
elements:

    >>> t = ['a', 'b', 'c', 'd', 'e', 'f']
    >>> t[1:3] = ['x', 'y']
    >>> t
    ['a', 'x', 'y', 'd', 'e', 'f']

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex List methods

Python provides methods that operate on lists. For example, `append`
adds a new element to the end of a list:

    >>> t = ['a', 'b', 'c']
    >>> t.append('d')
    >>> t
    ['a', 'b', 'c', 'd']

`extend` takes a list as an argument and appends all of the elements:

    >>> t1 = ['a', 'b', 'c']
    >>> t2 = ['d', 'e']
    >>> t1.extend(t2)
    >>> t1
    ['a', 'b', 'c', 'd', 'e']

This example leaves `t2` unmodified.

`sort` arranges the elements of the list from low to high:

    >>> t = ['d', 'c', 'e', 'b', 'a']
    >>> t.sort()
    >>> t
    ['a', 'b', 'c', 'd', 'e']

Most list methods are void; they modify the list and return `None`. If
you accidentally write `t = t.sort()`, you will be disappointed with the
result.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Map, filter and reduce
[\[filter\]]{#filter label="filter"}

To add up all the numbers in a list, you can use a loop like this:

    def add_all(t):
        total = 0
        for x in t:
            total += x
        return total

`total` is initialized to 0. Each time through the loop, `x` gets one
element from the list. The `+=` operator provides a short way to update
a variable. This **augmented assignment statement**,

        total += x

is equivalent to

        total = total + x

As the loop runs, `total` accumulates the sum of the elements; a
variable used this way is sometimes called an **accumulator**.

Adding up the elements of a list is such a common operation that Python
provides it as a built-in function, `sum`:

    >>> t = [1, 2, 3]
    >>> sum(t)
    6

An operation like this that combines a sequence of elements into a
single value is sometimes called **reduce**.

Sometimes you want to traverse one list while building another. For
example, the following function takes a list of strings and returns a
new list that contains capitalized strings:

    def capitalize_all(t):
        res = []
        for s in t:
            res.append(s.capitalize())
        return res

`res` is initialized with an empty list; each time through the loop, we
append the next element. So `res` is another kind of accumulator.

An operation like `capitalize_all` is sometimes called a **map** because
it "maps" a function (in this case the method ` capitalize`) onto each
of the elements in a sequence.

Another common operation is to select some of the elements from a list
and return a sublist. For example, the following function takes a list
of strings and returns a list that contains only the uppercase strings:

    def only_upper(t):
        res = []
        for s in t:
            if s.isupper():
                res.append(s)
        return res

`isupper` is a string method that returns `True` if the string contains
only upper case letters.

An operation like `only_upper` is called a **filter** because it selects
some of the elements and filters out the others.

Most common list operations can be expressed as a combination of map,
filter and reduce.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Deleting elements

There are several ways to delete elements from a list. If you know the
index of the element you want, you can use `pop`:

    >>> t = ['a', 'b', 'c']
    >>> x = t.pop(1)
    >>> t
    ['a', 'c']
    >>> x
    'b'

`pop` modifies the list and returns the element that was removed. If you
don't provide an index, it deletes and returns the last element.

If you don't need the removed value, you can use the `del` operator:

    >>> t = ['a', 'b', 'c']
    >>> del t[1]
    >>> t
    ['a', 'c']

If you know the element you want to remove (but not the index), you can
use `remove`:

    >>> t = ['a', 'b', 'c']
    >>> t.remove('b')
    >>> t
    ['a', 'c']

The return value from `remove` is `None`.

To remove more than one element, you can use `del` with a slice index:

    >>> t = ['a', 'b', 'c', 'd', 'e', 'f']
    >>> del t[1:5]
    >>> t
    ['a', 'f']

As usual, the slice selects all the elements up to but not including the
second index.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Lists and strings

A string is a sequence of characters and a list is a sequence of values,
but a list of characters is not the same as a string. To convert from a
string to a list of characters, you can use `list`:

    >>> s = 'spam'
    >>> t = list(s)
    >>> t
    ['s', 'p', 'a', 'm']

Because `list` is the name of a built-in function, you should avoid
using it as a variable name. I also avoid `l` because it looks too much
like `1`. So that's why I use `t`.

The `list` function breaks a string into individual letters. If you want
to break a string into words, you can use the `split` method:

    >>> s = 'pining for the fjords'
    >>> t = s.split()
    >>> t
    ['pining', 'for', 'the', 'fjords']

An optional argument called a **delimiter** specifies which characters
to use as word boundaries. The following example uses a hyphen as a
delimiter:

    >>> s = 'spam-spam-spam'
    >>> delimiter = '-'
    >>> t = s.split(delimiter)
    >>> t
    ['spam', 'spam', 'spam']

`join` is the inverse of `split`. It takes a list of strings and
concatenates the elements. `join` is a string method, so you have to
invoke it on the delimiter and pass the list as a parameter:

    >>> t = ['pining', 'for', 'the', 'fjords']
    >>> delimiter = ' '
    >>> s = delimiter.join(t)
    >>> s
    'pining for the fjords'

In this case the delimiter is a space character, so `join` puts a space
between words. To concatenate strings without spaces, you can use the
empty string, `''`, as a delimiter.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Objects and values
[\[equivalence\]]{#equivalence label="equivalence"}

If we run these assignment statements:

    a = 'banana'
    b = 'banana'

We know that `a` and `b` both refer to a string, but we don't know
whether they refer to the *same* string. There are two possible states,
shown in Figure [11.2](#fig.list1){reference-type="ref"
reference="fig.list1"}.

![State diagram.[]{label="fig.list1"}](figs/list1.pdf){#fig.list1}

In one case, `a` and `b` refer to two different objects that have the
same value. In the second case, they refer to the same object.

To check whether two variables refer to the same object, you can use the
`is` operator.

    >>> a = 'banana'
    >>> b = 'banana'
    >>> a is b
    True

In this example, Python only created one string object, and both ` a`
and `b` refer to it. But when you create two lists, you get two objects:

    >>> a = [1, 2, 3]
    >>> b = [1, 2, 3]
    >>> a is b
    False

So the state diagram looks like
Figure [11.3](#fig.list2){reference-type="ref" reference="fig.list2"}.

![State diagram.[]{label="fig.list2"}](figs/list2.pdf){#fig.list2}

In this case we would say that the two lists are **equivalent**, because
they have the same elements, but not **identical**, because they are not
the same object. If two objects are identical, they are also equivalent,
but if they are equivalent, they are not necessarily identical.

Until now, we have been using "object" and "value" interchangeably, but
it is more precise to say that an object has a value. If you evaluate
`[1, 2, 3]`, you get a list object whose value is a sequence of
integers. If another list has the same elements, we say it has the same
value, but it is not the same object.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Aliasing

If `a` refers to an object and you assign `b = a`, then both variables
refer to the same object:

    >>> a = [1, 2, 3]
    >>> b = a
    >>> b is a
    True

The state diagram looks like
Figure [11.4](#fig.list3){reference-type="ref" reference="fig.list3"}.

![State diagram.[]{label="fig.list3"}](figs/list3.pdf){#fig.list3}

The association of a variable with an object is called a **reference**.
In this example, there are two references to the same object.

An object with more than one reference has more than one name, so we say
that the object is **aliased**.

If the aliased object is mutable, changes made with one alias affect the
other:

    >>> b[0] = 42
    >>> a
    [42, 2, 3]

Although this behavior can be useful, it is error-prone. In general, it
is safer to avoid aliasing when you are working with mutable objects.

For immutable objects like strings, aliasing is not as much of a
problem. In this example:

    a = 'banana'
    b = 'banana'

It almost never makes a difference whether `a` and `b` refer to the same
string or not.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex List arguments
[\[list.arguments\]]{#list.arguments label="list.arguments"}

When you pass a list to a function, the function gets a reference to the
list. If the function modifies the list, the caller sees the change. For
example, `delete_head` removes the first element from a list:

    def delete_head(t):
        del t[0]

Here's how it is used:

    >>> letters = ['a', 'b', 'c']
    >>> delete_head(letters)
    >>> letters
    ['b', 'c']

The parameter `t` and the variable `letters` are aliases for the same
object. The stack diagram looks like
Figure [11.5](#fig.stack5){reference-type="ref" reference="fig.stack5"}.

![Stack diagram.[]{label="fig.stack5"}](figs/stack5.pdf){#fig.stack5}

Since the list is shared by two frames, I drew it between them.

It is important to distinguish between operations that modify lists and
operations that create new lists. For example, the `append` method
modifies a list, but the `+` operator creates a new list.

Here's an example using `append`:

    >>> t1 = [1, 2]
    >>> t2 = t1.append(3)
    >>> t1
    [1, 2, 3]
    >>> t2
    None

The return value from `append` is `None`.

Here's an example using the `+` operator:

    >>> t3 = t1 + [4]
    >>> t1
    [1, 2, 3]
    >>> t3
    [1, 2, 3, 4]

The result of the operator is a new list, and the original list is
unchanged.

This difference is important when you write functions that are supposed
to modify lists. For example, this function *does not* delete the head
of a list:

    def bad_delete_head(t):
        t = t[1:]              # WRONG!

The slice operator creates a new list and the assignment makes `t` refer
to it, but that doesn't affect the caller.

    >>> t4 = [1, 2, 3]
    >>> bad_delete_head(t4)
    >>> t4
    [1, 2, 3]

At the beginning of `bad_delete_head`, `t` and `t4` refer to the same
list. At the end, `t` refers to a new list, but `t4` still refers to the
original, unmodified list.

An alternative is to write a function that creates and returns a new
list. For example, `tail` returns all but the first element of a list:

    def tail(t):
        return t[1:]

This function leaves the original list unmodified. Here's how it is
used:

    >>> letters = ['a', 'b', 'c']
    >>> rest = tail(letters)
    >>> rest
    ['b', 'c']

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Debugging

Careless use of lists (and other mutable objects) can lead to long hours
of debugging. Here are some common pitfalls and ways to avoid them:

1.  Most list methods modify the argument and return `None`. This is the
    opposite of the string methods, which return a new string and leave
    the original alone.

    If you are used to writing string code like this:

        word = word.strip()

    It is tempting to write list code like this:

        t = t.sort()           # WRONG!

    Because `sort` returns `None`, the next operation you perform with
    `t` is likely to fail.

    Before using list methods and operators, you should read the
    documentation carefully and then test them in interactive mode.

2.  Pick an idiom and stick with it.

    Part of the problem with lists is that there are too many ways to do
    things. For example, to remove an element from a list, you can use
    `pop`, `remove`, `del`, or even a slice assignment.

    To add an element, you can use the `append` method or the `+`
    operator. Assuming that `t` is a list and `x` is a list element,
    these are correct:

        t.append(x)
        t = t + [x]
        t += [x]

    And these are wrong:

        t.append([x])          # WRONG!
        t = t.append(x)        # WRONG!
        t + [x]                # WRONG!
        t = t + x              # WRONG!

    Try out each of these examples in interactive mode to make sure you
    understand what they do. Notice that only the last one causes a
    runtime error; the other three are legal, but they do the wrong
    thing.

3.  Make copies to avoid aliasing.

    If you want to use a method like `sort` that modifies the argument,
    but you need to keep the original list as well, you can make a copy.

        >>> t = [3, 1, 2]
        >>> t2 = t[:]
        >>> t2.sort()
        >>> t
        [3, 1, 2]
        >>> t2
        [1, 2, 3]

    In this example you could also use the built-in function `sorted`,
    which returns a new, sorted list and leaves the original alone.

        >>> t2 = sorted(t)
        >>> t
        [3, 1, 2]
        >>> t2
        [1, 2, 3]

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Glossary

list:

:   A sequence of values.

element:

:   One of the values in a list (or other sequence), also called items.

nested list:

:   A list that is an element of another list.

accumulator:

:   A variable used in a loop to add up or accumulate a result.

augmented assignment:

:   A statement that updates the value of a variable using an operator
    like `+=`.

reduce:

:   A processing pattern that traverses a sequence and accumulates the
    elements into a single result.

map:

:   A processing pattern that traverses a sequence and performs an
    operation on each element.

filter:

:   A processing pattern that traverses a list and selects the elements
    that satisfy some criterion.

object:

:   Something a variable can refer to. An object has a type and a value.

equivalent:

:   Having the same value.

identical:

:   Being the same object (which implies equivalence).

reference:

:   The association between a variable and its value.

aliasing:

:   A circumstance where two or more variables refer to the same object.

delimiter:

:   A character or string used to indicate where a string should be
    split.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

You can download solutions to these exercises from
<http://thinkpython2.com/code/list_exercises.py>.

Write a function called `nested_sum` that takes a list of lists of
integers and adds up the elements from all of the nested lists. For
example:

    >>> t = [[1, 2], [3], [4, 5, 6]]
    >>> nested_sum(t)
    21

[\[cumulative\]]{#cumulative label="cumulative"}

Write a function called `cumsum` that takes a list of numbers and
returns the cumulative sum; that is, a new list where the $i$th element
is the sum of the first $i+1$ elements from the original list. For
example:

    >>> t = [1, 2, 3]
    >>> cumsum(t)
    [1, 3, 6]

Write a function called `middle` that takes a list and returns a new
list that contains all but the first and last elements. For example:

    >>> t = [1, 2, 3, 4]
    >>> middle(t)
    [2, 3]

Write a function called `chop` that takes a list, modifies it by
removing the first and last elements, and returns `None`. For example:

    >>> t = [1, 2, 3, 4]
    >>> chop(t)
    >>> t
    [2, 3]

Write a function called `is_sorted` that takes a list as a parameter and
returns `True` if the list is sorted in ascending order and `False`
otherwise. For example:

    >>> is_sorted([1, 2, 2])
    True
    >>> is_sorted(['b', 'a'])
    False

[\[anagram\]]{#anagram label="anagram"}

Two words are anagrams if you can rearrange the letters from one to
spell the other. Write a function called `is_anagram` that takes two
strings and returns `True` if they are anagrams.

[\[duplicate\]]{#duplicate label="duplicate"}

Write a function called `has_duplicates` that takes a list and returns
`True` if there is any element that appears more than once. It should
not modify the original list.

This exercise pertains to the so-called Birthday Paradox, which you can
read about at <http://en.wikipedia.org/wiki/Birthday_paradox>.

If there are 23 students in your class, what are the chances that two of
you have the same birthday? You can estimate this probability by
generating random samples of 23 birthdays and checking for matches.
Hint: you can generate random birthdays with the `randint` function in
the `random` module.

You can download my solution from
<http://thinkpython2.com/code/birthday.py>.

Write a function that reads the file `words.txt` and builds a list with
one element per word. Write two versions of this function, one using the
`append` method and the other using the idiom `t = t + [x]`. Which one
takes longer to run? Why?

Solution: <http://thinkpython2.com/code/wordlist.py>.

[\[wordlist1\]]{#wordlist1 label="wordlist1"} [\[bisection\]]{#bisection
label="bisection"}

To check whether a word is in the word list, you could use the `in`
operator, but it would be slow because it searches through the words in
order.

Because the words are in alphabetical order, we can speed things up with
a bisection search (also known as binary search), which is similar to
what you do when you look a word up in the dictionary (the book, not the
data structure). You start in the middle and check to see whether the
word you are looking for comes before the word in the middle of the
list. If so, you search the first half of the list the same way.
Otherwise you search the second half.

Either way, you cut the remaining search space in half. If the word list
has 113,809 words, it will take about 17 steps to find the word or
conclude that it's not there.

Write a function called `in_bisect` that takes a sorted list and a
target value and returns `True` if the word is in the list and `False`
if it's not.

Or you could read the documentation of the `bisect` module and use that!
Solution: <http://thinkpython2.com/code/inlist.py>.

Two words are a "reverse pair" if each is the reverse of the other.
Write a program that finds all the reverse pairs in the word list.
Solution: <http://thinkpython2.com/code/reverse_pair.py>.

Two words "interlock" if taking alternating letters from each forms a
new word. For example, "shoe" and "cold" interlock to form "schooled".
Solution: <http://thinkpython2.com/code/interlock.py>. Credit: This
exercise is inspired by an example at <http://puzzlers.org>.

1.  Write a program that finds all pairs of words that interlock. Hint:
    don't enumerate all pairs!

2.  Can you find any words that are three-way interlocked; that is,
    every third letter forms a word, starting from the first, second or
    third?

Dictionaries
============

This chapter presents another built-in type called a dictionary.
Dictionaries are one of Python's best features; they are the building
blocks of many efficient and elegant algorithms.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex A dictionary is a mapping

A **dictionary** is like a list, but more general. In a list, the
indices have to be integers; in a dictionary they can be (almost) any
type.

A dictionary contains a collection of indices, which are called
**keys**, and a collection of values. Each key is associated with a
single value. The association of a key and a value is called a
**key-value pair** or sometimes an **item**.

In mathematical language, a dictionary represents a **mapping** from
keys to values, so you can also say that each key "maps to" a value. As
an example, we'll build a dictionary that maps from English to Spanish
words, so the keys and the values are all strings.

The function `dict` creates a new dictionary with no items. Because
`dict` is the name of a built-in function, you should avoid using it as
a variable name.

    >>> eng2sp = dict()
    >>> eng2sp
    {}

The squiggly-brackets, `{}`, represent an empty dictionary. To add items
to the dictionary, you can use square brackets:

    >>> eng2sp['one'] = 'uno'

This line creates an item that maps from the key `'one'` to the value
`'uno'`. If we print the dictionary again, we see a key-value pair with
a colon between the key and value:

    >>> eng2sp
    {'one': 'uno'}

This output format is also an input format. For example, you can create
a new dictionary with three items:

    >>> eng2sp = {'one': 'uno', 'two': 'dos', 'three': 'tres'}

But if you print `eng2sp`, you might be surprised:

    >>> eng2sp
    {'one': 'uno', 'three': 'tres', 'two': 'dos'}

The order of the key-value pairs might not be the same. If you type the
same example on your computer, you might get a different result. In
general, the order of items in a dictionary is unpredictable.

But that's not a problem because the elements of a dictionary are never
indexed with integer indices. Instead, you use the keys to look up the
corresponding values:

    >>> eng2sp['two']
    'dos'

The key `'two'` always maps to the value `'dos'` so the order of the
items doesn't matter.

If the key isn't in the dictionary, you get an exception:

    >>> eng2sp['four']
    KeyError: 'four'

The `len` function works on dictionaries; it returns the number of
key-value pairs:

    >>> len(eng2sp)
    3

The `in` operator works on dictionaries, too; it tells you whether
something appears as a *key* in the dictionary (appearing as a value is
not good enough).

    >>> 'one' in eng2sp
    True
    >>> 'uno' in eng2sp
    False

To see whether something appears as a value in a dictionary, you can use
the method `values`, which returns a collection of values, and then use
the `in` operator:

    >>> vals = eng2sp.values()
    >>> 'uno' in vals
    True

The `in` operator uses different algorithms for lists and dictionaries.
For lists, it searches the elements of the list in order, as in
Section [\[find\]](#find){reference-type="ref" reference="find"}. As the
list gets longer, the search time gets longer in direct proportion.

Python dictionaries use a data structure called a **hashtable** that has
a remarkable property: the `in` operator takes about the same amount of
time no matter how many items are in the dictionary. I explain how
that's possible in
Section [\[hashtable\]](#hashtable){reference-type="ref"
reference="hashtable"}, but the explanation might not make sense until
you've read a few more chapters.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Dictionary as a collection of
counters [\[histogram\]]{#histogram label="histogram"}

Suppose you are given a string and you want to count how many times each
letter appears. There are several ways you could do it:

1.  You could create 26 variables, one for each letter of the alphabet.
    Then you could traverse the string and, for each character,
    increment the corresponding counter, probably using a chained
    conditional.

2.  You could create a list with 26 elements. Then you could convert
    each character to a number (using the built-in function `ord`), use
    the number as an index into the list, and increment the appropriate
    counter.

3.  You could create a dictionary with characters as keys and counters
    as the corresponding values. The first time you see a character, you
    would add an item to the dictionary. After that you would increment
    the value of an existing item.

Each of these options performs the same computation, but each of them
implements that computation in a different way.

An **implementation** is a way of performing a computation; some
implementations are better than others. For example, an advantage of the
dictionary implementation is that we don't have to know ahead of time
which letters appear in the string and we only have to make room for the
letters that do appear.

Here is what the code might look like:

    def histogram(s):
        d = dict()
        for c in s:
            if c not in d:
                d[c] = 1
            else:
                d[c] += 1
        return d

The name of the function is `histogram`, which is a statistical term for
a collection of counters (or frequencies).

The first line of the function creates an empty dictionary. The `for`
loop traverses the string. Each time through the loop, if the character
`c` is not in the dictionary, we create a new item with key `c` and the
initial value 1 (since we have seen this letter once). If `c` is already
in the dictionary we increment `d[c]`.

Here's how it works:

    >>> h = histogram('brontosaurus')
    >>> h
    {'a': 1, 'b': 1, 'o': 2, 'n': 1, 's': 2, 'r': 2, 'u': 2, 't': 1}

The histogram indicates that the letters `'a'` and `'b'` appear once;
`'o'` appears twice, and so on.

Dictionaries have a method called `get` that takes a key and a default
value. If the key appears in the dictionary, `get` returns the
corresponding value; otherwise it returns the default value. For
example:

    >>> h = histogram('a')
    >>> h
    {'a': 1}
    >>> h.get('a', 0)
    1
    >>> h.get('c', 0)
    0

As an exercise, use `get` to write `histogram` more concisely. You
should be able to eliminate the `if` statement.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Looping and dictionaries

If you use a dictionary in a `for` statement, it traverses the keys of
the dictionary. For example, `print_hist` prints each key and the
corresponding value:

    def print_hist(h):
        for c in h:
            print(c, h[c])

Here's what the output looks like:

    >>> h = histogram('parrot')
    >>> print_hist(h)
    a 1
    p 1
    r 2
    t 1
    o 1

Again, the keys are in no particular order. To traverse the keys in
sorted order, you can use the built-in function `sorted`:

    >>> for key in sorted(h):
    ...     print(key, h[key])
    a 1
    o 1
    p 1
    r 2
    t 1

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Reverse lookup
[\[raise\]]{#raise label="raise"}

Given a dictionary `d` and a key `k`, it is easy to find the
corresponding value `v = d[k]`. This operation is called a **lookup**.

But what if you have `v` and you want to find `k`? You have two
problems: first, there might be more than one key that maps to the value
`v`. Depending on the application, you might be able to pick one, or you
might have to make a list that contains all of them. Second, there is no
simple syntax to do a **reverse lookup**; you have to search.

Here is a function that takes a value and returns the first key that
maps to that value:

    def reverse_lookup(d, v):
        for k in d:
            if d[k] == v:
                return k
        raise LookupError()

This function is yet another example of the search pattern, but it uses
a feature we haven't seen before, `raise`. The **raise statement**
causes an exception; in this case it causes a `LookupError`, which is a
built-in exception used to indicate that a lookup operation failed.

If we get to the end of the loop, that means `v` doesn't appear in the
dictionary as a value, so we raise an exception.

Here is an example of a successful reverse lookup:

    >>> h = histogram('parrot')
    >>> key = reverse_lookup(h, 2)
    >>> key
    'r'

And an unsuccessful one:

    >>> key = reverse_lookup(h, 3)
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
      File "<stdin>", line 5, in reverse_lookup
    LookupError

The effect when you raise an exception is the same as when Python raises
one: it prints a traceback and an error message.

When you raise an exception, you can provide a detailed error message as
an optional argument. For example:

    >>> raise LookupError('value does not appear in the dictionary')
    Traceback (most recent call last):
      File "<stdin>", line 1, in ?
    LookupError: value does not appear in the dictionary

A reverse lookup is much slower than a forward lookup; if you have to do
it often, or if the dictionary gets big, the performance of your program
will suffer.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Dictionaries and lists
[\[invert\]]{#invert label="invert"}

Lists can appear as values in a dictionary. For example, if you are
given a dictionary that maps from letters to frequencies, you might want
to invert it; that is, create a dictionary that maps from frequencies to
letters. Since there might be several letters with the same frequency,
each value in the inverted dictionary should be a list of letters.

Here is a function that inverts a dictionary:

    def invert_dict(d):
        inverse = dict()
        for key in d:
            val = d[key]
            if val not in inverse:
                inverse[val] = [key]
            else:
                inverse[val].append(key)
        return inverse

Each time through the loop, `key` gets a key from `d` and `val` gets the
corresponding value. If `val` is not in ` inverse`, that means we
haven't seen it before, so we create a new item and initialize it with a
**singleton** (a list that contains a single element). Otherwise we have
seen this value before, so we append the corresponding key to the list.

Here is an example:

    >>> hist = histogram('parrot')
    >>> hist
    {'a': 1, 'p': 1, 'r': 2, 't': 1, 'o': 1}
    >>> inverse = invert_dict(hist)
    >>> inverse
    {1: ['a', 'p', 't', 'o'], 2: ['r']}

![State diagram.[]{label="fig.dict1"}](figs/dict1.pdf){#fig.dict1}

Figure [12.1](#fig.dict1){reference-type="ref" reference="fig.dict1"} is
a state diagram showing `hist` and `inverse`. A dictionary is
represented as a box with the type `dict` above it and the key-value
pairs inside. If the values are integers, floats or strings, I draw them
inside the box, but I usually draw lists outside the box, just to keep
the diagram simple.

Lists can be values in a dictionary, as this example shows, but they
cannot be keys. Here's what happens if you try:

    >>> t = [1, 2, 3]
    >>> d = dict()
    >>> d[t] = 'oops'
    Traceback (most recent call last):
      File "<stdin>", line 1, in ?
    TypeError: list objects are unhashable

I mentioned earlier that a dictionary is implemented using a hashtable
and that means that the keys have to be **hashable**.

A **hash** is a function that takes a value (of any kind) and returns an
integer. Dictionaries use these integers, called hash values, to store
and look up key-value pairs.

This system works fine if the keys are immutable. But if the keys are
mutable, like lists, bad things happen. For example, when you create a
key-value pair, Python hashes the key and stores it in the corresponding
location. If you modify the key and then hash it again, it would go to a
different location. In that case you might have two entries for the same
key, or you might not be able to find a key. Either way, the dictionary
wouldn't work correctly.

That's why keys have to be hashable, and why mutable types like lists
aren't. The simplest way to get around this limitation is to use tuples,
which we will see in the next chapter.

Since dictionaries are mutable, they can't be used as keys, but they
*can* be used as values.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Memos [\[memoize\]]{#memoize
label="memoize"}

If you played with the `fibonacci` function from
Section [\[one.more.example\]](#one.more.example){reference-type="ref"
reference="one.more.example"}, you might have noticed that the bigger
the argument you provide, the longer the function takes to run.
Furthermore, the run time increases quickly.

To understand why, consider
Figure [12.2](#fig.fibonacci){reference-type="ref"
reference="fig.fibonacci"}, which shows the **call graph** for
`fibonacci` with `n=4`:

![Call
graph.[]{label="fig.fibonacci"}](figs/fibonacci.pdf){#fig.fibonacci}

A call graph shows a set of function frames, with lines connecting each
frame to the frames of the functions it calls. At the top of the graph,
`fibonacci` with `n=4` calls `fibonacci` with ` n=3` and `n=2`. In turn,
`fibonacci` with `n=3` calls `fibonacci` with `n=2` and `n=1`. And so
on.

Count how many times `fibonacci(0)` and `fibonacci(1)` are called. This
is an inefficient solution to the problem, and it gets worse as the
argument gets bigger.

One solution is to keep track of values that have already been computed
by storing them in a dictionary. A previously computed value that is
stored for later use is called a **memo**. Here is a "memoized" version
of `fibonacci`:

    known = {0:0, 1:1}

    def fibonacci(n):
        if n in known:
            return known[n]

        res = fibonacci(n-1) + fibonacci(n-2)
        known[n] = res
        return res

`known` is a dictionary that keeps track of the Fibonacci numbers we
already know. It starts with two items: 0 maps to 0 and 1 maps to 1.

Whenever `fibonacci` is called, it checks `known`. If the result is
already there, it can return immediately. Otherwise it has to compute
the new value, add it to the dictionary, and return it.

If you run this version of `fibonacci` and compare it with the original,
you will find that it is much faster.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Global variables

In the previous example, `known` is created outside the function, so it
belongs to the special frame called `__main__`. Variables in `__main__`
are sometimes called **global** because they can be accessed from any
function. Unlike local variables, which disappear when their function
ends, global variables persist from one function call to the next.

It is common to use global variables for **flags**; that is, boolean
variables that indicate ("flag") whether a condition is true. For
example, some programs use a flag named `verbose` to control the level
of detail in the output:

    verbose = True

    def example1():
        if verbose:
            print('Running example1')

If you try to reassign a global variable, you might be surprised. The
following example is supposed to keep track of whether the function has
been called:

    been_called = False

    def example2():
        been_called = True         # WRONG

But if you run it you will see that the value of `been_called` doesn't
change. The problem is that `example2` creates a new local variable
named `been_called`. The local variable goes away when the function
ends, and has no effect on the global variable.

To reassign a global variable inside a function you have to **declare**
the global variable before you use it:

    been_called = False

    def example2():
        global been_called 
        been_called = True

The **global statement** tells the interpreter something like, "In this
function, when I say `been_called`, I mean the global variable; don't
create a local one."

Here's an example that tries to update a global variable:

    count = 0

    def example3():
        count = count + 1          # WRONG

If you run it you get:

    UnboundLocalError: local variable 'count' referenced before assignment

Python assumes that `count` is local, and under that assumption you are
reading it before writing it. The solution, again, is to declare `count`
global.

    def example3():
        global count
        count += 1

If a global variable refers to a mutable value, you can modify the value
without declaring the variable:

    known = {0:0, 1:1}

    def example4():
        known[2] = 1

So you can add, remove and replace elements of a global list or
dictionary, but if you want to reassign the variable, you have to
declare it:

    def example5():
        global known
        known = dict()

Global variables can be useful, but if you have a lot of them, and you
modify them frequently, they can make programs hard to debug.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Debugging

As you work with bigger datasets it can become unwieldy to debug by
printing and checking the output by hand. Here are some suggestions for
debugging large datasets:

Scale down the input:

:   If possible, reduce the size of the dataset. For example if the
    program reads a text file, start with just the first 10 lines, or
    with the smallest example you can find. You can either edit the
    files themselves, or (better) modify the program so it reads only
    the first `n` lines.

    If there is an error, you can reduce `n` to the smallest value that
    manifests the error, and then increase it gradually as you find and
    correct errors.

Check summaries and types:

:   Instead of printing and checking the entire dataset, consider
    printing summaries of the data: for example, the number of items in
    a dictionary or the total of a list of numbers.

    A common cause of runtime errors is a value that is not the right
    type. For debugging this kind of error, it is often enough to print
    the type of a value.

Write self-checks:

:   Sometimes you can write code to check for errors automatically. For
    example, if you are computing the average of a list of numbers, you
    could check that the result is not greater than the largest element
    in the list or less than the smallest. This is called a "sanity
    check" because it detects results that are "insane".

    Another kind of check compares the results of two different
    computations to see if they are consistent. This is called a
    "consistency check".

Format the output:

:   Formatting debugging output can make it easier to spot an error. We
    saw an example in
    Section [\[factdebug\]](#factdebug){reference-type="ref"
    reference="factdebug"}. Another tool you might find useful is the
    `pprint` module, which provides a `pprint` function that displays
    built-in types in a more human-readable format (`pprint` stands for
    "pretty print").

Again, time you spend building scaffolding can reduce the time you spend
debugging.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Glossary

mapping:

:   A relationship in which each element of one set corresponds to an
    element of another set.

dictionary:

:   A mapping from keys to their corresponding values.

key-value pair:

:   The representation of the mapping from a key to a value.

item:

:   In a dictionary, another name for a key-value pair.

key:

:   An object that appears in a dictionary as the first part of a
    key-value pair.

value:

:   An object that appears in a dictionary as the second part of a
    key-value pair. This is more specific than our previous use of the
    word "value".

implementation:

:   A way of performing a computation.

hashtable:

:   The algorithm used to implement Python dictionaries.

hash function:

:   A function used by a hashtable to compute the location for a key.

hashable:

:   A type that has a hash function. Immutable types like integers,
    floats and strings are hashable; mutable types like lists and
    dictionaries are not.

lookup:

:   A dictionary operation that takes a key and finds the corresponding
    value.

reverse lookup:

:   A dictionary operation that takes a value and finds one or more keys
    that map to it.

raise statement:

:   A statement that (deliberately) raises an exception.

singleton:

:   A list (or other sequence) with a single element.

call graph:

:   A diagram that shows every frame created during the execution of a
    program, with an arrow from each caller to each callee.

memo:

:   A computed value stored to avoid unnecessary future computation.

global variable:

:   A variable defined outside a function. Global variables can be
    accessed from any function.

global statement:

:   A statement that declares a variable name global.

flag:

:   A boolean variable used to indicate whether a condition is true.

declaration:

:   A statement like `global` that tells the interpreter something about
    a variable.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Exercises

[\[wordlist2\]]{#wordlist2 label="wordlist2"}

Write a function that reads the words in `words.txt` and stores them as
keys in a dictionary. It doesn't matter what the values are. Then you
can use the `in` operator as a fast way to check whether a string is in
the dictionary.

If you did Exercise [\[wordlist1\]](#wordlist1){reference-type="ref"
reference="wordlist1"}, you can compare the speed of this implementation
with the list `in` operator and the bisection search.

[\[setdefault\]]{#setdefault label="setdefault"}

Read the documentation of the dictionary method `setdefault` and use it
to write a more concise version of `invert_dict`. Solution:
<http://thinkpython2.com/code/invert_dict.py>.

Memoize the Ackermann function from
Exercise [\[ackermann\]](#ackermann){reference-type="ref"
reference="ackermann"} and see if memoization makes it possible to
evaluate the function with bigger arguments. Hint: no. Solution:
<http://thinkpython2.com/code/ackermann_memo.py>.

If you did Exercise [\[duplicate\]](#duplicate){reference-type="ref"
reference="duplicate"}, you already have a function named
`has_duplicates` that takes a list as a parameter and returns `True` if
there is any object that appears more than once in the list.

Use a dictionary to write a faster, simpler version of `has_duplicates`.
Solution: <http://thinkpython2.com/code/has_duplicates.py>.

[\[exrotatepairs\]]{#exrotatepairs label="exrotatepairs"}

Two words are "rotate pairs" if you can rotate one of them and get the
other (see `rotate_word` in
Exercise [\[exrotate\]](#exrotate){reference-type="ref"
reference="exrotate"}).

Write a program that reads a wordlist and finds all the rotate pairs.
Solution: <http://thinkpython2.com/code/rotate_pairs.py>.

Here's another Puzzler from *Car Talk*
(<http://www.cartalk.com/content/puzzlers>):

> This was sent in by a fellow named Dan O'Leary. He came upon a common
> one-syllable, five-letter word recently that has the following unique
> property. When you remove the first letter, the remaining letters form
> a homophone of the original word, that is a word that sounds exactly
> the same. Replace the first letter, that is, put it back and remove
> the second letter and the result is yet another homophone of the
> original word. And the question is, what's the word?
>
> Now I'm going to give you an example that doesn't work. Let's look at
> the five-letter word, 'wrack.' W-R-A-C-K, you know like to 'wrack with
> pain.' If I remove the first letter, I am left with a four-letter
> word, 'R-A-C-K.' As in, 'Holy cow, did you see the rack on that buck!
> It must have been a nine-pointer!' It's a perfect homophone. If you
> put the 'w' back, and remove the 'r,' instead, you're left with the
> word, 'wack,' which is a real word, it's just not a homophone of the
> other two words.
>
> But there is, however, at least one word that Dan and we know of,
> which will yield two homophones if you remove either of the first two
> letters to make two, new four-letter words. The question is, what's
> the word?

You can use the dictionary from
Exercise [\[wordlist2\]](#wordlist2){reference-type="ref"
reference="wordlist2"} to check whether a string is in the word list.

To check whether two words are homophones, you can use the CMU
Pronouncing Dictionary. You can download it from
<http://www.speech.cs.cmu.edu/cgi-bin/cmudict> or from
<http://thinkpython2.com/code/c06d> and you can also download
<http://thinkpython2.com/code/pronounce.py>, which provides a function
named `read_dictionary` that reads the pronouncing dictionary and
returns a Python dictionary that maps from each word to a string that
describes its primary pronunciation.

Write a program that lists all the words that solve the Puzzler.
Solution: <http://thinkpython2.com/code/homophone.py>.

Tuples {#tuplechap}
======

This chapter presents one more built-in type, the tuple, and then shows
how lists, dictionaries, and tuples work together. I also present a
useful feature for variable-length argument lists, the gather and
scatter operators.

One note: there is no consensus on how to pronounce "tuple". Some people
say "tuh-ple", which rhymes with "supple". But in the context of
programming, most people say "too-ple", which rhymes with "quadruple".

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Tuples are immutable

A tuple is a sequence of values. The values can be any type, and they
are indexed by integers, so in that respect tuples are a lot like lists.
The important difference is that tuples are immutable.

Syntactically, a tuple is a comma-separated list of values:

    >>> t = 'a', 'b', 'c', 'd', 'e'

Although it is not necessary, it is common to enclose tuples in
parentheses:

    >>> t = ('a', 'b', 'c', 'd', 'e')

To create a tuple with a single element, you have to include a final
comma:

    >>> t1 = 'a',
    >>> type(t1)
    <class 'tuple'>

A value in parentheses is not a tuple:

    >>> t2 = ('a')
    >>> type(t2)
    <class 'str'>

Another way to create a tuple is the built-in function `tuple`. With no
argument, it creates an empty tuple:

    >>> t = tuple()
    >>> t
    ()

If the argument is a sequence (string, list or tuple), the result is a
tuple with the elements of the sequence:

    >>> t = tuple('lupins')
    >>> t
    ('l', 'u', 'p', 'i', 'n', 's')

Because `tuple` is the name of a built-in function, you should avoid
using it as a variable name.

Most list operators also work on tuples. The bracket operator indexes an
element:

    >>> t = ('a', 'b', 'c', 'd', 'e')
    >>> t[0]
    'a'

And the slice operator selects a range of elements.

    >>> t[1:3]
    ('b', 'c')

But if you try to modify one of the elements of the tuple, you get an
error:

    >>> t[0] = 'A'
    TypeError: object doesn't support item assignment

Because tuples are immutable, you can't modify the elements. But you can
replace one tuple with another:

    >>> t = ('A',) + t[1:]
    >>> t
    ('A', 'b', 'c', 'd', 'e')

This statement makes a new tuple and then makes `t` refer to it.

The relational operators work with tuples and other sequences; Python
starts by comparing the first element from each sequence. If they are
equal, it goes on to the next elements, and so on, until it finds
elements that differ. Subsequent elements are not considered (even if
they are really big).

    >>> (0, 1, 2) < (0, 3, 4)
    True
    >>> (0, 1, 2000000) < (0, 3, 4)
    True

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Tuple assignment
[\[tuple.assignment\]]{#tuple.assignment label="tuple.assignment"}

It is often useful to swap the values of two variables. With
conventional assignments, you have to use a temporary variable. For
example, to swap `a` and `b`:

    >>> temp = a
    >>> a = b
    >>> b = temp

This solution is cumbersome; **tuple assignment** is more elegant:

    >>> a, b = b, a

The left side is a tuple of variables; the right side is a tuple of
expressions. Each value is assigned to its respective variable. All the
expressions on the right side are evaluated before any of the
assignments.

The number of variables on the left and the number of values on the
right have to be the same:

    >>> a, b = 1, 2, 3
    ValueError: too many values to unpack

More generally, the right side can be any kind of sequence (string, list
or tuple). For example, to split an email address into a user name and a
domain, you could write:

    >>> addr = 'monty@python.org'
    >>> uname, domain = addr.split('@')

The return value from `split` is a list with two elements; the first
element is assigned to `uname`, the second to `domain`.

    >>> uname
    'monty'
    >>> domain
    'python.org'

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Tuples as return values

Strictly speaking, a function can only return one value, but if the
value is a tuple, the effect is the same as returning multiple values.
For example, if you want to divide two integers and compute the quotient
and remainder, it is inefficient to compute `x//y` and then `x%y`. It is
better to compute them both at the same time.

The built-in function `divmod` takes two arguments and returns a tuple
of two values, the quotient and remainder. You can store the result as a
tuple:

    >>> t = divmod(7, 3)
    >>> t
    (2, 1)

Or use tuple assignment to store the elements separately:

    >>> quot, rem = divmod(7, 3)
    >>> quot
    2
    >>> rem
    1

Here is an example of a function that returns a tuple:

    def min_max(t):
        return min(t), max(t)

`max` and `min` are built-in functions that find the largest and
smallest elements of a sequence. `min_max` computes both and returns a
tuple of two values.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Variable-length argument
tuples [\[gather\]]{#gather label="gather"}

Functions can take a variable number of arguments. A parameter name that
begins with `` **gathers** arguments into a tuple. For example,
`printall` takes any number of arguments and prints them:

    def printall(*args):
        print(args)

The gather parameter can have any name you like, but `args` is
conventional. Here's how the function works:

    >>> printall(1, 2.0, '3')
    (1, 2.0, '3')

The complement of gather is **scatter**. If you have a sequence of
values and you want to pass it to a function as multiple arguments, you
can use the `` operator. For example, `divmod` takes exactly two
arguments; it doesn't work with a tuple:

    >>> t = (7, 3)
    >>> divmod(t)
    TypeError: divmod expected 2 arguments, got 1

But if you scatter the tuple, it works:

    >>> divmod(*t)
    (2, 1)

Many of the built-in functions use variable-length argument tuples. For
example, `max` and `min` can take any number of arguments:

    >>> max(1, 2, 3)
    3

But `sum` does not.

    >>> sum(1, 2, 3)
    TypeError: sum expected at most 2 arguments, got 3

As an exercise, write a function called `sum_all` that takes any number
of arguments and returns their sum.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Lists and tuples

`zip` is a built-in function that takes two or more sequences and
interleaves them. The name of the function refers to a zipper, which
interleaves two rows of teeth.

This example zips a string and a list:

    >>> s = 'abc'
    >>> t = [0, 1, 2]
    >>> zip(s, t)
    <zip object at 0x7f7d0a9e7c48>

The result is a **zip object** that knows how to iterate through the
pairs. The most common use of `zip` is in a `for` loop:

    >>> for pair in zip(s, t):
    ...     print(pair)
    ...
    ('a', 0)
    ('b', 1)
    ('c', 2)

A zip object is a kind of **iterator**, which is any object that
iterates through a sequence. Iterators are similar to lists in some
ways, but unlike lists, you can't use an index to select an element from
an iterator.

If you want to use list operators and methods, you can use a zip object
to make a list:

    >>> list(zip(s, t))
    [('a', 0), ('b', 1), ('c', 2)]

The result is a list of tuples; in this example, each tuple contains a
character from the string and the corresponding element from the list.

If the sequences are not the same length, the result has the length of
the shorter one.

    >>> list(zip('Anne', 'Elk'))
    [('A', 'E'), ('n', 'l'), ('n', 'k')]

You can use tuple assignment in a `for` loop to traverse a list of
tuples:

    t = [('a', 0), ('b', 1), ('c', 2)]
    for letter, number in t:
        print(number, letter)

Each time through the loop, Python selects the next tuple in the list
and assigns the elements to `letter` and `number`. The output of this
loop is:

    0 a
    1 b
    2 c

If you combine `zip`, `for` and tuple assignment, you get a useful idiom
for traversing two (or more) sequences at the same time. For example,
`has_match` takes two sequences, `t1` and `t2`, and returns `True` if
there is an index `i` such that `t1[i] == t2[i]`:

    def has_match(t1, t2):
        for x, y in zip(t1, t2):
            if x == y:
                return True
        return False

If you need to traverse the elements of a sequence and their indices,
you can use the built-in function `enumerate`:

    for index, element in enumerate('abc'):
        print(index, element)

The result from `enumerate` is an enumerate object, which iterates a
sequence of pairs; each pair contains an index (starting from 0) and an
element from the given sequence. In this example, the output is

    0 a
    1 b
    2 c

Again.

section 1 0mm -3.5ex -1ex -.2ex 0.7ex .2ex Dictionaries and tuples
[\[dictuple\]]{#dictuple label="dictuple"}

Dictionaries have a method called `items` that returns a sequence of
tuples, where each tuple is a key-value pair.

    >>> d = {'a':0, 'b':1, 'c':2}
    >>> t = d.items()
    >>> t
    dict_items([('c', 2), ('a', 0), ('b', 1)])

The result is a `dict_items` object, which is an iterator that iterates
the key-value pairs. You can use it in a `for` loop like this:

    >>> for key, value in d.items():
    ...     print(key, value)
    ...
    c 2
    a 0
    b 1

As you should expect from a dictionary, the items are in no particular
order.

Going in the other direction, you can use a list of tuples to initialize
a new dictionary:

    >>> t = [('a', 0), ('c', 2), ('b', 1)]
    >>> d = dict(t)
    >>> d
    {'a': 0, 'c': 2, 'b': 1}

Combining `dict` with `zip` yields a concise way to create a dictionary:

    >>> d = dict(zip('abc', range(3)))
    >>> d
    {'a': 0, 'c': 2, 'b': 1}

The dictionary method `update` also takes a list of tuples and adds
them, as key-value pairs, to an existing dictionary.

It is common to use tuples as keys in dictionaries (primarily because
you can't use lists). For example, a telephone directory might map from
last-name, first-name pairs to telephone numbers. Assuming that we have
defined `last`, `first` and `number`, we could write:

    directory[last, first] = number

The expression in brackets is a tuple. We could use tuple assignment to
traverse this dictionary.

    for last, first in dire
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzMzkzMzMwM119
-->