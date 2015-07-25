# Some notes from CMU CS 15-212-ML, spring 1998

In the late 1990s, I TAed an introductory CS course at CMU, 15-212-ML, which taught topics including types, inductive reasoning and proof, functional programming, design of abstract and parameterized data types through modules, using Standard ML as the programming language of choice.

Verbatim below is a handout I gave the students. It would be an interesting exercise to update the pitch today, almost two decades later.

## ML and other functional languages, in the real world

ML originally developed out of the interactive theorem proving
community, so it is no surprise that hundreds of thousands of lines of
ML code out there are in the implementation of theorem provers and
reasoning assistants of all kinds.

ML's strength as a language suitable for correct, efficient, and very
large programs has led to its use in implementing interpreters,
compilers, program verification tools, digital circuit design, memory
coherency protocol design, microprocessor design and validation, other
hardware verification, network security, etc.

It has also been used successfully for operating systems related work.
For example, the Fox Project here at CMU used SML to implement a
TCP/IP protocol stack, all the way down to device drivers.  The Fox
Web page in fact runs an httpd server written in ML.

The Ensemble system at Cornell is a toolkit for distributed network
applications, written in a dialect of ML called O'Caml.  Originally
the project was done in C, but when the researchers moved to O'Caml,
they managed to quickly design very flexible systems that outperformed
the old C implementation by orders of magnitude.

The Pittsburgh Map and Restaurant Database at CMU is implemented in
NESL, a parallel purely functional language very close to ML.

ML and related languages are used in natural language research and
products, for example the MITRE Corporation speech recognition system
and the LOLITA natural language processing system.  People use ML to
investigate genetic algorithms, image processing, and neural networks.

There are also applications in the natural sciences.  For example,
MC-SYM, which is used by molecular biologists to compute the 3D shape
of a piece of nucleic acid molecule given a sequence of nucleotides
and a set of constraints.  The performance-critical code in a very
fast C Fast Fourier Transform library was developed by writing a C
code generator in Caml.

ML has been used for CGI programming.  There is also a Web browser
written in Caml.  This will run applets written in Caml, and comes
with a Netscape plugin so that you can run Caml applets from Netscape
if you want.  ML is used for generation of HTML, e.g., from TeX.

Concurrent ML is a superset of Standard ML, and is part of SML/NJ.
CML includes primitives for concurrency, so that you can concurrent or
parallel programs.  The multithreaded X Windows toolkit eXene is built
on top of CML, and is used to develop GUI applications.  The key to
efficient threads is the use of continuations.

SML/NJ is written in Standard ML, and is a scary monster of 90,000
lines of ML.

The most visible success of functional programming languages in
industry, however, must be Erlang, developed at Ericsson in Sweden.
Erlang is a functional programming language used for implementing very
large scale, real-time, concurrent, industrial applications. Erlang
has been used to control several very large scale (i.e. hundreds of
thousands of lines of source code) telecommunications switching system
products which are marketed world wide by Ericsson today. It has also
been used to implement countless prototypes and experiments. Ericsson
is one of the world's largest manufactures of telecommunications
equipment.
