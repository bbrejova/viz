---
title: Evolution project for Data Visualization course 2024/25
---

Proteins are chains of amino acids that perform many key functions in living cells. Proteins change during evolution due to mutations in DNA. Nonetheless we can often find similarities between proteins from different organisms. In this project, we will consider the amount of changes between proteins in different organisms.

### Protein distance file `dist.txt`

The key part of this dataset is file [dist.txt](https://compbio.fmph.uniba.sk/~bbrejova/tmp/prot-viz/dist.txt), which contains data about 13021 human proteins and the corresponding similar proteins from 5 other mammals: baboon, mouse, dog, mouse, and opossum.

The file contains 13021 distance tables of dimensions 6x6. Each table contains for each pair of animals a number quantifying how much the corresponding proteins in these two animals differ from each other. 

For example, the very first table in the file is the following:

```
A0A087WTH1
opossum     0.000000  0.437878  0.389459  0.368851  0.344118  0.385447
mouse       0.437878  0.000000  0.217262  0.192162  0.196955  0.232052
cow         0.389459  0.217262  0.000000  0.138486  0.154998  0.144013
dog         0.368851  0.192162  0.138486  0.000000  0.110481  0.109375
human       0.344118  0.196955  0.154998  0.110481  0.000000  0.029031
baboon      0.385447  0.232052  0.144013  0.109375  0.029031  0.000000
```

String A0A087WTH1 is the identifier of the human protein in Uniprot database. The description of this protein in this database is here: <https://www.uniprot.org/uniprotkb/A0A087WTH1/entry>

Each of the 6 rows starts with the name of one animal. The columns are ordered in the same way as rows but column names are not shown. Second number of the first row (0.437878) thus corresponds to the distance between opossum and mouse analogs of human protein A0A087WTH1. Distance between human and baboon proteins is much smaller, only 0.029031. These distances reflect the number of mutations that seperate the two proteins (higher number means more mutations) and are computed by rather complicated probabilistic models.

Beware, the order of species is different for different proteins. Diagonal values are always zero in all tables, and the table is symmetric, meaning that distance of A and B is the same as distance of B and A.  Therefore it is sufficient to consider only 15 values in the trinagle above the main diagonal. It is probably a good idea to reformat this file to a more convenient format in which each protein will get one line with 15 numbers in a fixed order.

### Differences in distances

You may notice that some matrices will have overall much higher distances than others. One of the reasons is natural selection. Often proteins that have very important functions change slower in evolution because every change is potentially dangerous. On the other hand, some fast evolving proteins may be important for adapting to new situations such as bacteria or viruses, new sources of food etc. This is why it is interesting to look for proteins that mutate very slowly but also for those that mutate very fast.

In addition to the overall speed of mutation for a particular protein, some proteins might evolve faster in some animals. This can mean some adaptation which is particularly important in this species. The way to detect this is to compute ratio of distance between aniomals *x* and *y* and animals *u* and *v* (some of these can be the same such as human-mouse and human-dog). Typically this ratio will be in some range and the outliers are potentially interesting, particularly if they are confirmed by different pairs of species.

### Possible questions to study with the tables

* Propose some measure of the overall speed of mutation of a protein and compare these speeds among proteins. Which proteins have the lowest and highest values in their matrices? 
* Find which proteins have unusual ratios of distances between pairs of species.
* Are these matrix properties related to other data about proteins which are described below?
* You can try to put all distance matrices on the same scale by dividing values in each matrix by some measure of the mutation speed. Then you can try to compute some "average" or "median" matrix which will say how closely are individual animals related to each other. Are these distances of animals in agreement with  the taxonomy described below?

## Additional data

The following files may provide additional properties of the proteins that you can use in your project, but you do not need to use all of them.

* [human-orig.fa.gz](https://compbio.fmph.uniba.sk/~bbrejova/tmp/prot-viz/human-orig.fa.gz) is the file of protein sequences. It contains all human proteins from the distance tables but also some additional proteins not included in our set. Each protein starts with line starting with ">" and containing protein identifiers and description of its function. This is followed by several lines containing the sequence of amino acids in the protein. Each amino acid is denoted by a single letter. You can correlate properties of matrices with keywords in protein descriptions. You can also compare frequencies of amino acids in individual proteins.
* [groups.txt](https://compbio.fmph.uniba.sk/~bbrejova/tmp/prot-viz/groups.txt) contains on each line identifiers of the six proteins used in one of the distance matrices. Each identifier has two parts: identifier from Uniprot database followed by underscore (_) and the name of the species. This file is useful mainly if you want to look up some proteins in the Uniprot database.
* [aln.tgz](https://compbio.fmph.uniba.sk/~bbrejova/tmp/prot-viz/aln.tgz) is an archive of a folder with a file for each group of 6 related proteins. Each file contains the proteins aligned to each other so that corresponding amino acids are in the same column. When an amino acid is missing in one of the proteins, a dash is added instead. From this file you can see what changes actually happened (and how many dashes there are). 
* [goslim.tsv](https://compbio.fmph.uniba.sk/~bbrejova/tmp/prot-viz/goslim.tsv) contains for each human protein identifier from our set several functional categories given as identifiers in Gene ontology. Each functional category is on a separate line. If the protein has no information about function, it will have zero lines. If it has 3 functional catgories, it will on three lines. [Gene ontology](https://geneontology.org/) is a set of well defined terms describing function of a gene or protein. Overall 135 different categories are used in the file.
* [goslim-names.tsv](https://compbio.fmph.uniba.sk/~bbrejova/tmp/prot-viz/goslim-names.tsv) gives a name for each functional category used in `goslim.tsv`. For example, file `goslim.tsv` contains line linking protein `A0A087WZ39` to category `GO:0005886` and file `goslim-names.tsv` specifies that `GO:0005886` means `plasma membrane`. So this particular protein is probably located in the plasma membrane (outer membrane surrounding a cell).

### Used species

* Homo sapiens (human)
* Papio anubis (Olive baboon)
* Mus musculus (House mouse)
* Canis lupus familiaris (Domestic dog)
* Bos taurus (Bovine, Hereford cattle)
* Monodelphis domestica (Gray short-tailed opossum)

Taxonomy:

* Human and baboon both belong to primates.
* Primates and mouse belong to a bigger group of Euarchontoglires.
* Dog and cow belong to group Laurasiatheria.
* Both Euarchontoglires and Laurasiatheria belong to Boreoeutheria.
* Boreoeutheria as well as the opossum belong to mammals.


### More information

Brona Brejova would be happy to answer your questions.
