# Note (added by [Van1yu3]( https://github.com/Van1yu3/ ))

This branch is taken from SHA code: `e8bbb02d9b5ce97c9cc64d0138c636cdcf3295eb`. Committed time: `Mar 4 10:01:51 2019`.

I extracted this branch since some functions would be updated in the next commit by the author, but some  papers utilized these old functions to obtain their results. I could successfully install this old version using a conda environment with R-3.5.3 and python 2.7.

My installation step:

```bash
$ pip install snaptools
```

```R
$ R
devtools::install_github("Van1yu3/SnapATAC@version1")
```

The following is the original README content. 

## SnapATAC (under development)

Single Nuclesus Analysis Package for ATAC-seq. 

## Introduction
SnapATAC is fast, accurate and unbiased method for analyzing single cell ATAC-seq datasets. Compared to previous methods, SnapATAC 1) overcomes limitation of reliance on open chromatin peaks defined by aggregate/bulk signal; 2) reveals novel cis-elements active in rare populations; 3) adjusts for differing sequencing depth between cells; 4) scales up to millions of cells.

SnapATAC has two components: [Snaptools](https://github.com/r3fang/SnapTools) and [SnapATAC](https://github.com/r3fang/SnapATAC). 

* Snaptools is a module for working with [snap](https://github.com/r3fang/SnapATAC/wiki/FAQs) file in Python. 
* SnapATAC is a R package for the downstream analysis. 

**NOTE: YOU ARE WELCOME TO USE SNAPATAC, BUT PLEASE NOTE THAT SNAPATAC IS STILL UNDER DEVELOPMENT AND MAY NEED FURTHER TESTING**

## Requirements  
* Python (2.7)
* R (>= 3.4.0)

## Install SnapTools
Install snaptools from PyPI

```bash
$ pip install snaptools==1.2.5 --user
```

See how to install snaptools on [FAQs](https://github.com/r3fang/SnapATAC/wiki/FAQs). 

## Install SnapATAC

```
$ R
> install.packages("devtools")
> library(devtools)
> install_github("r3fang/SnapATAC");
> library(SnapATAC);
```

## Get Started (see more details in MOs 2k in tutorials)

```R
> library(SnapATAC);
> data(mos);
> mos = calJaccard(mos);
> mos = runPCA(mos, pc.num=20);
> mos = runCluster(mos, k=15);
> mos = runViz(mos, dims=2, method="Rtsne");
```

## Galleries & Tutorials (click on the image for details)
[<img src="./images/MOS_2k.png" width="275" height="315" />](./examples/MOS_2k/MOS_2k.md)
[<img src="./images/Fang_2019.png" width="275" height="315" />](./examples/Fang_2019/Fang_2019.md)
[<img src="./images/10X_10k.png" width="275" height="315" />](./examples/10X_10k/10X_10k.md)
[<img src="./images/Cusanovich_2018.png" width="275" height="315" />](./examples/Cusanovich_2018/Cusanovich_2018.md)
[<img src="./images/Lake_2018.png" width="275" height="315" />](./examples/Lake_2018/Lake_2018.md)
[<img src="./images/Schep_2017.png" width="275" height="315" />](./examples/Schep_2017/Schep_2017.md)


