Testing API
===========

StryPy features a simple testing utility with a function to get the test directory path. For the full testing guide visit :any:`Testing`.

.. function:: sp.get_test_path()

    *Returns the path to the test directory*
    
    This function just returns the path of the test directory which is used to run tests:
        >>> sp.get_test_path()
        '/path/to/test/directory'