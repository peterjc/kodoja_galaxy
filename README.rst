.. image:: https://travis-ci.org/abaizan/kodoja_galaxy.svg?branch=master
   :alt: Linux testing with TravisCI
   :target: https://travis-ci.org/abaizan/kodoja_galaxy/branches

This is a Galaxy wrapper for the tool Kodoja, which is available to install in
conda from bioconda.

https://github.com/abaizan/kodoja

Galaxy wrappers for Kodoja
==========================

These wrappers are copyright 2018 by Amanda Baizan Edge (University of
St Andrews, and The James Hutton Institute) and Peter Cock (The James
Hutton Institute). They are released under the MIT licence.

These wrappers are available from the Galaxy Tool Shed at:
http://toolshed.g2.bx.psu.edu/view/abaizan/kodoja

In-development test releases are available from the Test Tool Shed at:
http://testtoolshed.g2.bx.psu.edu/view/abaizan/kodoja


Citation
========

Please refer to the main Kodoja citation instructions.


Automated Installation
======================

Galaxy should be able to automatically install the dependencies, namely
``kodoja`` and its dependencies like ``kraken`` and ``kaiju``, using the
conda and the bioconda recipes.

See the configuration notes below.


Configuration
=============

You must tell Galaxy about any Kraken and Kaiju databases using configuration
files ``kraken_databases.loc`` and ``kaiju_databases.loc`` which are located
in the ``tool-data/`` folder. Sample files are included which explain the
tab-based format to use.


History
=======

======= ======================================================================
Version Changes
------- ----------------------------------------------------------------------
v0.0.0  - Initial release covering ``kodoja_search.py`` v0.0.3.
======= ======================================================================


Bug Reports
===========

File a Galaxy wrapper issue at https://github.com/abaizan/kodoja_galaxy/issues

For issues with Kodoja itself, use https://github.com/abaizan/kodoja/issues


Developers
==========

For pushing a release to the test or main "Galaxy Tool Shed", use the
following Planemo commands (which requires you have set your Tool Shed access
details in ``~/.planemo.yml`` and that you have access rights on the Tool
Shed)::

    $ planemo shed_update -t testtoolshed --check_diff .
    ...

or::

    $ planemo shed_update -t toolshed --check_diff .
    ...

To just build and check the tar ball, use::

    $ planemo shed_upload -t testtoolshed --tar_only .
    ...
    $ tar -tzf shed_upload.tar.gz
    LICENSE
    README.rst
    ...

This simplifies ensuring a consistent set of files is bundled each time,
including all the relevant test files.


Licence (MIT)
=============

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
