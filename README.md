# ATI-ResComp-Service-docs

Source for documentation for the Alan Turing Institute Research Computing Service, data science platforms hosted by [EPCC](http://www.epcc.ed.ac.uk) for the [Alan Turing Institute](http://www.turing.ac.uk).

For the current, rendered, documentation, see [Alan Turing Institute Research Computing Service](http://ati-rescomp-service-docs.readthedocs.io/en/latest/index.html) on [Read the Docs](https://readthedocs.org).

The [Sphinx](http://www.sphinx-doc.org/) Python documentation generator is used to create HTML documentation from these sources.

## Prerequisites (Linux or Mac)

Install Anaconda Python 2.7 (or 3.6):

* See [Download Anaconda Distribution](https://www.anaconda.com/download/).

## Get the sources

Fork this repository on GitHub into your own user account.

Clone your fork e.g.

```bash
$ git clone https://github.com/your-github-username/ATI-ResComp-Service-docs
```

## Build HTML

Change into to the directory containing the user guide:

```bash
$ cd ATI-ResComp-Service-docs
```

Build the HTML pages:

```bash
$ make html
```

The HTML version of the documentation will be placed in `_build/html/`, with an entry point of `_build/html/index.html`.

## Edit documentation

Documentation is written in plain-text [reStructuredText](http://docutils.sourceforge.net/rst.html) format. For a summary of its notation, see the [reStructuredText Primer](http://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html).

Commit changes to your Git repository, remembering to use meaningful commit messages.

## Contribute updates.

Push changes back to your forked repository on GitHub.

Issue a pull request to this repository.

The documentation maintainers will review your changes and either merge them or let them know what you need to resolve.
