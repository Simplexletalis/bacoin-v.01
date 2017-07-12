Bacoin integration/staging tree
================================

http://www.bacoin.org

Copyright (c) 2009-2013 Bitcoin Developers
Copyright (c) 2017-2017 Bacoin Developers


Gitter:
https://gitter.im/Bacoins/Lobby


Testing clients Bacoind and bacoin-qt download:
https://drive.google.com/open?id=0Byoh2-GPva0eYmVsb0d6NHpPWEk






Anything below this may be innacurate and needs to be updated.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

What is Bacoin?
----------------

Bacoin is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 1 minute block targets
 - ~5 million total coins
 - 5 coins per block

For more information, as well as an immediately useable, binary version of
the Bacoin client sofware, see http://www.bacoin.org.

License
-------

Bacoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Bacoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on
https://gitter.im/Bacoins/Lobby

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./bacoin-qt_test

