
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

.. _Tuple2:

Tuple2
========

@alias Tuple2

Tuple2[A,B] is a simple data structure used to hold a pair of staged values.

Note that this name shadows the unstaged Scala type. For the unstaged type, use the full name scala.Tuple2[A,B]

-----------

**Infix methods**

@table-start
class Tuple2[A,B]

  /** Returns the first field in this Tuple2. **/
  @api def _1: A

  /** Returns the second field in this Tuple2. **/
  @api def _2: B

  /** 
    * Returns a printable String from this value. 
    *
    * `NOTE`: This method is unsynthesizable and can only be used on the CPU or in simulation. 
    **/
  @api def toString: String

----------

**Related methods**

@table-start
NoHeading

  /** Returns a staged Tuple2 from the given unstaged Tuple2. **/
  @api def pack[A:Type,B:Type](t: (A, B)): MTuple2[A,B] = MTuple2.pack(t)

  /** Returns a staged Tuple2 from the given pair of values. Shorthand for ``pack((a,b))``. **/
  @api def pack[A:Type,B:Type](a: A, b: B): MTuple2[A,B] = MTuple2.pack(a,b)

  /** Returns an unstaged scala.Tuple2 from this staged Tuple2. Shorthand for ``(x._1, x._2)``. **/
  @api def unpack[A:Type,B:Type](t: MTuple2[A,B]): (A,B) = (t._1, t._2)

@table-end

