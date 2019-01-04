# HTADs

A constrained hierarchical method to detect Topologically Associated Domains

## Getting Started

### Installing

You can install the package using the handy devtools::install_github.

install.packages("devtools")

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
# Load packages.

```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running algorithm

We use a specific input to illustrate how the constrained hierarchical clustering works. The raw data is derived from a small locus (~ 150Mb) on the chromosome 18 from Hi-C experiment of RAO[ref] in GM12878 cell type using a specific 4bp-cutter restriction enzyme, MboI (SRA: SRR1658602).This chromosomal region can be represented as a symmetric contact matrixes (M), where each color point represents the average number of interactions between the bins (M[i,j]) on the chromosome.

![alt text](http:https://github.com/paulasoler/HTADs/zoom_pictures_test.pdf)


To obtain this 40kb-binned raw interaction matrix, we processed Hi-C data using a complete Python library, called TADbit, that deals with all the necessary steps to analyze, model and explore 3C-based data. https://github.com/3DGenomes/TADbit


### Dependencies

```
require(colorRamps)
require(data.table)
require(Matrix)
require(doParallel)
require(rioja)
require(fpc)
require(reshape2)
```

### Format of input data:
We highly recommended normalize the data before to start the TAD caller. We give advice to use ONED normalization to correct the experimental bias that affects the signal profile defined by the contacts.
https://github.com/qenvio/dryhic

 - 3 columns-format stored in tab-separated value without header. The first and the second columns correspond to the pair of loci(i,j) which are stablish a average number of normalized interactions (the last column). 

```
28	27	1108.42577685
22	12	423.808156978
26	6	286.1442771
17	13	1740.23475628
```
### Visualization of the data and Pearson correlation matrix

### PCA (200) + Why 200?

### Fast version

### Optimazed version

### Assesment of the method: Calinski

### Benchmarks

## Built With

* [R](https://www.r-project.org/about.html) - The web framework used

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Paula Soler Vila** - *Initial work* - (https://github.com/paulasoler/)
* **Pol Cuscó Pons** - *Initial work* - (https://github.com/nanakiksc/)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
