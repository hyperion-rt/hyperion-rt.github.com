---
layout: default
title: Hyperion
tagline: Monte-Carlo dust continuum radiative transfer
---

Getting started
---------------

Hyperion is a parallelized three-dimensional dust continuum radiative transfer code. The code is described in [Robitaille (2011)](http://dx.doi.org/10.1051/0004-6361/201117150). Its main features include:

* Dust continuum radiative transfer
* SEDs, images, and polarization maps
* Support for arbitrary 3-d geometry
* Support for multiple sources and dust populations
* Support for arbitrary dust properties
* Cartesian, Polar, and Adaptive grids (Octree and AMR)
* Easy-to-use Python library to set up, run, and post-process models
* High performance parallelized (MPI) Fortran 2003 core

The current stable version of Hyperion is 0.9.0. The source code can be downloaded [here](http://www.github.com/hyperion-rt/hyperion/downloads). The documentation, which includes installation instructions, is located at [http://docs.hyperion-rt.org](http://docs.hyperion-rt.org)

**Note**: If you decide to use the code, you should sign up to the mailing list in order to be informed when new versions are available:

<center>
<form action="http://groups.google.com/group/hyperion-announce/boxsubscribe">
  <input type="text" name="email" size='29' value='enter your email address here' onblur="if (this.value == '') {this.value = 'enter your email address here';}" onfocus="if (this.value == 'enter your email address here') {this.value = '';}"/>
  <input type="submit" name="sub" value="Subscribe to the mailing list"/>
</form>
</center>
<br>

Reporting issues
----------------

If you encounter any issues with the code, or have requests for new features,
please open a new ticket on the GitHub [issue tracker](http://www.github.com/hyperion-rt/hyperion/issues).
Please resolve try and installation issues with your system administrator, as
they are likely due to issues with the dependencies - however, if you think
you have encountered a genuine bug in the installation, please do report it.

If you prefer, you can send any questions/issues to [help@hyperion-rt.org](mailto:help@hyperion-rt.org)!

Example model
-------------

Hyperion does not use parameter files, which are too restrictive. Instead, models are set up via Python scripts. The following code demonstrates how the Python Hyperion library can be used to easily set up a simple arbitrary model. The code interface focuses on being human-readable while being very flexible:

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

Contributing
------------

In addition to reporting issues with the code or the documentation, code and
documentation contributions are welcome. Please read the [following](http://docs.hyperion-rt.org/contributing>) page for more details on how to
contribute code.

