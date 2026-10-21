# A new cell type facilitated live-bearing and multiple independent origins of placentation in fish

Code and processed data for Safian, Kraunsoe et al. 2027 ([journal], [DOI]).

Live-bearing fishes in the family Poeciliidae have evolved placentas repeatedly
and recently, which makes them a natural experiment in how a new organ is built.
We profiled ovaries from nine poeciliid species, spanning species with and
without a placenta, to ask which cell types form the placenta in different
origins, how these cell types are specified, and what molecular changes they
undergo to enable nutrient transfer.

## In this repository

Code for the figure panels that can be rebuilt from the deposited data. Panels
that are microscopy, or whose analysis is described in the Methods rather than
driven by a script, are not reproduced.

### Main text figures

| File | Panels |
|---|---|
| [`figures/code_fig1.Rmd`](figures/code_fig1.Rmd) | (B) *P. turneri* and *P. prolifica* UMAPs; (C) SAMap correlation between them; (E) SAMap cell-type tree for the five placental species |
| [`figures/code_fig2.Rmd`](figures/code_fig2.Rmd) | (B) SAMap scores across the nine poeciliids; (D) *P. turneri* composition, adult against juvenile; (E) *P. gracilis* composition, pregnant against non-pregnant |
| [`figures/code_fig3.Rmd`](figures/code_fig3.Rmd) | (B) vitellogenesis and ovulation gene-set activity per cell type. Panels (A) and (C) are not reproduced here. |
| [`figures/code_fig4.Rmd`](figures/code_fig4.Rmd) | (B) TF motif activity across cell types; (C) consensus SCENIC+ regulatory networks |
| [`figures/code_fig5.Rmd`](figures/code_fig5.Rmd) | (E) conservation of TF-DEG interactions, for *P. turneri* and *P. bifurca* compared to *P. gracilis* and *P. picta*. Panels (B), (C) and (D) are not reproduced here. |

### Supplementary figures

| File | Panels |
|---|---|
| [`figures/supplementary/code_sf4.Rmd`](figures/supplementary/code_sf4.Rmd) | (A) cell-type tree from SAMap profiles; (B) tree from pseudobulk expression with bootstrap support |
| [`figures/supplementary/code_sf7.Rmd`](figures/supplementary/code_sf7.Rmd) | (A) global TF activity; (B) granulosa/theca and late follicle/germinal epithelium TF patterns |

## Reference data

Small reference tables are committed here and need no download:

```
data/reference/
|-- atac/
|   |-- Orthology/     one-to-one orthologue maps against turneri
|   |-- TF_lists/      the transcription factors scored per species
|   |-- TF_activity/   per-species TF motif activity by cell type
|   |-- cell_type_specific_eRegulons/
|   |                  SCENIC+ eRegulons for the late follicle cell, gzipped
|   |-- SCENICplus_eRegulons/   the full SCENIC+ eRegulon tables, gzipped
|   |-- SCENICplus_AUC/         binarised eRegulon activity per cell type
|   `-- SCENICplus_raw_pairs/   candidate TF-gene pairs, gzipped
|-- rna/
|   |-- Orthology/     the OrthoFinder/POSSVM orthology table
|   |-- SAMap/         pairwise SAMap mapping scores
|   |-- GO/            per-species gene-to-GO maps
|   `-- DEGs/          differential expression: one table per placental lineage
|                      against its sister, the same split by cell type, and
|                      topGO summaries of the up-regulated genes
`-- supplementary_tables/   orthology, positively selected genes, parallel substitutions
```

Only the single-nucleus atlases need downloading, from ArrayExpress. They are
read under the names ArrayExpress delivers, so nothing needs renaming; each
script opens with the accessions and the folder layout it expects.

## Running the figures

Each file is a standalone R Markdown document. Set `DATA_DIR` at the top to
wherever you unpacked the deposited data and knit; `REF_DIR` already points at
`data/reference/` in this repository. Every panel is printed into the rendered
document rather than written to disk, and each chunk states which panel it
produces.

## Data availability

* Single-nucleus RNA-seq: ArrayExpress [`E-MTAB-17757`](https://www.ebi.ac.uk/biostudies/arrayexpress/studies/E-MTAB-17757)
* Single-nucleus ATAC-seq: ArrayExpress [`E-MTAB-17776`](https://www.ebi.ac.uk/biostudies/arrayexpress/studies/E-MTAB-17776)
* Genome assemblies: ENA [`PRJEB115767`](https://www.ebi.ac.uk/ena/browser/view/PRJEB115767)
* Annotated Seurat objects for all eleven atlases, the ArchR projects and the
  SCENIC+ outputs are deposited alongside the raw data. Every atlas carries a
  `cell_type` column.

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

Sophie Kraunsoe (sophie.kraunsoe@crick.ac.uk)
Diego Safian (diego.safian@crick.ac.uk)
Margarida Cardoso-Moreira (margarida.cardosomoreira@crick.ac.uk)

Evolutionary Developmental Biology Laboratory, The Francis Crick Institute,
London, UK.

