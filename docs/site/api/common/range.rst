
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

.. _Range:

Range
=====

@alias Range

Range represents a sequence of 32b integer values from a given *start* (inclusive) to *end* (exclusive) with a non-zero step size.
Range also has an optional parallelization factor, which is used to determine physical unrolling in hardware.

In Accel scopes, Range instances can be implicitly converted to @Counter.

Ranges can be created using two different syntax flavors. When unspecified, the default value for `start` is 0, and
the default value for `step` and `par` are both 1.

Form 1::

    val range1 = max by step        // start of 0, step by 1, parallelization of 1
    val range2 = start until max    // start of 0, step by 1, parallelization of 1
    val range3 = start until max by step par p


Form 2::

    val range4 = start :: end       // Step of 1, parallelization of 1
    val range5 = start :: step :: end par p

**Form 1** is typically used for specifying the domain of a loop, while **Form 2** is used
for Matlab-like syntax when selecting a range of elements from a memory.

Ranges can also be used to create Scala-like for loops on the CPU:::

    for (i <- 0 until max by 2) {
        ..
    }

This loop will run for all even integers from \[0, max). Note that this syntax is only usable on the CPU or in simulation.

--------

**Infix methods**

@table-start
class Range

  /** Returns the length of this Range. **/
  @api def length: Index

  /** Creates a Range with this Range's start and end but with the given `step` size. **/
  @api def by(step: Index): Range = Range(start, end, Some(step), p, isUnit = false)
  /** Creates a Range with this Range's start, end, and stride, but with the given `par` parallelization factor. **/
  @api def par(p: Index): Range = Range(start, end, step, Some(p), isUnit = false)

  /**
    * Creates a Range with this Range's end, with the previous start as the step size, and the given start.
    * Note that this operator is right-associative.
    */
  @api def ::(start2: Index): Range = Range(Some(start2), end, start, p, isUnit = false)

  /**
    * Iterates over all integers in this range, calling `func` on each.
    *
    * `NOTE`: This method is unsynthesizable, and can be used only on the CPU or in simulation.
    */
  @api def foreach(func: Index => MUnit): MUnit = {

@table-end


----------------


**Implicit methods**

@table-start
NoHeading

  /** Implicitly creates a hardware @Counter from this Range. **/
  @api def rangeToCounter(range: Range): Counter

@table-end

