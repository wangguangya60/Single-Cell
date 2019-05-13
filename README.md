# Single-Cell
## New Techniques
*  [Slide-seq](https://www.broadinstitute.org/news/new-tool-uses-rna-sequencing-chart-rich-maps-cellular-and-tissue-function?utm_source=twitter&utm_content=news-story%2Ctools&utm_medium=social&utm_campaign=Broad+Institute) A scalable technology for measuring genome-wide expression at high spatial resolution. [article](https://sci-hub.tw/10.1126/science.aaw1219)
* [course](https://hemberg-lab.github.io/scRNA.seq.course/construction-of-expression-matrix.html)
* [New York genome center](https://www.nygenome.org/lab-groups-overview/publications/)
* [ATAT-seq](https://www.nature.com/articles/s41467-019-09670-4), [github](https://github.com/pinellolab/STREAM)

## Cell barcode and UMI 
* [UMI counting issues](https://hemberg-lab.github.io/scRNA.seq.course/construction-of-expression-matrix.html)
![image](img/UMI.issues.png)
* [Cell Ranger correct barcode sequencing errors correction](https://kb.10xgenomics.com/hc/en-us/articles/115003822406-How-does-Cell-Ranger-correct-barcode-sequencing-errors-) based on whitelist.
* [error correction for cell barcodes and UMIs](https://davetang.org/muse/2018/06/06/10x-single-cell-bam-files/)
* [UMI-tools](https://genome.cshlp.org/content/27/3/491.full) used a network approach to join UMIs that map to the same location and only differed by 1 bp, which was caused by PCR amplification. [paper](https://genome.cshlp.org/content/27/3/491.full)
* [alevin](https://github.com/COMBINE-lab/salmon/blob/master/doc/source/alevin.rst) is simialr tool, [paper](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-019-1670-y)
* [The Chromium Single Cell 3'lib](https://teichlab.github.io/scg_lib_structs/methods_html/10xChromium3.html)
* [The difference between 3' and 5' lib](https://kb.10xgenomics.com/hc/en-us/articles/360000939852-What-is-the-difference-between-Single-Cell-3-and-5-Gene-Expression-libraries-)

## Alignment of single cell fastqs
* [Introduction to bam file produced by cellranger](https://davetang.org/muse/2018/06/06/10x-single-cell-bam-files/), [official](https://support.10xgenomics.com/single-cell-gene-expression/software/pipelines/latest/output/bam)
* Read1 (the read containing the cell barcode and UMI) will not have its own line in the bams, the information about read1 is recorded in read2 alignment records
* [overview of algorithms](https://support.10xgenomics.com/single-cell-gene-expression/software/pipelines/latest/algorithms/overview): firsit map
* [mapping to genome or transcripts](https://github.com/CGATOxford/UMI-tools/blob/master/doc/Single_cell_tutorial.md#Mapping-to-the-transcriptome-rather-than-genome)
* [quantification](https://salmon.readthedocs.io/en/latest/alevin.html)

## 10X output gene expression matrix (Market Matrix format to store sparce matrix)
* [read and transform step by step](https://support.10xgenomics.com/single-cell-gene-expression/software/pipelines/latest/output/matrices)
* [transform *.mtx to padas dataframe](https://stackoverflow.com/questions/40514521/transform-matrix-market-matrix-into-pandas-data-frame-python)
* [Suerat tutorial](https://satijalab.org/seurat/v3.0/pbmc3k_tutorial.html) and [algorithms behind](https://www.biorxiv.org/content/biorxiv/early/2018/11/02/460147.full.pdf)
## 10X visualisation
* [Loupe Cell Browser](https://support.10xgenomics.com/single-cell-gene-expression/software/visualization/latest/what-is-loupe-cell-browser)
* [supports](https://support.10xgenomics.com/)

## Introduction to Scanpy
* [Scanpy](https://github.com/theislab/scanpy) use [AnnData](https://anndata.readthedocs.io/en/latest/anndata.AnnData.html), which is based on HDF5 to record expression data
* [basic usage of AnnData](http://falexwolf.de/blog/171223_AnnData_indexing_views_HDF5-backing/).


## Dimensionality reductions
*  [PCA plot](https://hemberg-lab.github.io/scRNA.seq.course/cleaning-the-expression-matrix.html#visual-pca)， Convert a set of observations into a set of values of linearly uncorrelated variables called principal components 
![PCA](img/PCA.png)
*  [tSNE map](https://hemberg-lab.github.io/scRNA.seq.course/cleaning-the-expression-matrix.html#visual-tsne)
*  [MDS plot]

## Clustering of cells
*  [Clustering methods](https://hemberg-lab.github.io/scRNA.seq.course/biological-analysis.html)
*  [Clustering packages and softwares](https://hemberg-lab.github.io/scRNA.seq.course/biological-analysis.html#clustering-introduction)
*  [SC3](https://github.com/hemberg-lab/SC3)
*  [pcaReduce](https://github.com/JustinaZ/pcaReduce)

## experimental issues
*  Appropriate approaches to batch effects in scRNASeq. Red arrows indicate batch effects which are (pale) or are not (vibrant) correctable through batch-correction
![batch effects](img/batch.effects.png)

## Datasets
*  [Tabula Muris](https://tabula-muris.ds.czbiohub.org/) contains nearly 100,000 cells from 20 organs and tissues in Mus musculus. [github](https://github.com/czbiohub/tabula-muris). [dataset download](https://figshare.com/projects/Tabula_Muris_Transcriptomic_characterization_of_20_organs_and_tissues_from_Mus_musculus_at_single_cell_resolution/27733)
*  [summary of scRNA-seq tools](https://www.scrna-tools.org/)

## Filter barcodes(droplets with no cells)
*  [a blog](https://davetang.org/muse/2018/08/09/getting-started-with-cell-ranger/)
