# Data and scripts accompanying the PhyloNext manuscript

Pipeline documentation: [https://phylonext.github.io/](https://phylonext.github.io/)  
Pipeline source code: [https://github.com/vmikk/PhyloNext](https://github.com/vmikk/PhyloNext)  

Directory **Data** contains:  
- `Acacia_2013_parquet.7z` - the original dataset (based on [DOI:10.5061/dryad.33kn3](https://datadryad.org/stash/dataset/doi:10.5061/dryad.33kn3)) converted into Parquet format  
- `Acacia_2022Dec_parquet.7z` - the subset of *Acacia* species occurrences deposited in GBIF (as of December 2022)  
- `Acacia_2013_tree.nwk` - the original phylogenetic tree used in González-Orozco *et al.* (2013)  
- `Acacia_2022_OTT_tree.nwk` - phylogenetic tree fetched from the Open Tree of Life (does not contain tree tips imputed based on taxonomic data only)  
- `Acacia_GBIF_speciesKeys.txt` - GBIF species keys used to obtain a data subset comparable to the original dataset.  
- `Acacia_2022Dec_Dataset_DOIs.txt` - DOIs of datasets with Australian *Acacia* species occurrences  


Directory **Scripts** contains:  
- `Acacia_PhyloNext.txt` - the main script that performs the analysis  


Directory **Results** contains:  
- the obtained diversity estimates in tabular format (`Biodiverse_results_merged.txt`)  
- interactive choropleth maps (`Choropleth.html`)  
- results in GeoPackage format (`Diversity_estimates.gpkg`)  
- biodiversity estimates, along with the phylogenetic tree, in the native Biodiverse format (`Biodiverse.bds`)  

The test included:  
a) a nearly identical analysis of the original spatial dataset and phylogeny,  
b) analysis of original phylogeny with new filtered GBIF occurrence data with the original phylogeny,  
c) analysis of the original occurrence data with a custom synthetic phylogeny from OpenTree,  
d) analysis of new filtered GBIF occurrence data with a custom synthetic phylogeny from OpenTree.  


## `Acacia_2013_parquet.7z`

To make the dataset compatible with PhyloNext, it was converted into Apache Parquet file format. In the original dataset, species occurrences are in Lambert Conformal Conic projection for Australia, which was converted into latitude and longitude coordinates (`EPSG:4326`).  
In addition, several *Acacia* species were renamed according to the current classification system:

| Name in the original dataset | Updated name           |
| ---------------------------- | ---------------------- |
| *Acacia bancroftii*          | *Acacia bancroftiorum* |
| *Acacia bartleana*           | *Acacia microbotrya*   |
| *Acacia centrinervia*        | *Acacia lineata*       |
| *Acacia cometes*             | *Acacia lachnophylla*  |
| *Acacia cunninghamii*        | *Acacia cummingiana*   |
| *Acacia diphylla*            | *Acacia blakei*        |
| *Acacia eglandulosa*         | *Acacia cyclops*       |
| *Acacia homalophylla*        | *Acacia omalophylla*   |
| *Acacia hunteriana*          | *Acacia boormanii*     |
| *Acacia jutsonii*            | *Acacia heteroneura*   |
| *Acacia leichardtii*         | *Acacia leichhardtii*  |
| *Acacia microcephala*        | *Acacia microcybe*     |
| *Acacia perangusta*          | *Acacia fimbriata*     |
| *Acacia stowardii*           | *Acacia chamaeleon*    |
| *Acacia vincentii*           | *Acacia deltoidea*     |



## Citation:

### *Acacia* 2013 dataset:

González-Orozco CE, Laffan SW, Knerr N, Miller JT. (2013) Data from: A biogeographical regionalisation of Australian *Acacia* species. Dryad, Dataset [DOI:10.5061/dryad.33kn3](https://datadryad.org/stash/dataset/doi:10.5061/dryad.33kn3)  

González-Orozco CE, Laffan SW, Knerr N, Miller JT. (2013) A biogeographical regionalization of Australian *Acacia* species. The Journal of Biogeography, 40: 2156-2166. [DOI:10.1111/jbi.12153](https://onlinelibrary.wiley.com/doi/10.1111/jbi.12153)  

Mishler BD, Knerr N, González-Orozco CE, Thornhill AH, Laffan SW, Miller JT. (2014). Phylogenetic measures of biodiversity and neo- and paleo-endemism in Australian *Acacia*. Nature Communications, 5(1), 4473.  [DOI:10.1038/ncomms5473](https://www.nature.com/articles/ncomms5473)  

### *Acacia* 2022 dataset:

See the [`Data/Acacia_2022Dec_Dataset_DOIs.txt`](https://github.com/vmikk/PhyloNext_manuscript/blob/main/Data/Acacia_2022Dec_Dataset_DOIs.txt) file.  

