0.1.0b2
=======

.. warning::

 | period_cut (in seconds) has been replaced by high_pass (in Hz) in FirstLevelModel & design matrices.
 | This is a code-breaking change. Please update your code accordingly.

New
---

* Use :func:`nistats.reporting.make_glm_report` to easily generate HTML reports from fitted first and second level models and contrasts.

Fixes
-----

* Removed Python 2 deprecation warning for Python 3 installations.
* fixed effect contrasts now average effect sizes across runs rather than
  summing them.

Contributors
------------


0.0.1b
=======

Changelog
---------

* Updated the minimum versions of the dependencies
    * Numpy >= 1.11
    * SciPy >= 0.17
    * Nibabel >= 2.0.2
    * Nilearn >= 0.4.0
    * Pandas >= 0.18.0
    * Sklearn >= 0.18.0

* Added comprehensive tutorial

* Second-level model accepts 4D images as input.

* Changes in function parameters
    * third argument of map_threshold is now called ``level``.
    * Changed the defaut oversampling value for the hemodynamic response
      to 50 and exposed this parameter.
    * changed the term ``paradigm`` to ``events`` and made it
      BIDS-compliant. Set the event file to be tab-separated
    * ``FirstLevelModel.compute_contrasts`` parameter ``output_type`` can
      take the value ``'all'``, returning a dictionary of images for each
      output type

* Certain functions and methods have been renamed for clarity
    * ``nistats.design_matrix``
        * ``make_design_matrix() -> make_first_level_design_matrix()``
        * ``create_second_level_design() -> make_second_level_design_matrix()``
    * ``nistats.utils``
        * ``pos_recipr() -> positive_reciprocal()``
        * ``multiple_fast_inv() -> multiple_fast_inverse()``

* Python2 Deprecation:
    Python 2 is now deprecated and will not be supported in a future version.
    A DeprecationWarning is displayed in Python 2 environments with a suggestion to move to Python 3.


Contributors
------------

The following people contributed to this release::

    45  Bertrand Thirion
    70  Kshitij Chawla
    16  Taylor Salo
     6  KamalakerDadi
     5  chrplr
     5  hcherkaoui
     5  rschmaelzle
     4  mannalytics
     3  Martin Perez-Guevara
     2  Christopher J. Markiewicz
     1  Loïc Estève



0.0.1a
=======

Changelog
---------

First alpha release of nistats.

Contributors (from ``git shortlog -ns``)::

   223  Martin Perez-Guevara
   195  bthirion
    24  Gael Varoquaux
     9  Loïc Estève
     3  AnaLu
     2  Alexandre Gramfort
     1  DOHMATOB Elvis
     1  Horea Christian
     1  Michael Hanke
     1  Salma
     1  chrplr
