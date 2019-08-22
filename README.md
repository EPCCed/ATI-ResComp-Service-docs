# ATI-ResComp-Service-docs

[![docs](https://readthedocs.org/projects/ati-rescomp-service-docs/badge/?version=latest)](http://ati-rescomp-service-docs.readthedocs.io/?badge=latest)

## Overview

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
$ git clone https://github.com/<your-github-username>/ATI-ResComp-Service-docs
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

Documentation is written in plain-text [reStructuredText](http://docutils.sourceforge.net/rst.html) format. For a summary of its notation, see the [reStructuredText Primer](http://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html)

Commit changes to your Git repository, remembering to use meaningful commit messages.

## Edit images

Image sources are in [images-src/](./images-src) as SVG files.

If you have created a new SVG file, export the SVG as a PNG file and add both to the repository.

If you have updated an existing SVG file, export the SVG to update the corresponding PNG file, add commit the updates to the repository.

### Edit images using Inkscape

[Inkscape](https://inkscape.org/en/) is a free SVG editor which can be used to edit SVG files and export the images as PNG files.

To export an image as PNG:

* Select File => Export PNG Image...

To set the default background for an image:

* Select File => Document Properties...
* Click square next to background colour.
* Set R, G, B, A components.
* For a white background, set R, G, B, A to 255.
* For a transparent background, set R, G, B to 255 and A to 0.

To install additional symbols (e.g. from inkscape-open-symbols below):

* Download symbols as SVGs.
* Copy to Inkscape's `share/symbols` directory.
  - For example, on Windows, `C:\Program Files\Inkscape\share\symbols`.

### Third-party symbols in images

Some SVG images used symbols which were sourced as follows.

**Inkscape open symbols**

See [inkscape-open-symbols](https://github.com/Xaviju/inkscape-open-symbols) on GitHub.

Icons from the following sets have been used:

* GitHub Octicons, MIT licence, `inkscape-open-symbols/octicons/octicons.svg`
* Google Material Design Icons [File Set], Apache 2.0 licence, `inkscape-open-symbols/
material-design/material-design-file.svg`
* Google Material Design Icons [Hardware Set], Apache 2.0 licence, `inkscape-open-symbols/material-design/material-design-hardware.svg`

**Docker logos**

See [Docker brand guidelines](https://www.docker.com/legal/brand-guidelines).

An icon (`docker_logos_2018/CMYK/Monochomatic/AI/vertical.ai`) from [docker_logos_2018.zip](https://www.docker.com/sites/default/files/legal/docker_logos_2018.zip) is used.

Reuse is permitted under conditions documented on the brand guidelines page.

## Contribute updates.

Push changes back to your forked repository on GitHub.

Issue a pull request to this repository.

The documentation maintainers will review your changes and either merge them or let them know what you need to resolve.
