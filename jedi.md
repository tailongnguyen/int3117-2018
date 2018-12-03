## Jedi - một thư viện tự động điền /phân tích tĩnh  cho Python

Jedi là một công cụ phân tích tĩnh cho Python có thể sử dụng cho cả IDE và Editor . Chức năng chủ yếu của nó là tự động điền cũng như phân tích tĩnh . Jedi chạy rất nhanh và được test rất cẩn thận. Nó có thể hiểu được các dòng code Python ở một mức sâu hơn các công cụ phân tích tĩnh khác.
Jedi sử dụng một API vô cùng đơn giản để giao tiếp với IDE, chính vì thế nó được gợi ý để sử dụng với các IDE. Các IDE được hỗ trợ bao gồm: Vim, Emacs, Sublime Text, Atom, Visual Studio Code, Gedit, Eric IDE, IPython, Kate.
Here are some pictures taken from jedi-vim_:

.. image:: https://github.com/davidhalter/jedi/raw/master/docs/_screenshots/screenshot_complete.png

Completion for almost anything (Ctrl+Space).

.. image:: https://github.com/davidhalter/jedi/raw/master/docs/_screenshots/screenshot_function.png

Display of function/class bodies, docstrings.

.. image:: https://github.com/davidhalter/jedi/raw/master/docs/_screenshots/screenshot_pydoc.png

Pydoc support (Shift+k).

There is also support for goto and renaming.

Get the latest version from `github <https://github.com/davidhalter/jedi>`_
(master branch should always be kind of stable/working).

Docs are available at `https://jedi.readthedocs.org/en/latest/
<https://jedi.readthedocs.org/en/latest/>`_. Pull requests with documentation
enhancements and/or fixes are awesome and most welcome. Jedi uses `semantic
versioning <https://semver.org/>`_.

If you want to stay up-to-date (News / RFCs), please subscribe to this `github
thread <https://github.com/davidhalter/jedi/issues/1063>`_.:



Installation
============

    pip install jedi

Note: This just installs the Jedi library, not the editor plugins. For
information about how to make it work with your editor, refer to the
corresponding documentation.

You don't want to use ``pip``? Please refer to the `manual
<https://jedi.readthedocs.org/en/latest/docs/installation.html>`_.


Feature Support and Caveats
===========================

Jedi really understands your Python code. For a comprehensive list what Jedi
understands, see: `Features
<https://jedi.readthedocs.org/en/latest/docs/features.html>`_. A list of
caveats can be found on the same page.

You can run Jedi on CPython 2.7 or 3.4+ but it should also
understand/parse code older than those versions. Additionally you should be able
to use `Virtualenvs <https://jedi.readthedocs.org/en/latest/docs/api.html#environments>`_
very well.

Tips on how to use Jedi efficiently can be found `here
<https://jedi.readthedocs.org/en/latest/docs/features.html#recipes>`_.

API
---

You can find the documentation for the `API here <https://jedi.readthedocs.org/en/latest/docs/api.html>`_.


Autocompletion / Goto / Pydoc
-----------------------------

Please check the API for a good explanation. There are the following commands:

- ``jedi.Script.goto_assignments``
- ``jedi.Script.completions``
- ``jedi.Script.usages``

The returned objects are very powerful and really all you might need.


Autocompletion in your REPL (IPython, etc.)
-------------------------------------------

Starting with IPython `6.0.0` Jedi is a dependency of IPython. Autocompletion
in IPython is therefore possible without additional configuration.

It's possible to have Jedi autocompletion in REPL modes - `example video <https://vimeo.com/122332037>`_.
This means that in Python you can enable tab completion in a `REPL
<https://jedi.readthedocs.org/en/latest/docs/usage.html#tab-completion-in-the-python-shell>`_.


Static Analysis / Linter
------------------------

To do all forms of static analysis, please try to use ``jedi.names``. It will
return a list of names that you can use to infer types and so on.

Linting is another thing that is going to be part of Jedi. For now you can try
an alpha version ``python -m jedi linter``. The API might change though and
it's still buggy. It's Jedi's goal to be smarter than classic linter and
understand ``AttributeError`` and other code issues.


Refactoring
-----------

Jedi's parser would support refactoring, but there's no API to use it right
now.  If you're interested in helping out here, let me know. With the latest
parser changes, it should be very easy to actually make it work.


Development
===========

There's a pretty good and extensive `development documentation
<https://jedi.readthedocs.org/en/latest/docs/development.html>`_.


Testing
=======

The test suite depends on ``tox`` and ``pytest``::

    pip install tox pytest

To run the tests for all supported Python versions::

    tox
