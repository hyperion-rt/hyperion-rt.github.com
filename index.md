---
layout: default
title: Hyperion
tagline: Monte-Carlo dust continuum radiative transfer
---

About
-----

Hyperion is a parallelized three-dimensional dust continuum radiative transfer code (see Robitaille et al., 2011 for details). The main features include:

* Dust continuum radiative transfer
* SEDs, images, and polarization maps
* Arbitrary 3-d geometry
* Multiple sources and dust populations
* Arbitrary dust properties
* Cartesian, Polar, and Adaptive grids (Octree and AMR)
* Easy-to-use Python library to set up, run, and post-process models
* High performance parallelized Fortran 2003 core

Example
-------

{% highlight python %}
from hyperion.model import Model

m = Model()

s = m.add_spherical_source()
s.radius = rsun
s.spectrum = (nu, fnu)
s.luminosity = lsun

m.set_spherical_polar_grid(r_wall, t_wall, p_wall)

m.add_density_grid(density, 'dust_file.hdf5')

m.set_n_photons(initial=100000, imaging=10000)

m.write('model.rtin')
m.run('model.rtout')
{% endhighlight %}

Getting started
---------------

The current version of Hyperion is 0.9.0. The source code can be downloaded [here](http://www.github.com/hyperion-rt/hyperion/downloads) and installation instructions are provided in the [documentation](http://docs.hyperion-rt.org/installation/installation.html).

Documentation
-------------

The documentation for Hyperion is can be found at http://docs.hyperion-rt.org

Reporting issues
----------------

If you encounter any issues with the code, or have requests for new features,
please open a new feature on the GitHub [issue tracker](http://www.github.com/hyperion-rt/hyperion/issues) . Please resolve installation issues with your system administrator, as they are likely due to issues with the dependencies - however, if you think you have encountered a genuine bug in the installation, please do report it.

Contributing
------------

In addition to reporting issues with the code or the documentation, code and
documentation contributions are welcome. Please read the [following](http://docs.hyperion-rt.org/contributing>) page for more details on how to
contribute code.

