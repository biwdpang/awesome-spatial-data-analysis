# awesome-spatial-data-analysis
Awesome list of tools and methods to perform spatial transcriptomic data analysis.

old copy braches.
View all the methods <a href="https://htmlpreview.github.io/?https://github.com/drieslab/awesome-spatial-data-analysis/blob/main/review_spat_trns_methods.html">here</a>

# Stereo-seq in MGI

## The basic analysis workflow

Stereopy: https://stereopy.readthedocs.io/en/latest/index.html
Stereopy is a fundamental and comprehensive tool for mining and visualization based on spatial transcriptomics data, such as Stereo-seq (spatial enhanced resolution omics sequencing) data. More analysis will be added here, either from other popular tools or developed by ourselves, to meet diverse requirements. Meanwhile, we are still working on the improvement of performance and calculation efficiency.

## Cell segmentation

Spateo: https://spateo-release.readthedocs.io/en/latest/index.html
Leveraging the ultra-high spatial-resolution, large field of view and high RNA capture sensitivity of Stereo-seq, spateo enables single cell resolution spatial transcriptomics via nuclei-staining and RNA signal based cell segmentation.

## Spatial transcriptome CNV

SpatialInferCNV: https://github.com/aerickso/SpatialInferCNV
Spatially resolved transcriptomics has emerged as a genome-wide analysis of gene expression to explore tissues in an unsupervised manner. In this study we infer genome-wide copy-number variations (CNV) from spatially resolved mRNA profiles in situ. Gene expression has previously been used to infer CNVs in single cells, successfully identifying regions of chromosomal gain and loss. Here we expand into a spatial modality, generating CNV calls in each spatial region represented by barcoded spots.

CalicoST: https://github.com/raphael-group/CalicoST
CalicoST is a probabilistic model that infers allele-specific copy number aberrations and tumor phylogeography from spatially resolved transcriptomics.CalicoST has the following key features:

    Identifies allele-specific integer copy numbers for each transcribed region, revealing events such as copy neutral loss of heterozygosity (CNLOH) and mirrored subclonal CNAs that are invisible to total copy number analysis.
    Assigns each spot a clone label indicating whether the spot is primarily normal cells or a cancer clone with aberration copy number profile.
    Infers a phylogeny relating the identified cancer clones as well as a phylogeography that combines genetic evolution and spatial dissemination of clones.
    Handles normal cell admixture in SRT technologies hat are not single-cell resolution (e.g. 10x Genomics Visium) to infer more accurate allele-specific copy numbers and cancer clones.
    Simultaneously analyzes multiple regions or aligned SRT slices from the same tumor.

## Spatial transcriptome deconvolution

Tangram: https://github.com/broadinstitute/Tangram
Tangram is a Python package, written in PyTorch and based on scanpy, for mapping single-cell (or single-nucleus) gene expression data onto spatial gene expression data. The single-cell dataset and the spatial dataset should be collected from the same anatomical region/tissue type, ideally from a biological replicate, and need to share a set of genes. 

SPOTlight: https://github.com/MarcElosua/SPOTlight (old or new is different)
SPOTlight provides a tool that enables the deconvolution of mixtures of cells from a single-cell reference. Originally developed for 10X's Visium - spatial transcriptomics- technology, it can be used for all technologies that output mixtures of cells. 

Cell2location: https://github.com/BayraktarLab/cell2location
Cell2location is a principled Bayesian model that can resolve fine-grained cell types in spatial transcriptomic data and create comprehensive cellular maps of diverse tissues. Cell2location accounts for technical sources of variation and borrows statistical strength across locations, thereby enabling the integration of single cell and spatial transcriptomics with higher sensitivity and resolution than existing tools. This is achieved by estimating which combination of cell types in which cell abundance could have given the mRNA counts in the spatial data, while modelling technical effects (platform/technology effect, contaminating RNA, unexplained variance).

RCTD(spacexr): https://github.com/dmcable/spacexr
RCTD can assign single cell types or cell type mixtures to spatial transcriptomics spots. RCTD has three modes: doublet mode, which assigns 1-2 cell types per spot and is recommended for technologies with high spatial resolution such as Slide-seq and MERFISH; full mode, which assigns any number of cell types per spot and is recommended for technologies with poor spatial resolution such as 100-micron resolution Visium; multi mode, an extension of doublet mode that can discover more than two cell types per spot as an alternative option to full mode.

## Spatial transcriptome communication

Spateo

# From single-cell
## NMF
CoGAPS: https://fertiglab.github.io/CoGAPSGuide/
Here, we aim to introduce a suite of computational tools that implement NMF and provide methods for accurate, clear biological interpretation and analysis. A generalized discussion of NMF covering its benefits, limitations, and open questions in the field is followed by three procedures for the Bayesian NMF algorithm CoGAPS (Coordinated Gene Activity across Pattern Subsets). Each procedure will demonstrate NMF analysis to quantify cell state transitions in public domain single-cell RNA-sequencing (scRNA-seq) data of 25,422 epithelial cells from pancreatic ductal adenocarcinoma (PDAC) tumors and control samples. The first demonstrates PyCoGAPS, our new Python implementation of CoGAPS that enhances runtime of Bayesian NMF for large datasets.(include R packages CoGAPS)

## cell-cell communication
CellphoneDB: https://cellphonedb.readthedocs.io/en/latest/RESULTS-DOCUMENTATION.html#
CellphoneDB tool provides different methods to assess cellular crosstalk between different cell types by leveraging our CellphoneDB database of interacting molecules with single-cell transcriptome data.

## RNA velocity
Velocyte: http://velocyto.org/velocyto.py/tutorial/index.html#running-the-cli

scVelo: https://scvelo.readthedocs.io/en/stable/
scVelo is a scalable toolkit for RNA velocity analysis in single cells; RNA velocity enables the recovery of directed dynamic information by leveraging splicing kinetics [Manno et al., 2018]. scVelo collects different methods for inferring RNA velocity using an expectation-maximization framework [Bergen et al., 2020], deep generative modeling [Gayoso et al., 2023], or metabolically labeled transcripts [Weiler et al., 2023].
(reference tutorial https://smorabit.github.io/blog/2021/velocyto/)





