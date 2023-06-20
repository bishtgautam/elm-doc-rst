# Overview

This is a test repository to explore options for developing documentation for
the E3SM Land Model. 

- The guide in this repo is written in [reStructured Text (RST)](https://en.wikipedia.org/wiki/ReStructuredText).
- [Sphinx](https://www.sphinx-doc.org/) is used to generate the html pages based on RST.
- The html version of the guide is available on [ReadTheDocs](https://elm-doc-rst.readthedocs.io/en/latest/).
- The guide on ReadTheDocs is automatically updated when the `main` branch of this repo is updated.

# Building the guide locally

Assuming `sphinx-build` is installed on the machine, the html version of the manuscript
can be build via

```
cd docs
make html
```
