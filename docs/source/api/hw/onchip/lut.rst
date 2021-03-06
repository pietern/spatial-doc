
.. role:: black
.. role:: gray
.. role:: silver
.. role:: white
.. role:: maroon
.. role:: red
.. role:: fuchsia
.. role:: pink
.. role:: orange
.. role:: yellow
.. role:: lime
.. role:: green
.. role:: olive
.. role:: teal
.. role:: cyan
.. role:: aqua
.. role:: blue
.. role:: navy
.. role:: purple

.. _LUT:

LUT
====



**LUTs** are on-chip, read-only memories of fixed size. LUTs can be specified as 1 to 5 dimensional.

LUTs can be created from files using the ``fromFile`` methods in the LUT object. This file reading is currently done at compilation time.

---------------

**Static methods**

+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| object     **LUT**                                                                                                                                                                                                                                                                                                                                                                           |
+==========+===================================================================================================================================================================================================================================================================================================================================================================================+
| |    def   **apply**\[T\::doc:`Type <../../typeclasses/type>`\::doc:`Bits <../../typeclasses/bits>`\]\(dim\: :doc:`Int <../../common/fixpt>`\)\(elems\: T\*\)\: :doc:`LUT1 <lut>`\[T\]                                                                                                                                                                                                       |
| |            Creates a 1-dimensional read-only lookup table with given elements.                                                                                                                                                                                                                                                                                                             |
| |            The number of supplied elements must match the given dimensions.                                                                                                                                                                                                                                                                                                                |
+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| |    def   **apply**\[T\::doc:`Type <../../typeclasses/type>`\::doc:`Bits <../../typeclasses/bits>`\]\(dim1\: :doc:`Int <../../common/fixpt>`, dim2\: :doc:`Int <../../common/fixpt>`\)\(elems\: T\*\)\: :doc:`LUT2 <lut>`\[T\]                                                                                                                                                              |
| |            Creates a 2-dimensional read-only lookup table with given elements.                                                                                                                                                                                                                                                                                                             |
| |            The number of supplied elements must match the given dimensions.                                                                                                                                                                                                                                                                                                                |
+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| |    def   **apply**\[T\::doc:`Type <../../typeclasses/type>`\::doc:`Bits <../../typeclasses/bits>`\]\(dim1\: :doc:`Int <../../common/fixpt>`, dim2\: :doc:`Int <../../common/fixpt>`, dim3\: :doc:`Int <../../common/fixpt>`\)\(elems\: T\*\)\: :doc:`LUT3 <lut>`\[T\]                                                                                                                      |
| |            Creates a 3-dimensional read-only lookup table with given elements.                                                                                                                                                                                                                                                                                                             |
| |            The number of supplied elements must match the given dimensions.                                                                                                                                                                                                                                                                                                                |
+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| |    def   **apply**\[T\::doc:`Type <../../typeclasses/type>`\::doc:`Bits <../../typeclasses/bits>`\]\(dim1\: :doc:`Int <../../common/fixpt>`, dim2\: :doc:`Int <../../common/fixpt>`, dim3\: :doc:`Int <../../common/fixpt>`, dim4\: :doc:`Int <../../common/fixpt>`\)\(elems\: T\*\)\: :doc:`LUT4 <lut>`\[T\]                                                                              |
| |            Creates a 4-dimensional read-only lookup table with given elements.                                                                                                                                                                                                                                                                                                             |
| |            The number of supplied elements must match the given dimensions.                                                                                                                                                                                                                                                                                                                |
+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| |    def   **apply**\[T\::doc:`Type <../../typeclasses/type>`\::doc:`Bits <../../typeclasses/bits>`\]\(dim1\: :doc:`Int <../../common/fixpt>`, dim2\: :doc:`Int <../../common/fixpt>`, dim3\: :doc:`Int <../../common/fixpt>`, dim4\: :doc:`Int <../../common/fixpt>`, dim5\: :doc:`Int <../../common/fixpt>`\)\(elems\: T\*\)\: :doc:`LUT5 <lut>`\[T\]                                      |
| |            Creates a 5-dimensional read-only lookup table with given elements.                                                                                                                                                                                                                                                                                                             |
| |            The number of supplied elements must match the given dimensions.                                                                                                                                                                                                                                                                                                                |
+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| |    def   **fromFile**\[T\::doc:`Type <../../typeclasses/type>`\::doc:`Bits <../../typeclasses/bits>`\]\(dim1\: :doc:`Int <../../common/fixpt>`\)\(filename\: :doc:`String <../../sw/string>`\)\: :doc:`LUT1 <lut>`\[T\]                                                                                                                                                                    |
| |            Creates a 1-dimensional read-only lookup table from the given data file.                                                                                                                                                                                                                                                                                                        |
| |            Note that this file is read during **compilation**, not runtime.                                                                                                                                                                                                                                                                                                                |
| |            The number of supplied elements must match the given dimensions.                                                                                                                                                                                                                                                                                                                |
+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| |    def   **fromFile**\[T\::doc:`Type <../../typeclasses/type>`\::doc:`Bits <../../typeclasses/bits>`\]\(dim1\: :doc:`Int <../../common/fixpt>`, dim2\: :doc:`Int <../../common/fixpt>`\)\(filename\: :doc:`String <../../sw/string>`\)\: :doc:`LUT2 <lut>`\[T\]                                                                                                                            |
| |            Creates a 2-dimensional read-only lookup table from the given data file.                                                                                                                                                                                                                                                                                                        |
| |            Note that this file is read during **compilation**, not runtime.                                                                                                                                                                                                                                                                                                                |
| |            The number of supplied elements must match the given dimensions.                                                                                                                                                                                                                                                                                                                |
+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| |    def   **fromFile**\[T\::doc:`Type <../../typeclasses/type>`\::doc:`Bits <../../typeclasses/bits>`\]\(dim1\: :doc:`Int <../../common/fixpt>`, dim2\: :doc:`Int <../../common/fixpt>`, dim3\: :doc:`Int <../../common/fixpt>`\)\(filename\: :doc:`String <../../sw/string>`\)\: :doc:`LUT3 <lut>`\[T\]                                                                                    |
| |            Creates a 3-dimensional read-only lookup table from the given data file.                                                                                                                                                                                                                                                                                                        |
| |            Note that this file is read during **compilation**, not runtime.                                                                                                                                                                                                                                                                                                                |
| |            The number of supplied elements must match the given dimensions.                                                                                                                                                                                                                                                                                                                |
+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| |    def   **fromFile**\[T\::doc:`Type <../../typeclasses/type>`\::doc:`Bits <../../typeclasses/bits>`\]\(dim1\: :doc:`Int <../../common/fixpt>`, dim2\: :doc:`Int <../../common/fixpt>`, dim3\: :doc:`Int <../../common/fixpt>`, dim4\: :doc:`Int <../../common/fixpt>`\)\(filename\: :doc:`String <../../sw/string>`\)\: :doc:`LUT4 <lut>`\[T\]                                            |
| |            Creates a 4-dimensional read-only lookup table from the given data file.                                                                                                                                                                                                                                                                                                        |
| |            Note that this file is read during **compilation**, not runtime.                                                                                                                                                                                                                                                                                                                |
| |            The number of supplied elements must match the given dimensions.                                                                                                                                                                                                                                                                                                                |
+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| |    def   **fromFile**\[T\::doc:`Type <../../typeclasses/type>`\::doc:`Bits <../../typeclasses/bits>`\]\(dim1\: :doc:`Int <../../common/fixpt>`, dim2\: :doc:`Int <../../common/fixpt>`, dim3\: :doc:`Int <../../common/fixpt>`, dim4\: :doc:`Int <../../common/fixpt>`, dim5\: :doc:`Int <../../common/fixpt>`\)\(filename\: :doc:`String <../../sw/string>`\)\: :doc:`LUT5 <lut>`\[T\]    |
| |            Creates a 5-dimensional read-only lookup table from the given data file.                                                                                                                                                                                                                                                                                                        |
| |            Note that this file is read during **compilation**, not runtime.                                                                                                                                                                                                                                                                                                                |
| |            The number of supplied elements must match the given dimensions.                                                                                                                                                                                                                                                                                                                |
+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


--------------

**Infix methods**

+----------------+---------------------------------+
| abstract class   **LUT**\[T\]                    |
+----------------+---------------------------------+



+----------+-----------------------------------------------------------+
| class      **LUT1**\[T\] extends LUT\[T\]                            |
+==========+===========================================================+
| |    def   **apply**\(i\: :doc:`Index <../../common/fixpt>`\)\: T    |
| |            Returns the element at the given address **i**.         |
+----------+-----------------------------------------------------------+



+----------+--------------------------------------------------------------------------------------------------+
| class      **LUT2**\[T\] extends LUT\[T\]                                                                   |
+==========+==================================================================================================+
| |    def   **apply**\(r\: :doc:`Index <../../common/fixpt>`, c\: :doc:`Index <../../common/fixpt>`\)\: T    |
| |            Returns the element at the given address **r**, **c**.                                         |
+----------+--------------------------------------------------------------------------------------------------+



+----------+-----------------------------------------------------------------------------------------------------------------------------------------+
| class      **LUT3**\[T\] extends LUT\[T\]                                                                                                          |
+==========+=========================================================================================================================================+
| |    def   **apply**\(r\: :doc:`Index <../../common/fixpt>`, c\: :doc:`Index <../../common/fixpt>`, p\: :doc:`Index <../../common/fixpt>`\)\: T    |
| |            Returns the element at the given 3-dimensional address.                                                                               |
+----------+-----------------------------------------------------------------------------------------------------------------------------------------+




+----------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| class      **LUT4**\[T\] extends LUT\[T\]                                                                                                                                                 |
+==========+================================================================================================================================================================================+
| |    def   **apply**\(r\: :doc:`Index <../../common/fixpt>`, c\: :doc:`Index <../../common/fixpt>`, p\: :doc:`Index <../../common/fixpt>`, q\: :doc:`Index <../../common/fixpt>`\)\: T    |
| |            Returns the element at the given 4-dimensional address.                                                                                                                      |
+----------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+



+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| class      **LUT5**\[T\] extends LUT\[T\]                                                                                                                                                                                        |
+==========+=======================================================================================================================================================================================================================+
| |    def   **apply**\(r\: :doc:`Index <../../common/fixpt>`, c\: :doc:`Index <../../common/fixpt>`, p\: :doc:`Index <../../common/fixpt>`, q\: :doc:`Index <../../common/fixpt>`, m\: :doc:`Index <../../common/fixpt>`\)\: T    |
| |            Returns the element at the given 5-dimensional address.                                                                                                                                                             |
+----------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


