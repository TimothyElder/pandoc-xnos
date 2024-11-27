
pandoc-xnos
===========

This is a forked version of `pandoc-xnos` created by @tomduck. It has a single digit difference from the master branch version of `pandoc-xnos` which fixes a regex that reads the pandoc version number. See [tomduck/pandoc-xnos#28](https://github.com/tomduck/pandoc-xnos/issues/28) for more information.

The *pandoc-xnos* filter suite provides facilities for cross-referencing in markdown documents processed by [pandoc]. Individual filters are maintained in separate projects.  They are:

* [pandoc-fignos]: Numbers figures and figure references.
* [pandoc-eqnos]: Numbers equations and equation references.
* [pandoc-tablenos]: Numbers tables and table references.
* [pandoc-secnos]: Numbers section references (sections are
  numbered by pandoc itself).

Click on the above links to access documentation for each filter.   LaTeX/pdf, html, and epub output have native support.  Native support for docx output is a work in progress.

This project provides library code for the suite and a `pandoc-xnos` filter that applies all of the above filters in sequence.

See also: [pandoc-comments], [pandoc-latex-extensions]

[pandoc]: http://pandoc.org/
[pandoc-fignos]: https://github.com/tomduck/pandoc-fignos
[pandoc-eqnos]: https://github.com/tomduck/pandoc-eqnos
[pandoc-tablenos]: https://github.com/tomduck/pandoc-tablenos
[pandoc-secnos]: https://github.com/tomduck/pandoc-secnos
[pandoc-comments]: https://github.com/tomduck/pandoc-comments
[pandoc-latex-extensions]: https://github.com/tomduck/pandoc-latex-extensions


Contents
--------

 1. [Installation](#installation)
 2. [Usage](#usage)

Installation
------------

The Pandoc-xnos filters require [python].  It is easily installed -- see [here](https://realpython.com/installing-python/). Either python 2.7 or 3.x will do.

The forked version of pandoc-xnos filter suite may be installed using the shell command

    pip install git+https://github.com/TimothyElder/pandoc-xnos

**Be sure to add the location of the binaries to your PATH**. They are usually installed in `/Users/your-user-name/Library/Python/3.9/bin`.

Pip is a program that downloads and installs software from the Python Package Index, [PyPI].

Instructions for installing from source are given in [DEVELOPERS.md].

[python]: https://www.python.org/
[PyPI]: https://pypi.python.org/pypi
[DEVELOPERS.md]: DEVELOPERS.md


Usage
-----

The pandoc-xnos filter suite may be applied using the

    --filter pandoc-xnos

option with pandoc.  It is also possible to apply the filters individually.

Any use of `--filter pandoc-citeproc` or `--bibliography=FILE` should come *after* the `pandoc-xnos` filter call.
