===================================================
Community Detection Infomap
===================================================

.. image:: https://img.shields.io/pypi/v/cdinfomap.svg
        :target: https://pypi.python.org/pypi/cdinfomap

.. image:: https://img.shields.io/travis/idekerlab/cdinfomap.svg
        :target: https://travis-ci.org/idekerlab/cdinfomap

.. image:: https://readthedocs.org/projects/cdinfomap/badge/?version=latest
        :target: https://cdinfomap.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status

.. image:: https://requires.io/github/idekerlab/cdinfomap/requirements.svg?branch=master
        :target: https://requires.io/github/idekerlab/cdinfomap/requirements?branch=master
        :alt: Dependencies

This repository creates a CDAPS compatible community detection Docker image using Infomap
packaged from https://www.mapequation.org/code.html

* A method based on Flux. Detect communities from dynamics on the network.
* Result hierarchy shallower than louvain, but can possess overlapping communites.
* Works on any graph
* Parameter `overlap`: true/false, whether allow overlapping communites to be detected. When set to true and the network is large, can render substantial increase in runtime. (default `false`)
* Parameter `direct`: true/false, whether the input network is directed or not. (default `false`)
* Parameter `markovtime`: a positive number indicating link flow/ cost of moving between modules. Higher for less communities. (default `0.75`)

Dependencies
------------

* `Docker <https://www.docker.com/>`_
* `make <https://www.gnu.org/software/make/>`_ (to build)
* Python (to build)

Direct invocation
------------------

Version `0.1.0` can be directly pulled from dockerhub with this command:

.. code-block::

   docker pull coleslawndex/cdinfomap:0.1.0

Building
--------

.. code-block::

   git clone https://github.com/idekerlab/cdinfomap
   cd cdinfomap
   make dockerbuild

Run **make** command with no arguments to see other build/deploy options including creation of Docker image

.. code-block::

   make

Output:

.. code-block::

   clean                remove all build, test, coverage and Python artifacts
   clean-build          remove build artifacts
   clean-pyc            remove Python file artifacts
   clean-test           remove test and coverage artifacts
   lint                 check style with flake8
   test                 run tests quickly with the default Python
   test-all             run tests on every Python version with tox
   coverage             check code coverage quickly with the default Python
   docs                 generate Sphinx HTML documentation, including API docs
   servedocs            compile the docs watching for changes
   testrelease          package and upload a TEST release
   release              package and upload a release
   dist                 builds source and wheel package
   install              install the package to the active Python's site-packages
   dockerbuild          build docker image and store in local repository
   dockerpush           push image to dockerhub


Usage
-----

.. code-block::

   docker run -v coleslawndex/cdinfomap:0.1.0 -h

Credits
---------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
