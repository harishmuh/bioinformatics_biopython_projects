# 16S rRNA Gene Sequence and Phylogenetic Analysis of Vibrio isolates using Biopython Library
A study case from a Shrimp Pond in Patrol, Indramayu, West Java, Indonesia

![Shrimp pond Indramayu](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/vibrio_isolate_analysis_Indramayu_Indonesia/data_and_assets/Shrimp%20pond%20-%20Petrol%20Indramayu.jpg)

## Context
**Background**

Shrimp aquaculture is a vital contributor to global seafood production, supporting livelihoods and economies worldwide. However, the industry is highly vulnerable to disease outbreaks, with vibriosis being one of the most devastating bacterial infections affecting shrimp. Vibriosis is caused by species of the genus Vibrio, and outbreaks can result in mortality rates exceeding 70% in affected ponds, significantly impacting production and leading to economic losses estimated at billions of USD annually (De Schryver et al., 2014; Soto-Rodriguez et al., 2015). Pathogenic Vibrio species such as Vibrio harveyi, Vibrio parahaemolyticus, Vibrio alginolyticus, and Vibrio vulnificus are commonly associated with shrimp diseases, causing symptoms ranging from septicemia and luminescent bacterial disease to slow growth and death.

**Some Clinical signs of Vibriosis** (Aguilera-Rivera et al, 2019): 
 
![Clinical signs](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/vibrio_isolate_analysis_Indramayu_Indonesia/data_and_assets/vibriosis%20signs%20-%20Aguilera-Rivera%20et%20al%202019.PNG)

A. Melanization B. Necrosis in uropods C. Redness (Erythema) in appendages or body parts

Indonesia, a major player in global shrimp aquaculture. The north coast of Java, particularly Indramayu, is a crucial hub for shrimp aquaculture in Indonesia. Shrimp ponds in this area are vital for local and national economies, yet they are highly susceptible to vibriosis outbreaks due to the prevalence of Vibrio species in the aquatic environment. Understanding the composition and diversity of Vibrio populations in these ecosystems is essential for the development of effective disease management strategies.

One powerful approach for identifying bacterial species and understanding their evolutionary relationships is the analysis of the 16S ribosomal RNA (rRNA) gene. This gene is a highly conserved molecular marker that provides taxonomic and phylogenetic insights into bacterial communities. By sequencing the 16S rRNA gene, researchers can distinguish pathogenic Vibrio species and study their relationships, which is essential for developing biosecurity measures and disease prevention programs in aquaculture.

In this study, bioinformatic analysis was performed on the 16S rRNA sequences of Vibrio isolates collected from shrimp ponds in Patrol, Indramayu, West Java. Furthermore, the Biopython library was employed to help the analysis by supporting biological computation, facilitating tasks such as sequence alignment, data parsing, and phylogenetic tree construction.

**The Objective of the Analysis**

Molecular identification:
* To analyze the identity of Vibrio isolates through 16S rRNA gene sequencing and BLAST analysis with Biopython library
  
Phylogenetic tree relationship:
* To construct phylogenetic tree and analysis using Biopython library and BioPhylo Module and to elucidate the relationship of isolate with other vibrio species.
  
Pathogenic potential in Aquaculture:
* To investigate the potential pathogenicity of the isolates by analyzing their association with pathogenic Vibrio species (e.g., Vibrio rotiferianus, Vibrio harveyi, Vibrio owensii)

## Sample collection, Vibrio's DNA Isolation, and Sequencing

**Sampling Location**

The study was conducted on pond water from a shrimp farm, located in the north coastal area of Java, in Patrol district, Indramayu, West Java, Indonesia.

![Folium map](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/vibrio_isolate_analysis_Indramayu_Indonesia/data_and_assets/folium%20geo%20map.PNG)

![GeoPandas map](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/vibrio_isolate_analysis_Indramayu_Indonesia/data_and_assets/Sampling%20locations%20-%20geopandas.PNG)

**Sample Collection and Isolation**

Water samples were collected from shrimp ponds and placed into sterile containers. The containers stored in a cool box to maintain sample integrity, and transported to the laboratory at the Bandung Institute of Technology. All samples were processed within 24 hours to ensure reliable microbial recovery.

**Vibrio Bacteria Isolation**

In the laboratory, water samples were spread onto Thiosulfate Citrate Bile Salt Sucrose (TCBS) agar, a selective medium designed for isolating Vibrio species. The plates were incubated at 28°C for 24 hours, similar to the shrimp pond environment. After incubation, distinct colonies were examined for morphological characteristics, and representative colonies were selected for further analysis. In this study, there were two distinct colonies that consistent to be present during overall sampling period. The two grown colonies in the TCBS were hypothesized as Vibrio isolates, but we will verify the identity on the next steps.

To be more practical, these two isolates will be mentioned later as

* First Isolate: **Isolate Indramayu 1**
* Second Isolate: **Isolate Indramayu 2**

**DNA Extraction, Amplification, and Verification**

* DNA was extracted from the isolated bacterial colonies using a standard extraction kit (a PCR Ready-to-Go kit), following the manufacturer’s instructions. The extracted DNA was then amplified by targeting the 16S rRNA gene, a well-conserved region suitable for bacterial identification, using universal primers. The amplification was performed with polymerase chain reaction (PCR) under optimized conditions, ensuring the production of high-quality DNA fragments. Verification of successful amplification was confirmed through agarose gel electrophoresis, where the expected 1,500-1600 base-pair (bp) bands were visualized under UV light.

**Purification and DNA Sequencing/Sequence Characterization**

* Following amplification, the PCR products were purified to remove excess primers and contaminants that might interfere with sequencing. The purified DNA was sent to Macrogen Inc., Korea, for sequencing, where the Sanger method was applied to obtain high-quality reads of the 16S rRNA gene sequence for each isolate.

**Bioinformatic Analysis**

* All bioinformatic analysis was conducted using biopython library and modules. The biopython library facilitates bioinformatic analyses and provides robust tools for interacting with biological databases, manipulating sequences, and automating bioinformatics workflows. The library also contains modules to use BLAST (Basic Local Alignment Search Tool), conduct multiple alignment, distance matrix calculation, and phylogenetic tree construction and visualization (Cock et.al, 2009).

## Isolate sequence analysis using Biopython library and BLAST

This steps mainly started from preprocessing the sequence files into working FASTA format and conducting analysis using BLAST.

**BLAST Analysis with Biopython**

* After the sequences were pre-processed, Biopython's BLAST (MEGABLAST) interface was used to align it against the NCBI nucleotide database to identify the bacterial species. A function for running MEGABLAST was created to facilitate the work. MEGABLAST setting was preferred than the usual BLASTN as we wanted to find highly similar matches to identify closely related sequences.

* The sequence was submitted to MEGABLAST, and the resulting alignment scores, query coverage, e-values, and match percent identity were retrieved for comparison. These parameters were used to provide insight into the closest known sequences in the NCBI database, helping to confirm the bacterial identity by matching sequence with similar sequences already cataloged in the NCBI database. Furthermore, An additional constraint, maximum alignment length (1600 bp), was inputed into query to make sure the BLAST's results contained only 16S rRNA gene sequence.

## Phylogenetic Tree Construction and Visualization
We conducted phylogenetic tree construction and visualization for the first isolat (Isolate Indramayu 1) and second isolate (Isolat Indramayu 2) separately. The phylogenetic analysis was performed to assess their evolutionary relationships with known Vibrio species sequences obtained from the NCBI database. For this purpose, the UPGMA (Unweighted Pair Group Method with Arithmetic Mean) algorithm was utilized, a method particularly suited for 16S rRNA gene-based analyses due to its reliance on pairwise genetic distances and the assumption of a constant molecular clock. The trees were constructed and visualized using the robust tools provided by the Biopython library's Phylo module. The steps for creating phylogenetic tree can be breakdown as:

**Sequence collection and setting an outgrup**

* The phylogenetic tree construction began with identifying similar sequences from the NCBI database based on the previous step in MEGABLAST analysis. Sequences with high percent identity and very low e-values were selected and downloaded using Biopython's Entrez module. Additionally, an Escherichia coli 16S rRNA gene sequence was included as an outgroup to root the tree. All sequences, including the sequence of respective isolate and the downloaded reference sequences, were saved in FASTA format for alignment.

**Preprocessing: Multiple sequences alignment**

* The sequences were aligned using the ClustalW2 tool to ensure homologous regions were accurately compared.

**Distance matrix calculation**

* From the aligned sequences, a genetic pairwise distance matrix was computed using Biopython's DistanceCalculator. This matrix quantified the genetic dissimilarity between sequences based on nucleotide differences.

**Clustering: UPGMA algorithm**

* The clustering process employed Biopython's DistanceTreeConstructor class, which uses the UPGMA algorithm to iteratively group sequences with the smallest genetic distances. UPGMA progressively merges the closest sequences into clusters, ultimately computing a rooted tree that reflects the evolutionary relationships among all included sequences.

**Additional settings: Mapping ID to species**

* The resulting phylogenetic tree was exported in Newick format, and the sequence labels were updated to display species names by mapping sequence IDs to corresponding species information. This labeling provided a clearer interpretation of the relationships depicted in the tree.

**Phylogenetic Tree Visualization**
* The finalized phylogenetic trees for both Vibrio isolates were visualized using Biopython's Phylo.draw() method. This visualization presented a rooted tree, with the common ancestor of all sequences positioned at the root.

## Results and Discussions

### BLAST Results and Insights

**First Isolate BLAST Results**
![First isolate BLAST](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/vibrio_isolate_analysis_Indramayu_Indonesia/data_and_assets/MegaBlast_isolat_1_indramayu.PNG)

### **Insights - BLAST result (First isolate)**

Based on the MEGABLAST results from the first isolate sequence, isolate shows very high similarity to multiple Vibrio species. We could point out some insights:

* The highest scoring of MEGABLAST matches suggest that the sequence is closely related to species including Vibrio sp. YASM14 (99.93% percent identity and full query coverage) and Vibrio rotiferianus strain 32BCA (99.93% percent identity and 99.73% query coverage)
* Some hits were labeled as "Uncultured" (e.g., Uncultured bacterium clone 8M39), indicating sequences derived from environmental samples. These results may represent environmental strains, possibly adapted to a specific habitat or host (in aquaculture ecology), closely related to cultured Vibrio species.
* Several other strains of Vibrio rotiferianus (e.g., WCM6, CUVET, etc.) also have high identity (99.87–99.93%) and query coverage (~99.8%), suggesting a close evolutionary relationship with this species.
* The similarity of the sequeces to multiple species (Vibrio sp., Vibrio rotiferianus, Vibrio campbellii) also raised the possibility of the sample being a **hybrid strain**.



**Second Isolate BLAST Results**

![Second Isolate](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/vibrio_isolate_analysis_Indramayu_Indonesia/data_and_assets/MegaBlast_isolat_2_indramayu.PNG)

### **Insights - BLAST Results (Second Isolate)**

* The highest-ranking match was **Vibrio sp. MY-2008-U5** with 100% identity and 97.61% query coverage.
* The second highest matches were (**Vibrio sp. strain WAB2255** and **Vibrio owensii**) have 99.93% percent identity and 97.61 query coverage)
* Some other entries (Vibrio sp. strain WAB2255, Vibrio owensii, Vibrio harveyi, etc.) highlight matches with multiple Vibrio species or strains, such as Vibrio owensii, Vibrio harveyi, and uncultured Vibrio species.
  

### Phylogenetic Tree Insights


**First Isolate Phylogenetic Tree**

![First Isolate Phylogenetic Tree](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/vibrio_isolate_analysis_Indramayu_Indonesia/data_and_assets/1.%20The%20Phylogenetic%20tree%20of%20first%20isolate.PNG)

### **Insights of The Phylogenetic Tree (First Isolate)**


Based on visual overview of the phylogenetict tree, it appears that there are 3 distinct clusters and an outgroup.

**Outgrup**
* Includes: Escherichia_coli_16S
* This species serves as a clear outgroup, showing significant divergence from the Vibrio species. Its separation to Vibrio species helps validating the phylogenetic analysis as Eschericia coli belongs to a different genus.

**Cluster 1: Vibrio rotiferanus group**
* Includes: Vibrio rotiferianus_partial_16, Vibrio_campbellii_strain_XTF-1, Vibrio_rotiferianus_WCM6, Vibrio_rotiferianus_CUVET, Vibrio_rotiferianus_32BCA and Indramayu Isolate 1.
* This cluster is mostly dominated by Vibrio rotiferianus species.
Indramayu Isolate 1 is closely grouped with Vibrio_rotiferianus_WCM6, showing a very small branch length from it.
* The Vibrio rotifieranus species and Vibrio Campbellii are often associated with pathogenicity in aquaculture, especially causing vibriosis in shrimp and other marine species.

**Cluster 2: Vibrio harveyi and Related Species**
* Includes: Vibrio_harveyi_NB0901, Vibrio_sp._YASM14, Vibrio_sp._YASM15, Uncultured_bacterium_8M39, and Uncultured_bacterium_YZ20
* This cluster contains Vibrio harveyi, a well documented aquaculture pathogen, causing luminescent vibriosis in shrimp (Austin and Zhang, 2006).
According to the tree, Vibrio_sp._YASM14 and Vibrio_sp._YASM15 are closely related to Vibrio harveyi.
* Environmental uncultured Vibrio species (8M39 and YZ20) also appear here, possibly an environmental variant or less characterized Vibrio strains.

**Cluster 3: Environmental Vibrio Species**
* Includes: Vibrio_sp._S1-3-7, Uncultured_Vibrio_sp._1_142, Uncultured_Vibrio_sp._2_99
* This cluster contains uncultured Vibrio species and environmental isolates.
* These species may have less pathogenic potential compared to the first two clusters but could still play roles in opportunistic infections.
  
**Insights of Relationship - Indramayu isolate 1 and other Vibrio Species**
* The Indramayu Isolate I is closest to the Vibrio_rotiferianus_WCM6 and this close relationship places the isolate in the cluster 1. This also suggests a stronger evolutionary ties to this Vibrio rotiferianus strains.
* Moreover, Its position within Cluster 1 implies that the Indramayu isolate 1 may have pathogenic potential, as Vibrio rotiferianus species are known pathogens in aquaculture.

**Second Isolate Phylogenetic Tree**

![Second Isolate Phylogenetic Tree](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/vibrio_isolate_analysis_Indramayu_Indonesia/data_and_assets/2.%20The%20Phylogenetic%20tree%20of%20second%20isolate.PNG)

### **Insights of The Phylogenetic Tree (Second Isolate)**


According to the second isolate phylogenetic tree, Its appear there are at least 4 clusters and outgrup.

**Outgroup**
* Includes: Escherichia_coli_16S
* This species is distinct that clearly represent it position as outgroup, with longer branch lengths separating it from Vibrio species, as expected due to its taxonomic difference.

**Cluster 1: Vibrio Cluster, Pathogenic subgroup 1 (inner 6)**
* Includes: Vibrio harveyi NBVh-Sp2, Vibrio sp. HD-1, Vibrio owensii NBVo-Mr1
* Beside well documented pathogenic Vibrio harveyi, Vibrio owensii is known for its pathogenic potential in marine organisms (Isnansetyo et al, 2022)
* They may share ecological roles or pathogenic traits relevant to aquaculture, such as causing disease outbreaks in shrimp farming.
* The close relationship suggests they might have diverged recently or share a common habitat.

**Cluster 2: Vibrio Cluster, Pathogenic subgroup 2 (inner 14)**
* Includes: Vibrio harveyi SW-3, Vibrio sp. MY-2008-32d, Vibrio sp. MY-2008-U24, Vibrio sp. MY-2008-U9, Vibrio sp. MY-2008-U27
* This cluster could represent a subgroup with specific adaptations or pathogenic factor as well for aquaculture species as this contains Vibrio harveyi.

**Cluster 3: Environmental vibrio (Inner 22)**
* Includes: Indramayu Isolate 2, Vibrio sp. W-13, Vibrio communis J821, Vibrio communis F052, Uncultured bacterium MAY6C41
* This group, including Indramayu Isolate 2, seems more environmentally adapted to the specific location. Potentially has role pond microbiomes and nutrient cycle.

**Cluster 4: Distict Gamma Group (inner 17)**
* Includes: Uncultured gamma, Vibrio owensii GISD-4
* This cluster's branch lengths suggest genetic divergence from other Vibrio species (Cluster 2), hinting at unique ecological or evolutionary pathways.

**Insights of Relationship - Indramayu isolate 2 and other Vibrio Species**

* Indramayu Isolate 2 clusters within an environmentally adapted group, grouped in a cluster with other Vibrio species (Vibrio communis and Vibrio sp. W-13), indicating a shared evolutionary origin or genetic similarity. This grouping suggests these species may share common ecological roles or genetic traits, such as environmental adaptation or metabolic pathways.
* While Vibrio communis and Vibrio sp. W-13 are not among the commonly studied highly pathogenic species in shrimp or other marine hosts and the Indramayu Isolate 2 does not group inside with the highly pathogen Vibrio harveyi, the location of Indramayu Isolate 2 in the UPGMA tree that near pathogenic Vibrio (e.g, Vibrioi owensii) might have some pathogenic potential.
* Alternatively, Indramayu Isolate 2 could be a commensal species or play a role in nutrient cycling in the shrimp pond ecosystem.
* However, It may act as an opportunistic pathogen as well, causing disease when environmental or host conditions are compromised (e.g., poor water quality, high organic load).


## Conclusions

This study investigated the genetic identification, phylogenetic relationship, and potential pathogenicity of two Vibrio isolates obtained from shrimp pond water in Indramayu, Indonesia, using 16S rRNA sequencing, BLAST analysis, and phylogenetic tree construction.

**BLAST Analysis**

* First Isolate: MEGABLAST results revealed a very high similarity (99.93% identity) to Vibrio sp. YASM14 and Vibrio rotiferianus strain 32BCA. These species are known to be associated with aquaculture environments and may have pathogenic potential.
* Second Isolate: The closest match was Vibrio sp. MY-2008-U5 with 100% identity and 97.61% query coverage. Other matches included Vibrio harveyi and Vibrio owensii, both of which are known aquaculture pathogens.

**Phylogenetic Tree Analysis**

* First Isolate: Indramayu Isolate 1 clustered closely with Vibrio rotiferianus WCM6 in a group dominated by V. rotiferianus species, suggesting strong evolutionary ties and potential pathogenicity similar to known vibriosis-causing species.
* Second Isolate: Indramayu Isolate 2 grouped with Vibrio communis and Vibrio sp. W-13, indicating an environmentally adapted cluster. Despite its non-association with highly pathogenic strains, its proximity to Vibrio owensii suggests it could have opportunistic pathogenic traits under unfavorable conditions.

**Potential Pathogenicity for Aquaculture**

* First Isolate: The close association with V. rotiferianus species, known for causing shrimp vibriosis, strongly indicates pathogenic potential.
* Second Isolate: Though part of an environmentally adapted cluster, its similarity to Vibrio communis and proximity to pathogenic Vibrio owensii raise concerns about its opportunistic pathogenicity, especially in stressed aquaculture environments.

## Recommendations
**Monitoring and Management**
* Regular monitoring of shrimp ponds for Vibrio species, including both isolates, to detect early signs of potential outbreaks.
* Improve water quality management to prevent opportunistic infections by reducing organic loads and environmental stressors.

**Further Research**
* Perform virulence factor testing and experimental infections to confirm the pathogenicity of Indramayu Isolates 1 and 2.
Conduct whole-genome sequencing to identify genes linked to pathogenicity (eg., Virulence gen PirA and PirB) and antibiotic resistance.

## References
* Aguilera-Rivera, D., Prieto-Davó, A., Rodríguez-Fuentes, G., Escalante-Herrera, K. S., & Gaxiola, G. (2019). A vibriosis outbreak in the Pacific white shrimp, Litopenaeus vannamei, reared in biofloc and clear seawater. Journal of Invertebrate Pathology, 167, Article 107249.
* Austin, B., & Zhang, X. H. (2006). Vibrio harveyi: A significant pathogen of marine vertebrates and invertebrates. Letters in Applied Microbiology, 43(2), 119–124. 
* Cock PJ, Antao T, Chang JT, Chapman BA, Cox CJ, Dalke A, Friedberg I, Hamelryck T, Kauff F, Wilczynski B, and de Hoon MJL (2009). Biopython: freely available Python tools for computational molecular biology and bioinformatics. Bioinformatics, 25, 1422-1423.
* De Schryver, P., Defoirdt, T., & Sorgeloos, P. (2014). Early mortality syndrome outbreaks: A new paradigm in shrimp farming? Reviews in Aquaculture, 6(4), 227-237.
* Isnansetyo, A., Istiqomah, I., Anshary, H., Sriwulan, S., Yudiati, E., Subagiyo, S., Arif, A., & Kartikasari, D. W. (2022). Identification and antibiotic-resistant properties of Vibrio owensii and V. alginolyticus isolated from the Spermonde Islands, Indonesia. Biodiversitas, 23(11), 5995–6005.
* Soto-Rodriguez, S. A., et al. (2015). Virulence of Vibrio species isolated from diseased shrimp. Aquaculture, 448, 52-58.
* Thompson, F. L., Iida, T., & Swings, J. (2004). Biodiversity of Vibrios. Microbiology and Molecular Biology Reviews, 68(3), 403-431.

## Asset
* [Notebook of Analysis]()


