# **In Silico Phylogenetic Analysis of Fish Species in The Batanghari River, Indonesia, using Biopython and FastTree Library**

![River in Jambi](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/in_silico_analysis_fish_species_BatanghariRiver_Indonesia/data_and_assets/map%20of%20Jambi%20river.PNG)

## **Context**
The Batanghari River, located in central Sumatra, Jambi, Province, Indonesia, is one of the region’s largest and most ecologically significant rivers. Its basin spans multiple provinces and encompasses diverse habitats, including freshwater lakes, wetlands, and mangrove ecosystems. These varied habitats support a remarkable diversity of aquatic life, particularly fish species. However, growing human activities such as deforestation, urbanization, and pollution pose significant threats to the river's biodiversity.

Preserving the biodiversity of the Batanghari River is vital, not only for ecological stability but also for maintaining the river’s role in supporting local livelihoods and regional ecosystems. Additionally, understanding the relationships among fish species may offer critical insights into their ecological roles, which can guide effective conservation strategies.

### **In Silico study**
In silico study was conducted based on the previous research paper by Nurdawati (2007), which explored the diversity and distribution of fish species in the Batanghari River. Sampling sites included various lakes and rivers in Jambi, such as Teluk Lake, Buluran Kenali Lake, Kaos Lake, and the Terap, Lubuk Ruso, and Pijoan Rivers. The 20 freshwater fish species were selected from Nurdawati’s findings to be used for this study. Their genetic data were retrieved from the NCBI GenBank database. Although the sequences are not from specimens directly collected in the Batanghari River, they are expected to represent genetically similar populations, providing valuable insights into the evolutionary relationships among these species. This in silico approach offers a cost-effective and time-efficient alternative to traditional wet lab experiments. By leveraging bioinformatics tools, the study can analyze fish species' evolutionary relationships without requiring DNA extraction or sequencing.

### **Objective of the Analysis**
The main objectives of this in silico study are:

* To construct a phylogenetic tree using Biopython and FastTree libraries.
* To determine the evolutionary relationships among fish species from various habitats in the Batanghari River basin.

### **Dataset Source**
* Scientific Basis: Nurdawati, S. (2007). [Study on biodiversity and distribution of fish fry in some type of habitats of Batanghari 
River basin, Jambi (Abstract)](https://www.e-jurnal.com/2018/01/keanekaragaman-dan-distribusi-benih.html#more), [Article](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/in_silico_analysis_fish_species_BatanghariRiver_Indonesia/data_and_assets/nurdawati%20-%202007.pdf)
* Genetic Data: DNA sequences for the selected fish species will be obtained from the NCBI GenBank database.

## **Data Collection**

| Accession ID  | Species                   |
|---------------|---------------------------|
| MW591010.1    | Barbodes schwanenfeldii   |
| FJ753486.1    | Chela maassi              |
| MN243487.1    | Parachela oxygastroides   |
| KF410686.1    | Macrochirichthys macrochirus |
| MN342802.1    | Rasbora kalochroma        |
| MN342789.1    | Rasbora caudimaculata     |
| MN342865.1    | Rasbora heteromorpha      |
| EF452873.2    | Rasbora dorsiocellata     |
| MN342798.1    | Rasbora dusonensis        |
| MK567225.1    | Rasbora argyrotaenia      |
| KM213055.1    | Puntius johorensis        |
| KP856763.1    | Osteochilus hasseltii     |
| GQ911724.1    | Betta anabatoides         |
| KT250368.1    | Trichopsis vittata        |
| KU692544.1    | Helostoma temminckii      |
| KM213043.1    | Belontia hasselti         |
| MW627474.1    | Channa striata            |
| KJ937430.1    | Channa lucius             |
| JN024962.1    | Channa micropeltes        |
| KJ937390.1    | Channa pleurophthalmus    |
| MN256459.1    | Anguillicola crassus      |

## **Result and Key Insights**

**Phylogenetic Tree**
![Phylogenetic tree](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/in_silico_analysis_fish_species_BatanghariRiver_Indonesia/data_and_assets/Phylogenetic%20tree%20analysis%20-%20maximum%20likelihood.PNG)

**Phylogenetic Tree Clusters and Insights**

The phylogenetic tree constructed using the Maximum-Likelihood (ML) method reveals four main clusters of fish species, alongside the role of an outgroup species. Below is the detailed interpretation of the clusters, species relationships, and evolutionary patterns:

**Outgroup**

* Anguillicola crassus is located at the far right of the tree and serves as the outgroup. Its placement indicates that it is genetically distinct from the other taxa and is used to root the tree, providing a reference point to understand the evolutionary divergence among the other species.

**Cluster 1: Belontia, Betta, and Related Species**
* Includes: Osteochilus hasseltii, Barbodes schwanenfeldii, Puntius johorensis, Betta anabatoides, and Trichopsis vittata.
* Insights:
  * This cluster represents species with relatively close genetic relationships, potentially due to shared habitats or ecological roles.
  * Within this cluster, Belontia hasseltii and Betta anabatoides form a smaller, distinct subgroup, suggesting they are closely related within the evolutionary tree.

**Cluster 2: Channa Species Group**
* Includes: Channa striata, Channa lucius, Channa micropeltes, and Channa pleurophthalmus.
* Insights:
  * These species form a closely related clade, indicating they share a recent common ancestor.
  * The relatively short branch lengths within this group suggest low genetic divergence, which may reflect similar ecological niches or recent speciation events.

**Cluster 3: Rasbora Species Group**
* Includes: Rasbora kalochroma, Rasbora heteromorpha, Rasbora caudimaculata, Rasbora dorsocellata, Rasbora dusonensis, and Rasbora argyrotaenia.
* Insights:
  * These species cluster together in a distinct clade, representing the Rasbora genus within the Cyprinidae family.
  * Their grouping reflects close evolutionary relationships and likely diversification from a shared ancestral species.

**Cluster 4: Divergent Species**
* Includes: Parachela oxygastroides and Macrochirichthys macrochirus.
* Insights:
  * These species are placed on longer branches, indicating higher genetic divergence compared to other groups.
  * Their evolutionary distinctiveness suggests adaptation to different ecological pressures or more ancient divergence from the other taxa.
 
## **Conclusion**
* The phylogenetic tree based on evolutionary relationship among fish species in the Batanghari River has been constructed using biopython and FastTree library.
* Based on the selected DNA sequences of fish species from the BatangHari River, the phylogenetic analysis identified 4 clusters of fish species with close genetic relationships (and Anguilocola grassus serves as an outgrup, not belong to any cluster).

**Implications for Future Studies**
* This analysis establishes a baseline for the molecular understanding of Batanghari River fish species. Future research should integrate locally sequenced genetic data and ecological studies to validate and enhance the findings.
* Additional genetic markers, such as nuclear DNA, may be included to complement mitochondrial DNA in studying hybridization or deeper evolutionary patterns.
