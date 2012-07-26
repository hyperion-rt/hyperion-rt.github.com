---
layout: default
title: Hyperion
tagline: Monte-Carlo dust continuum radiative transfer
---

Getting started
---------------

Hyperion is a parallelized 3-d dust continuum radiative transfer code. The code is described in [Robitaille (2011)](http://dx.doi.org/10.1051/0004-6361/201117150). Its main features include:

* Dust continuum radiative transfer
* Dust temperature calculation
* SEDs, images, and polarization maps
* Support for arbitrary 3-d geometry
* Support for multiple sources and dust populations
* Support for arbitrary dust properties
* Cartesian, Polar, and Adaptive grids (Octree and AMR)
* Easy-to-use Python library to set up, run, and post-process models
* High performance parallelized (MPI) Fortran 2003 core

The current stable version of Hyperion is 0.9.0 - [download](http://github.com/downloads/hyperion-rt/hyperion/hyperion-0.9.0.tar.gz)

The documentation and installation instructions are located at [http://docs.hyperion-rt.org](http://docs.hyperion-rt.org)

**Note**: If you decide to use the code, you should sign up to the mailing list in order to be informed when new versions are available:

<center>
<form action="http://groups.google.com/group/hyperion-announce/boxsubscribe">
  <input type="text" name="email" size='29' value='enter your email address here' onblur="if (this.value == '') {this.value = 'enter your email address here';}" onfocus="if (this.value == 'enter your email address here') {this.value = '';}"/>
  <input type="submit" name="sub" value="Subscribe to the mailing list"/>
</form>
</center>
<br>

If your work makes use of Hyperion, please cite the following publication: **Robitaille, 2011**, *HYPERION: an open-source parallelized three-dimensional dust continuum radiative transfer code*, Astronomy & Astrophysics 536 A79 - [ADS](http://adsabs.harvard.edu/abs/2011A%26A...536A..79R) - [BibTeX](http://adsabs.harvard.edu/cgi-bin/nph-bib_query?bibcode=2011A%26A...536A..79R&data_type=BIBTEX&db_key=AST&nocookieset=1)

Reporting issues
----------------

If you encounter any issues with the code, or have requests for new features,
please open a new ticket on the GitHub [issue tracker](http://www.github.com/hyperion-rt/hyperion/issues).
You can also send any questions/issues to [help@hyperion-rt.org](mailto:help@hyperion-rt.org).

Please try and resolve installation issues with your system administrator, as
they are likely due to issues with dependencies - however, if you think
you have encountered a genuine issue in the installation, please do report it.

Contributing
------------

In addition to reporting issues with the code or the documentation, code and
documentation contributions are welcome. Please read the [following](http://docs.hyperion-rt.org/en/latest/contributing.html) page for more details on how to
contribute code.

