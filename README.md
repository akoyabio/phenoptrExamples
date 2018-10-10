# phenoptrExamples - Extended examples for use with the `phenoptr` package

<style type="text/css">
img { 
  border: none;
}
table {
    width: auto !important;
}
</style>

`phenoptrExamples` contains 
[example code](https://akoyabio.github.io/phenoptrExamples/articles/index.html) 
and extended data sets demonstrating
the use of the [phenoptr](http://akoyabio.github.io/phenoptr) package to
analyze data from multiple fields. 

<div class="panel panel-default"><div class="panel-body">
For introductory examples, please see
the
<a href="https://akoyabio.github.io/phenoptr/articles/index.html">Tutorials</a>
included in the <code>phenoptr</code> documentation.</div></div>

`phenoptr` contains functions that make it easier to read and analyze data tables
and images created by Akoya Biosciences' inForm<sup>&reg;</sup> software.
`phenoptr` and `phenoptrExamples` are part of the Akoya Biosciences Phenoptics&trade;
family of
Quantitative Pathology Research Solutions. For more information
visit the Phenoptics&trade;
[home page](http://www.perkinelmer.com/cancer|immunology/index.html).

----

## Installation

Installation is from GitHub. Note: this package includes many large files.
The entire package contains over 150 MB of data files.

```
# install.packages("devtools")
devtools::install_github("akoyabio/phenoptrExamples", build_vignettes=TRUE)
```

----

## Getting started

The Tutorials demonstrate aggregation of data across multiple fields and slides.

- [Aggregating data from multiple fields](https://akoyabio.github.io/phenoptrExamples/articles/aggregation.html)
demonstrates reading and processing cell seg data from multiple fields and samples.
- [Aggregating touch counts](https://akoyabio.github.io/phenoptrExamples/articles/count_touches.html) shows how to count touching cells across multiple fields and aggregate
the results per sample.

### Sample data

`phenoptrExamples` contains selected inForm output from nine images taken
from three samples of lung cancer tissue.

The tissue was stained with DAPI counterstain and Opal™ stains
and imaged on a 
Vectra® Polaris™ Automated Quantitative Pathology Imaging System.
The MSI images were unmixed to components, segmented and classified
with inForm® image analysis software. 

The sample cell data includes these phenotypes:

- `CD8+` (cytotoxic T cell)
- `CD68+` (macrophage)
- `FoxP3+` (regulatory T cell)
- `CK+` (tumor)
- `other`

Four files are included for each image:

- Composite image in JPEG format (`composite_image.jpg`)
- Cell segmentation data (`cell_seg_data.txt`)
- Cell segmentation maps (`binary_seg_maps.tif`)
- Composite with tissue segmentation (`image_with_tissue_seg.jpg`)

To see a full list of all included files, use the command
`list.files(system.file("extdata", "samples", package = "phenoptrExamples"))`.

This table shows the stains used, the epitopes they were bound to,
and the colors used to show the stains in the composite and phenotype views.

Stain   | Epitope | Composite | Phenotype
--------|---------|-----------|----------
DAPI    | Nucleus | Blue      | N/A
Opal520 | PDL1    | Red       | N/A
Opal540 | CD8     | Yellow    | Yellow
Opal570 | FoxP3   | Orange    | Orange
Opal620 | CD68    | Magenta   | Magenta
Opal650 | PD1     | Green     | N/A
Opal690 | CK      | Cyan      | Cyan

----

### Full documentation

See the
[Tutorials](https://akoyabio.github.io/phenoptrExamples/articles/index.html)
and the 
[full phenoptr documentation](http://akoyabio.github.io/phenoptr).
