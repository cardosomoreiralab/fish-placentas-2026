# A new cell type facilitated live-bearing and multiple independent origins of placentation in fish

Code and processed data for Safian, Kraunsoe et al. 2027 ([journal], [DOI]).

Live-bearing fishes in the family Poeciliidae have evolved placentas repeatedly
and recently, which makes them a natural experiment in how a new organ is built.
We profiled ovaries from nine poeciliid species, spanning species with and
without a placenta, to ask which cell types form the placenta in different
origins, how these cell types are specified, and what molecular changes they
undergo to enable nutrient transfer.

## What is here

Code to reproduce the figures in the paper. The data processing steps are
described in the Methods; these scripts start from the processed objects and
reference files, which are deposited (see Data availability).

* [`figures/code_fig1.Rmd`](figures/code_fig1.Rmd) — (B) *P. prolifica* and
  *P. turneri* UMAPs; (C) the correlation heatmap between them; (E) the SAMap
  cell-type tree for the five placental species.
* [`figures/code_fig2.Rmd`](figures/code_fig2.Rmd) — (B) SAMap correlation heatmap
  for all nine poeciliids plus zebrafish and killifish; (D) cell-type
  proportions in the *P. turneri* and *P. gracilis* atlases, by sample status
  (pregnant, non-pregnant, juvenile).
* [`figures/code_fig3.Rmd`](figures/code_fig3.Rmd) — (A) GO terms for markers of
  the late follicle cell; (B) cell-type enrichment of vitellogenesis and
  ovulation genes; (C) upset plot and pie chart of positively selected genes
  highly expressed in the late follicle cell.
* [`figures/code_fig4.Rmd`](figures/code_fig4.Rmd) — (B) TF motif enrichment and
  activity across cell types; (C) SCENIC+ transcription-factor gene regulatory
  networks.
* [`figures/code_fig5.Rmd`](figures/code_fig5.Rmd) — (B) GO terms for
  differentially expressed genes; (C) Venn diagrams of DEG overlap between the
  placental species; (D) upset plot of genes involved in different processes
  across species; (E) conservation of TF-DEG interactions.
* [`figures/code_fig6.Rmd`](figures/code_fig6.Rmd) — (A) module-score enrichment of
  genes of different evolutionary ages; (B) upset plot and pie charts of GO
  terms for genes with parallel substitutions in the late follicle cell and the
  yolk pericardial sac.
Supplementary figures, in [`figures/supplementary/`](figures/supplementary):

| | |
|---|---|
| [`code_sf1.Rmd`](figures/supplementary/code_sf1.Rmd) | quality control for all nine atlases |
| [`code_sf2.Rmd`](figures/supplementary/code_sf2.Rmd) | proportion of each snRNA-seq library per species |
| [`code_sf3.Rmd`](figures/supplementary/code_sf3.Rmd) | cell-type-specific marker genes for ovarian cell types in *P. turneri* and *P. prolifica* |
| [`code_sf4.Rmd`](figures/supplementary/code_sf4.Rmd) | dendrograms of 1 - SAMap score, and a tree from pseudobulks and GSI |
| [`code_sf5.Rmd`](figures/supplementary/code_sf5.Rmd) | GO bar charts for genes under positive selection |
| — | Supplementary 6 is imaging; no code |
| [`code_sf7.Rmd`](figures/supplementary/code_sf7.Rmd) | (A) global TF activity heatmap; (B) granulosa/theca and late follicle/germinal epithelium TF patterns |
| [`code_sf8.Rmd`](figures/supplementary/code_sf8.Rmd) | GO bar charts for late follicle cell DEGs |
| [`code_sf9.Rmd`](figures/supplementary/code_sf9.Rmd) | sharing of DEGs between the placental species |
| [`code_sf10.Rmd`](figures/supplementary/code_sf10.Rmd) | number of DEGs per cell type in the placental species |
| [`code_sf11.Rmd`](figures/supplementary/code_sf11.Rmd) | enrichment of genes of different ages across ovarian cell types, in the four species pairs |

## Reference data

Inputs are in [`data/`](data).

## Data availability

* Single-nucleus RNA-seq: ArrayExpress [`E-MTAB-17757`](https://www.ebi.ac.uk/biostudies/arrayexpress/studies/E-MTAB-17757)
* Single-nucleus ATAC-seq: ArrayExpress [`E-MTAB-17776`](https://www.ebi.ac.uk/biostudies/arrayexpress/studies/E-MTAB-17776)
* Genome assemblies: ENA [`PRJEB115767`](https://www.ebi.ac.uk/ena/browser/view/PRJEB115767)
* Annotated Seurat objects for all eleven atlases, the ArchR projects and the
  SCENIC+ outputs are deposited alongside the raw data; cell-type names follow
  the single vocabulary described in [`snRNA-seq/cell_types.md`](snRNA-seq/cell_types.md).

## Data exploration

[**Atlas browser**](https://shiny.cardosomoreiralab.org/fishplacentas/) — single-nucleus
RNA-seq from nine species, ATAC-seq from four, and the SCENIC+ regulatory
networks built from them: cell types, gene expression and chromatin
accessibility, side by side across species.

## Citation

Safian D\*, Kraunsoe S\*, Falis M, Labra L, Reznick D, Cardoso-Moreira M (2026).
A new cell type facilitated live-bearing and multiple independent origins of
placentation in fish. *[Journal]*. [DOI]

\* These authors contributed equally.

## Contact

Sophie Kraunsoe
(sophie.kraunsoe@crick.ac.uk), Diego Safian (diego.safian@crick.ac.uk) and Margarida Cardoso-Moreira
(margarida.cardosomoreira@crick.ac.uk), Evolutionary Developmental Biology
Laboratory, The Francis Crick Institute, London, UK.

