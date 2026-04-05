---
layout: page
title: CMB Lensing
description: A JAX compatible version of the original CMBLensing.jl Julia package
img: assets/img/cmb.png
importance: 1
category: work
related_publications: false
---

<a href="https://github.com/zaneblood1/CMB-Maximization/tree/main/cmb_lensing">CMBLensing.py</a> is currently under development, and will contain all the basic functionality originally found in <a href="https://github.com/marius311/CMBLensing.jl/tree/master/src">CMBLensing.jl</a>. The package has its own simulation code that allows the user to generate random temperature, polarization, and lensing potential fields in the flat sky approximation. The LenseFlow algorithm then quickly lenses these CMB fields, and white noise is added along with a mask and a beam to approximate the type of data that would be measured by instruments here on Earth. Such a data field is then passed through a gradient descent algorithm which takes a series of steps in parameter space to arrive at the maximum likelihood estimators for the true unlensed CMB field and lensing potential.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/u_mode.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/q_mode.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Q and U mode Stokes' polarizations of the Cosmic Microwave Background generated via Gaussian random sampling of the theoretical power spectra using Python CAMB inputs. 
</div>

The original paper which derived and implemented the LenseFlow algorithm is linked <a href="https://arxiv.org/pdf/1708.06753">here</a>. In summary, the CMB field we measure here on Earth using our telescopes or satellites is actually a distorted version of the true field as the light passes through space to reach us and gets deflected or "lensed" by the total effective gravitational potential of all the matter between us and the source of the signal. The LenseFlow algorithm takes in an unlensed CMB field along with a lensing potential and numerically integrates an Ordinary Differential Equation to output a lensed field where each pixel in the resulting map is systematically translated relative to its original position.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/phi.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cmb.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A characteristic lensing potential on the left and an unlensed raw CMB temperature map on the right. All simulations are done in the Flat Sky approximation assuming that spherical harmonics can be accurately approximated by Fourier modes. 
</div>

The LenseFlow algorithm and simulation code are just individual pieces of the whole package. Its main usefulness comes in its MAP joint algorithm which takes as inputs the lensed, noisy signal we measure with our instruments and then recovers the true unlensed fields and lensing potential. This is done by taking gradients of the log of a probability distribution function with respect to the unlensed field and the lensing potential and then performing an alternating step gradient descent algorithm to recover the fields which maximize this PDF.
