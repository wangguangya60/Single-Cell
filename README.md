# Single-Cell
## New Techniques
*  [Slide-seq](https://www.broadinstitute.org/news/new-tool-uses-rna-sequencing-chart-rich-maps-cellular-and-tissue-function?utm_source=twitter&utm_content=news-story%2Ctools&utm_medium=social&utm_campaign=Broad+Institute) A scalable technology for measuring genome-wide expression at high spatial resolution. [article](https://sci-hub.tw/10.1126/science.aaw1219)
* [course](https://hemberg-lab.github.io/scRNA.seq.course/construction-of-expression-matrix.html)
* [New York genome center](https://www.nygenome.org/lab-groups-overview/publications/)


## UMI
* [UMI counting issues](https://hemberg-lab.github.io/scRNA.seq.course/construction-of-expression-matrix.html)
![image](img/UMI.issues.png)
* [error correction for cell barcodes and UMIs](https://davetang.org/muse/2018/06/06/10x-single-cell-bam-files/)
* [UMI-tools](https://genome.cshlp.org/content/27/3/491.full) used a network approach to join UMIs that map to the same location and only differed by 1 bp, which was caused by PCR amplification.
* [The Chromium Single Cell 3'lib](https://teichlab.github.io/scg_lib_structs/methods_html/10xChromium3.html)
* [The difference between 3' and 5' lib](https://kb.10xgenomics.com/hc/en-us/articles/360000939852-What-is-the-difference-between-Single-Cell-3-and-5-Gene-Expression-libraries-)

## Alignment of single cell fastqs
* [Introduction to bam file produced by cellranger](https://davetang.org/muse/2018/06/06/10x-single-cell-bam-files/), [official](https://support.10xgenomics.com/single-cell-gene-expression/software/pipelines/latest/output/bam)
* Read1 (the read containing the cell barcode and UMI) will not have its own line in the bams, the information about read1 is recorded in read2 alignment records
* [overview of algorithms](https://support.10xgenomics.com/single-cell-gene-expression/software/pipelines/latest/algorithms/overview): firsit map
* [quantification](https://salmon.readthedocs.io/en/latest/alevin.html)

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
