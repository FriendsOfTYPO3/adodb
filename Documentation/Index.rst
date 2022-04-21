.. include:: /Includes.rst.txt

====================
Integration of ADOdb
====================

:Extension key:
   adodb

:Package name:
   friendsoftypo3/adodb

:Version:
   |release|

:Language:
   en

:Author:
   TYPO3 contributors

:License:
   This document is published under the
   `Creative Commons BY 4.0 <https://creativecommons.org/licenses/by/4.0/>`__
   license.

:Rendered:
   |today|

----

This extension ships the PHP database abstraction library *ADOdb* which is
mainly used by the TYPO3 extension `dbal`_.

The functionality was part of TYPO3, until TYPO3 v8.4, and moved into its own
extension, receiving its own public repository.

.. _dbal: https://extensions.typo3.org/extension/dbal/

----

**Table of Contents:**

.. contents::
   :backlinks: top
   :depth: 2
   :local:

Installation
============

The latest version can be installed via `TER`_ or via composer by running

.. code-block:: bash

   composer require friendsoftypo3/adodb

in a TYPO3 v8.4+ installation.

.. _TER: https://extensions.typo3.org/extension/adodb/

Current state
=============

This extension provides a wrapper for ADOdb plus some patched changes which were
needed for the TYPO3 extension dbal and TYPO3 until v8.4. It is shipped as is.

Contribution
============

Feel free to submit any pull request, or add documentation, tests, as you please.
We will publish a new version every once in a while, depending on the amount of
changes and pull requests submitted.

License
-------

The extension is published under GPL v2+, all included third-party libraries are
published under their respective licenses.

Authors
-------

Over a dozen contributors have been working on this area while this
functionality was part of the TYPO3 Core. This package is now maintained by a
loose group of TYPO3 enthusiasts inside the TYPO3 Community. Feel free to
contact them by clicking the "Contact" link in the footer.

Changes made to ADOdb
=====================

Now in use
----------

The currently used ADOdb version is 5.19 [1]_.

.. [1] https://github.com/ADOdb/ADOdb/releases/tag/v5.19

Our changes
-----------

This is a list of changes we made in ADOdb that must re-applied if EXT:adodb is
updated to upstream.

- ADOdb: Invalid override method signature (48034_) (Solved in 5.20-dev [2]_)
- ADOdb: Set charset properly (61738_)
- EXT:adodb: Table names in ALTER TABLE broken (63659_)
- MSSQL native driver for ADOdb returns erroneous message (66674_)
- ADOdb: mssqlnative driver fails to create sequences (66678_)
- ADOdb: mssqlnative driver is not properly initialized (66830_)
- ADOdb: mssqlnative driver does not properly define the port (63070_)
- ADOdb: Allow setting NOT NULL/DEFAULT on blob and text columns (67442_) (Upstream pull request: [3]_)
- ADOdb: Table names in sequences broken (64990_)
- ADOdb: PHP7 redefinition of parameter (71244_)
- Security: XML entity expansion (61269_)

.. [2] https://github.com/ADOdb/ADOdb/commit/85f05a98974ea85ecae943faf230a27afdbaa746
.. [3] https://github.com/ADOdb/ADOdb/pull/118
.. _48034: https://forge.typo3.org/issues/48034
.. _61738: https://forge.typo3.org/issues/61738
.. _63659: https://forge.typo3.org/issues/63659
.. _66674: https://forge.typo3.org/issues/66674
.. _66678: https://forge.typo3.org/issues/66678
.. _66830: https://forge.typo3.org/issues/66830
.. _63070: https://forge.typo3.org/issues/63070
.. _67442: https://forge.typo3.org/issues/67442
.. _64990: https://forge.typo3.org/issues/64990
.. _71244: https://forge.typo3.org/issues/71244
.. _61269: https://forge.typo3.org/issues/61269

Diff
----

You'll find a diff file in EXT:adodb/Documentation/typo3-adodb.diff.
