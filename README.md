  This is release 0.1 of the Caml Light system with functions studied @ UniPi, for Unix machines.

This version is a release of the first stable version of Camllight (0.75).
* Add unipi_forall
* Add unipi_exists
* Add unipi_map
* Add unipi_filter
* Add unipi_foldr

OVERVIEW:

  Caml Light is a small, portable implementation of the ML language.
  that runs on most Unix machines. It has also been ported to the
  Macintosh, the PC, and other microcomputers.

  Caml Light implements the Caml language, a functional language from
  the ML family. Caml is quite close to Standard ML, though not strictly
  conformant. There are some slight differences in syntax and semantics,
  and major differences in the module system.

  Caml Light is implemented as a bytecode compiler, and fully
  bootstrapped.  The runtime system and bytecode interpreter is written
  in standard C, hence Caml Light is easy to port to almost any 32 or 64 bit
  platform. The whole system is quite small: about 100K for the runtime
  system, and another 100K of bytecode for the compiler. 2 megabytes of
  memory is enough to recompile the whole system. This stands in sharp
  contrast with other implementations of ML, such as SML-NJ, that
  requires about ten times more memory. Performance is quite good for a
  bytecoded implementation.

  Caml Light comes in two flavors: a classical, interactive, toplevel-based
  system; and a standalone, batch-oriented compiler that produces standalone
  programs, in the spirit of the Unix cc compiler. The former is good for
  learning the language and testing programs. The latter integrates more
  smoothly with the Unix programming environment: make, compilations under
  Emacs, ... The generated programs are quite small, and can be used like
  any other Unix command.

CONTENTS:

  src/                  the sources for the core Caml Light system
    src/runtime/          the bytecode interpreter and runtime system (in C)
    src/lib/              the standard library (in Caml Light)
    src/compiler/         the compiler (in Caml Light)
    src/linker/           the linker (in Caml Light)
    src/librar/           the linker (in Caml Light)
    src/toplevel/         the toplevel interactive system (in Caml Light)
    src/lex/              the lexer generator (in Caml Light)
    src/yacc/             the parser generator (in C)
    src/tools/            various utilities (sh, perl, C, Caml Light)
    src/caml*             the bootstrap compilers
  config/               the configuration files and autoconfiguration tool
  contrib/              the sources for various libraries and utilities
  examples/             some example programs
  COPYRIGHT             INRIA's copyright notice
  INSTALL               instructions for installation
  README                this file
  CHANGES               what's new
  PORTING               hints on porting Caml Light to a non-Unix machine


COPYRIGHT:

  All files in this distribution are copyright INRIA and distributed
  under the conditions stated in file COPYRIGHT.
  They can be freely redistributed for non-commercial purposes, provided
  the copyright notice remains attached.


INSTALLATION:

  See the file [INSTALL](INSTALL.md)  for installation instructions on Unix
  machines. 


DOCUMENTATION:

  The Caml Light system is described in:

  "The Caml Light system, release 0.75", by Xavier Leroy (reference manual)
  "Functional programming using Caml Light", by Michel Mauny (tutorial)

  These documents are distributed in Postscript, DVI, and plain text.
  They can be obtained by anonymous FTP from ftp.inria.fr as described below.

  The following Web site offers lots of information on Caml:

        http://pauillac.inria.fr/caml/

  including a comprehensive "Frequently Asked Questions" list, short
  tutorials, and material for programming courses.


AVAILABILITY:

  The whole Caml Light distribution resides on ftp.inria.fr, and can
  be accessed by anonymous FTP:

        host:       ftp.inria.fr (192.93.2.54)
        directory:  lang/caml-light

  or through the Web at URL http://pauillac.inria.fr/caml/


KEEPING IN TOUCH WITH THE CAML COMMUNITY:

  There exists a mailing list of users of the Caml and Caml Light
  systems developed at INRIA. The purpose of this list is to share
  experience, exchange ideas (and even code), and report on applications
  of the Caml language. This list is moderated; messages can be
  written in English or in French. The list has about 200 subscribers.

  Messages to the list should be sent to:

                caml-list@inria.fr

  If you wish to subscribe to this list, please send a message
  (including your email address) to:

                caml-list-request@inria.fr

  The Usenet news group comp.lang.ml also contains discussions about
  the ML family of programming languages, including Caml. The newsgroup
  is moderated. For those without Usenet access, this newsgroup is
  also accessible via a mailing list (to subscribe:
  sml-list-request@cs.cmu.edu, to post a message: sml-list@cs.cmu.edu).

BUG REPORTS AND USER FEEDBACK:

  Send your bug reports by E-mail to

          caml-light@inria.fr

  or by paper mail to

          Caml Light, projet Formel
          INRIA Rocquencourt
          B.P. 105
          78153 Le Chesnay
          France

  To be effective, bug reports should include a complete program (preferably
  small) that exhibits the unexpected behavior, and the configuration
  you are using (machine type, etc).

  The mailing list caml-light@inria.fr is forwarded to a small
  group of implementors at INRIA. For general questions and discussions,
  caml-list@inria.fr is better; for bug reports and very specific
  technical questions, caml-light@inria.fr is preferred. We often
  cross-post from one list to the other, anyway.

