# TYPO3 Extension "adodb"

Ships the PHP database abstraction library "adodb" which is mainly used by the TYPO3
extension "dbal".

The functionality was part of TYPO3, until TYPO3 v8.4, and moved into its own
extension, receiving its own public repository.

## Installation
The latest version can be installed via TER (http://typo3.org) or via composer
by adding ''composer require friendsoftypo3/adodb'' in a TYPO3 v8.4+ installation.

## Current state
This extension provides a wrapper for adodb plus some patched changes which were
needed for "dbal" and TYPO3 until v8.4. It is shipped as is.

## Contribution
Feel free to submit any pull request, or add documentation, tests, as you please.
We will publish a new version every once in a while, depending on the amount of changes
and pull requests submitted.

### License
The extension is published under GPL v2+, all included third-party libraries are
published under their respective licenses.

### Authors
Over a dozen contributors have been working on this area while this functionality was part of
the TYPO3 Core. This package is now maintained by a loose group of TYPO3 enthusiasts inside
the TYPO3 Community. Feel free to contact Benni Mack (benni.mack@typo3.org) for any questions
regarding "adodb".
