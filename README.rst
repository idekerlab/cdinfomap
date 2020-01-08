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

Packaged from https://www.mapequation.org/code.html

* A method based on Flux. Detect communities from dynamics on the network.
* Result hierarchy shallower than louvain, but can possess overlapping communites.
* Works on any graph
* Parameter `overlap`: true/false, whether allow overlapping communites to be detected. When set to true and the network is large, can render substantial increase in runtime. (default `false`)
* Parameter `direct`: true/false, whether the input network is directed or not. (default `false`)
* Parameter `markovtime`: a positive number indicating link flow/ cost of moving between modules. Higher for less communities. (default `0.75`)

Features
--------

* TODO

Credits
---------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
