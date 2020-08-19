![logo](https://raw.githubusercontent.com/cmkobel/kma-assemblycomparator/master/scripts/logo.png "")


The KMA Assembly Comparator is a simple pipeline consisting of tools for the analysis of microbial genomics. The idea is that the user provides a directory of assemblies of related bacterial strains, and the pipeline will run a series of generally relevant analyses on a high performance computing cluster.

The KMA Assembly Comparator supports many formats: `gb/fa/fq/gff/gfa/clw/sth` which can be any of `gz/bz2/zip`-formats compressed.

# Installation
In order to use the KMA Assembly Comparator, you have to install it such that you can call the main file (bash) in any directory on your system. For instance
```
export PATH=/path/to/assemblycomparator/:$PATH
```

The program uses a conda environment to handle all dependencies. Please provide this in the conda activation command in assemblycomparator

TODO: set up environment.yml

If you wish to receive an email when the pipeline is done, provide your email in the `$COMPARATOR_DEFAULT_EMAIL_ADDRESS` variable.


# Usage

Create a directory anywhere on your system containing the assemblies you want to analyse, cd to that directory and run the main program `assemblycomparator`.

Then, the program will list a series of options, helping you to start the pipeline.


# Development

This project is still in development. Please check the [repo project manager](https://github.com/cmkobel/kma-assemblycomparator/projects/1) for tracking new features. 

A few subanalyses are in the process of being implemented, (parenthesized programs in the list below)
Installation is also not easy, as the code is only supporting a specific Linux/gwf-setup.


### For each assembly
  * [any2fasta](https://github.com/tseemann/any2fasta) (wide input format support)
  * [prokka](https://github.com/tseemann/prokka) (annotation)
  * [kraken2](https://ccb.jhu.edu/software/kraken2/) (species identification)
  * [mlst](https://github.com/tseemann/mlst) (multi locus sequence typing)
  * [abricate](https://github.com/tseemann/abricate) (virulence/resistance gene identification)
  * ([Oriloc](http://pbil.univ-lyon1.fr/software/Oriloc/oriloc.html)) (Identify possible replication origins, and thereby identify chromids)

  
  
### For each group
  * [roary](https://sanger-pathogens.github.io/Roary/) (pan and core genome)
  * [snp-dists](https://github.com/tseemann/snp-dists) (core genome snp-distances)
  * [panito](https://github.com/sanger-pathogens/panito) (average nucleotide identity
  * [FastTree](http://www.microbesonline.org/fasttree/) (phylogenetic tree of core genome)
  * [IQ-tree](http://www.iqtree.org/) (phylogenetic tree of core genome with bootstrapping)
  * (GC3-profiling) ("fingerprinting" of the distribution of GC-content)
  * (Identification of horizontally transferred genes)
  
  
  
  
