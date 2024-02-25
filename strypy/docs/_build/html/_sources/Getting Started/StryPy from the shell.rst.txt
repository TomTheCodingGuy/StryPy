=====================
StryPy from the shell
=====================

Running StryPy in a shell environment is very easy and useful for any quick Python code you want to run, and provides a simple way to view the docstrings of the package. 

Importing
=========

To import the package use:
    >>> import strypy as sp
    >>> . . .

Useful commands
===============

To view the docstrings of any function or module (or the whole package) use:
    >>> print(sp.function-or-module.__doc__)
    >>> # Real example
    >>> print(sp.add.__doc__)
          '''
          Adds strings together, with spaces optional.
          >>> sp.add("hello", "world", spaces=True)
          'hello world'
          '''
          
To import only specific module use:
    >>> import strypy.basics as sb
    >>> . . .
    
To simply call a function use:
    >>> sp.add("Hello", "World")
    'Hello World'
    
    
A Real-World Example
====================

This small example demonstrates StryPy's quick and easy shell use to generate a random password and copy it to the clipboard for use:
    >>> import strypy as sp                                 # Imports StryPy
    >>> password = sp.randstr(minlength=8, maxlength=15)    # Creates random password
    >>> sp.copy(password)                                   # Copys password to clipboard