===================
StryPy in a program
===================

StryPy can also be used as part of a larger program in a Python file. In this small project we will implement it in a file path splitter and editor for Linux and Mac.

First import the neccessary packages:

.. code-block:: python
   :linenos:
   
   import strypy as sp
   
Then create the function to split a file path to get a list of directorys:

.. code-block:: python
   :lineno-start: 2
   
   def split_path(path):
       return sp.split(path,'/')
       
And the function to go back a directory:

.. code-block:: python
   :lineno-start: 4
   
   def back(path, copy=False):
       split = split_path(path)
       new_split = split.pop()
       new_path = sp.join(new_split, between='/')
       
       if copy == True:
           sp.copy(new_path)
           
       return new_path
       
Add a new directory on the end:

.. code-block::
   :lineno-start: 13
   
   def add_path(path, add, copy=False):
       new_path = sp.add(path, "/", str(add))
       
       if copy == True:
           sp.copy(new_path)
       
       return new_path