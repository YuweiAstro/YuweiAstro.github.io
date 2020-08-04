---
layout:     post
title:      "Tips for Radio Astronomy"
date:       2020-07-21
author:     "Yuwei"
header-img: "img/post-bg-os-metro.jpg"
mathjax: true
category: [astronomy]
tags:
  - astronomy
  - tip
---

## Convert Intensity \(Jy/beam\) to Flux density \(Jy\)

To calculate flux density (Jy) from intensity (Jy/beam) of an extended source:

* sum up all the pixels
* divide it by the beam volume, $\Omega_b$, where: $\Omega_{b}=\frac{\pi}{4 \ln 2} \times \Theta_{maj} \times \Theta_{\min }$

$\Theta_{m a j}$ and $\Theta_{\min }$ is the major and minor axis of the synthesis beam, measured in pixels. To convert from angles to pixels, one need to know the pixel increments along each axis in the FITS file, which are the $\mathtt{CDELT}$ values in the header. 

And then: $\frac{J y /(beam / p i x)}{pixels / beam}=J y$

## Frequency to Velocity

The special relativistic equation for the conversion of the observed frequency, f, of a source into radial velocity, v, under the assumption that the object is moving towards or away from the observer reads :

​	$\frac{v}{c}=\frac{f_{0}^{2}-f^{2}}{f_{0}^{2}+f^{2}}$

For a small bandwidth $\Delta f$:

​	${c}{\Delta v=v_{2}-v_{1}=c \frac{\left(f_{0}+\Delta f\right)^{2}-f_{0}^{2}}{\left(f_{0}+f\right)^{2}+f_{0}^{2}}}
{=c \frac{2 f_{0} \Delta f+\Delta f^{2}}{2 f_{0}^{2}+2 f_{0} \Delta f+\Delta f^{2}}}$	

omit $\Delta f^2$ and the equation becomes:

​	$=\frac{c \Delta f}{f_{0}+\Delta f}$		



> Find more information in  [Useful equations for radio astronomy](https://www.atnf.csiro.au/people/Tobias.Westmeier/tools_hihelpers.php#velocity)



## Uncertainties in Flux Density Measurement

See the appendix in [**Beltrán, 2001, AJ, 121, 1556**](http://adsabs.harvard.edu/abs/2001AJ....121.1556B)  for a detailed discription of **uncertainty in the flux density measurement for extended sources:**
