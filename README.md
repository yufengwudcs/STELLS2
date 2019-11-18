# STELLS2
Coalescent-based maximum likelihood inference of species tree from gene tree topologies

*******************************************************************************************
Please read the user manual if you want to use STELLS.
*******************************************************************************************

Software accompaniment to

If you use the STELLS2 to run on larger data in a publication, please cite the following reference: 

Jingwen Pei and Yufeng Wu, STELLS2: Fast and Accurate Coalescent-based Maximum Likelihood Inference of Species Trees from Gene Tree Topologies, Bioinformatics, in press, 2017. This paper develops the STELLS2 approach.
  
Yufeng Wu, "Coalescent-based Species Tree Inference from Gene Tree Topologies Under Incomplete Lineage Sorting by Maximum Likelihood", Evolution, v. 66 (3), p. 763-775, 2012. (This is the original paper developing the overall STELLS algorithm for the inference of species tree from gene tree topologies.)

Yufeng Wu, "A coalescent-based method for population tree inference with haplotypes", Bioinformatics, v31, p. 691-698, 2015. (This paper develops an extension of STELLS, called STELLSH, for the inference of population tree, which takes population haplotypes as input and infer the population split history (called population tree). This allows the inference from sequences directly, and may be a better choice when the time scale is shorter.).

Yufeng Wu, "An Algorithm for Computing the Gene Tree Probability under the Multispecies Coalescent and its Application in the Inference of Population Tree", Bioinformatics, 32(12):i225-i233, 2016. (This is a recent paper for a faster algorithm when there are multiple gene lineages for small number of populations. It also includes a new approach for the population tree inference from pairwise population distances.)


STELLS2: this release contains the implementaiton of STELLS2, a faster species tree inference method than the original STELLS. My test shows STELLS2 is much faster than the original STELLS, and STELLS2 and STELLS have about the same inference accuracy. By default, if you run STELLS, you are using STELLS2.

------------------------------------------------------------------------------------------------------------------------------
STELLS is a program for finding the maximum likelihood estimate of the species tree for the given gene trees, which undergo incomplete lineage sorting (as illustrated in the above figure). STELLS can also compute the gene tree probability for a given species tree. It has also been extended for the inference of population trees from haplotypes. See my papers for more details.

Note: Files can be downloaded using "Save Link/Target As..." After downloading the softwares, you may need to change file access permissions (e.g. chmod u+x stells-linux).

Current version: v. 2.1.0.1 (released at: November 8, 2016). Source code available (see below). Here is a list of files for the distribution of STELLS.

    stells-v2-1-0-1-linux64, executable compiled under Linux 64 bits system.
    stells-v2-1-0-1-mac, executable compiled for Mac.
    User manual in PDF. Read this carefully before using STELLS.
    example-gene.trees, a simple gene tree example for sample input.
    example-dup-gene.trees, a simple gene tree example with multiple gene lineages per species.
    example-species.trees, a simple species tree example for sample input.
    example-10trees.gtrees, a larger example of gene trees with multiple gene lineages per population which demonstrates the usage of the -p option (pairwise population distance based inference, which runs much faster than the case of not using the -p option).


In case you want to build from source code, download the source code in STELLSv2.1.0.1.tar.gz. Simply de-compress and type "make".

* November 18, 2019
I realized I forgot to upload a revised code to fix a small bug in v.2.1.0. Please use v.2.1.0.1 from now on.
