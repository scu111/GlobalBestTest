# GlobalBestTestR
R Codes for a function to perform the Global BEST Significance tests (Clarke et al., 2008) associated with the BIOENV (Clarke & Ainsworth, 1993; now part of the BEST suite, Clarke et al., 2008) procedure in multivariate ecological analyses. 

In linking dissimilarity matrices of biotic communities with environmental variables, the BIOENV procedure is very useful to extract the environmental variable (or combinations thereof) that “best” explain(s) the biotic community dissimilarities. This procedure can be performed in R using the Vegan Package (https://cran.r-project.org/web/packages/vegan/vegan.pdf), amongst others.

A sister procedure, the BVStep (Clarke & Warwick, 1998, also part of the BEST suite) can perform BIO-BIO, ENV-BIO, BIO-ENV, and ENV-ENV analyses, essentially flexible with using either an environmental or biotic dissimilarity matrices in the explanatory or fixed field. In R, this procedure can be performed using Marc Taylor's Sinkr (https://github.com/marchtaylor/sinkr)

The Global Best Significance test assesses the significance of the BIOENV output and generates a p-value based on a specified number of permutations. For my PhD thesis (https://ueaeprints.uea.ac.uk/id/eprint/82744/1/2021UdochiSPhD.pdf), I needed to perform the Global Best Significance Test linked to the BIOENV procedure but 
discovered that this was not possible in any open source software - only available in the PRIMER package with paid subscription. I therefore wrote these codes, which I'm now adding here should this be beneficial to anyone out there.

The functions, global.best and global.BVStep, described in this repository perform the underlying procedure (BIOENV or BVStep, using Vegan or Sinkr codes), perform the “global BEST” significance tests, and plot histograms of permuted coefficients showing the actual coefficient and permutation p-value. They were validated using the Clyde Macrofauna biomass and environmental datasets available in PRIMER, generating the same results as in the published studies (Clarke et al., 2008, 2014). The computation is, however, CPU intensive and might take a bit of time to complete.

Enjoy!
