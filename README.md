# a520-glimpse

This repository contains the data and code to reproduce the results in [Sparse Reconstruction of the Merging A520 Cluster System](https://iopscience.iop.org/article/10.3847/1538-4357/aa850d/meta) (Peel et al. 2017). It relies on the multi-scale sparsity-based mass mapping software called [Glimpse](https://github.com/CosmoStat/Glimpse). We have reconstructed the mass distribution of Abell 520, a merging galaxy cluster system also known as the 'cosmic train wreck'.  We obtained high-resolution mass maps using two separate galaxy catalogs derived from HST observations and compared the results to previous weak-lensing studies of the system.

## Data

Galaxy shear catalogues for A520 from two different telescope surveys are available. The first is from [Clowe et al. 2012, ApJ 758, 128 ](https://iopscience.iop.org/article/10.1088/0004-637X/758/2/128/meta) (C12), and the second is from [Jee et al. 2014, ApJ 783, 78](https://iopscience.iop.org/article/10.1088/0004-637X/783/2/78/meta) (J14).

## Requirements

The [Glimpse](https://github.com/CosmoStat/Glimpse) software is required to reproduce our mass maps. Details of the algorithm and tests on simulated data can be found in [High resolution weak lensing mass mapping combining shear and flexion](https://www.aanda.org/articles/aa/abs/2016/07/aa28278-16/aa28278-16.html) (Lanusse et al. 2016).

## Usage

```shell
$ cd data
$ glimpse config_A520_c12.ini A520_cat_c12.fits kappa.fits
```

## Figures
<p align="center">
<img src="https://github.com/austinpeel/a520-glimpse/blob/master/figures/a520_glimpse_maps.png" alt="glimpse_maps" width="700"/>
</p>

Mass maps reconstructed with [Glimpse](https://github.com/CosmoStat/Glimpse) on C12 (left) and J14 (right) telescope data. The projected matter distributions (dark + luminous) are in color and overlaid on the science image.

<p align="center">
<img src="https://github.com/austinpeel/a520-glimpse/blob/master/figures/a520_source_density.png" alt="source_density" width="750"/>
</p>

Source galaxy density maps from C12 (left) and J14 (right) data sets. The C12 galaxy ellipticity catalog was derived from a combination of Magellan and HST/ACS images with galaxy number densities of 22 and 56 per square arcmin, respectively. The J14 catalog comes from the same ACS data as C12 but has a higher galaxy number density of 109 per square arcmin due to a different reduction pipeline.
