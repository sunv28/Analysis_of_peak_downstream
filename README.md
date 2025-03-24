# Analysis_of_peak_downstream

Analysis_of_peak_downstream consists of three parts:

you can downland the html to see the turiol

-   **Genome Coordinate Conversion** 🌍🔄
-   **Peak Overlap** 📊
-   **Peak Annotation, Comparison and Visualization** 🔬✨

------------------------------------------------------------------------

## Genome Coordinate Conversion 🌍

When conducting research, we need to unify the genome coordinate system. The process of converting from one version of the coordinate system to another is called **liftover (UCSC)** or **crossmap (Ensembl)**.

-   The **UCSC and Ensembl** provides a ready-to-use **web version**:

    [**UCSC** web version](https://genome.ucsc.edu/cgi-bin/hgLiftOver) 🌐  
    [**Ensembl** web version](https://grch37.ensembl.org/Homo_sapiens/Tools/AssemblyConverter) 🌐 **(Only supports species: human, mouse, Caenorhabditis elegans, Saccharomyces cerevisiae, Zebrafish)**

------------------------------------------------------------------------

## Peak Overlap 📊

This section covers how to find overlaps of peaks:

-   First, we use the peak files to create **`GRanges`** objects.

-   **`findOverlaps()`**: Creates **`NCList`** and **`GNCList`** objects to find the overlaps between two "range-based" objects.

-   **`findOverlapsOfPeaks()`**: Another version for finding overlaps using **`findOverlaps()`** specifically for peaks.

-   **`makeVennDiagram()`**: Create Venn Diagrams to visualize peak overlaps.

------------------------------------------------------------------------

## **Peak Annotation, Comparison, and Visualization** 🔬✨

This section covers the usage of [**`ChIPseeker`**](https://bioconductor.org/packages/release/bioc/vignettes/ChIPseeker/inst/doc/ChIPseeker.html), an R package for **peak annotation, comparison, and visualization**:

-   If two ChIP-seq datasets, obtained by different binding proteins, overlap significantly, these two proteins may form a complex or have interactions in regulating chromosome remodeling or gene expression. 💡

-   [**`ChIPseeker`**](https://bioconductor.org/packages/release/bioc/vignettes/ChIPseeker/inst/doc/ChIPseeker.html) supports statistical testing of significant overlap among ChIP-seq datasets and incorporates open access databases like GEO (which contains **17,000 bed files**) for users to compare their own datasets with those deposited in the database. 📚

-   Converting genome coordinates from one genome version to another is also supported. 🔄
