# 16S rRNA Gene Analysis of The Isolated Bacteria DNA from Soil Sample in Ranca Upas, West Java, Indonesia

![Ranca Upas](https://backpackerjakarta.com/wp-content/uploads/2016/09/Ranca-Upas-Bandung-Jawa-Barat.jpg)

View of Ranca Upas, West Java, Indoensia



## Context

**Background**

Microbial isolation and identification are essential for understanding microbial diversity in the environment. Soil, a complex ecosystem, harbors bacteria that play vital roles in nutrient cycling, organic matter decomposition, and soil health. Identifying these bacteria provides insights into their ecological functions and potential applications in agriculture and biotechnology.

The 16S rRNA gene is an ideal marker for bacterial identification, with conserved regions for universal primer design and variable regions for species differentiation. This gene helps classify bacterial species from diverse environments.

Ranca Upas in Ciwidey, West Java, is ecologically significant, with its unique soil influenced by climate, vegetation, and human activity. Analyzing bacterial DNA from this soil offers insights into its microbial composition.

This study employs BioPython, a powerful library for computational biology, to process and analyze sequences. The BLAST (Basic Local Alignment Search Tool) algorithm is used to compare the sequences against established databases, enabling identification of the bacteria.

**Objective of the Analysis**

The primary objective is to analyze and to identify bacterial sequence isolated from soil samples in Ranca Upas using BioPython and BLAST bioinformatics tools.

## Methods

### Sample Collection and Bacterial DNA Isolation

#### Sample Collection and Bacterial Colony Isolation

The soil sample was collected (Soil sample in Ranca Upas, West Java, Indonesia) using sterile tools to avoid contamination, ensuring an accurate representation of the microbial community. Once collected, the sample was stored on cooler box until it could be processed in the lab. In the lab, the soil sample was mixed with a sterile liquid, phosphate-buffered saline (PBS), and vigorously shaken to release bacteria from soil particles. Serial dilution was performed on the solution to reduce microbial concentrations. Then, diluted solution was spread on agar plates and incubated at the suitable temperature until colonies were seen on agar. Individual bacterial colonies were isolated on nutrient agar plates and further incubated to promote growth. After incubation, distinct colonies with unique morphologies were selected for DNA extraction. In this study, only one colony was selected for further investigation.

**Sampling Location**

![Sampling Location](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/Soil_bacteria_DNA_analysis_RancaUpas_WestJava_Indonesia/Sampling%20location.PNG)

#### DNA Extraction, Amplification, and Verification

DNA was extracted from the isolated bacterial colonies using a standard extraction kit, following the manufacturer’s instructions. The extracted DNA was then amplified by targeting the 16S rRNA gene, a well-conserved region suitable for bacterial identification, using universal primers. The amplification was performed with polymerase chain reaction (PCR) under optimized conditions, ensuring the production of high-quality DNA fragments specific to each bacterial species. Verification of successful amplification was confirmed through agarose gel electrophoresis, where the expected 1,500 base-pair (bp) bands were visualized under UV light.

#### Purification and DNA Sequencing

Following amplification, the PCR products were purified to remove excess primers and contaminants that might interfere with sequencing. The purified DNA was sent to Macrogen, Korea, for sequencing, where the Sanger method was applied to obtain high-quality reads of the 16S rRNA gene sequence for each isolate. This method allows precise determination of the nucleotide sequence, which is essential for accurate bacterial identification.

### Sequence Analysis using BioPython and BLAST

#### Sequences Preprocessing

The analysis began with processing the sequences received by importing them into Python using Biopython’s SeqIO module, which handles various sequence formats. After that, multiple reads were aligned and combined to generate a consensus sequence. Once the consensus sequence was obtained, it was prepared for further comparison.

#### BLAST Analysis with Biopython

After establishing the consensus sequence, Biopython's BLAST interface was used to align it against the NCBI nucleotide database to identify the bacterial species. The sequence was submitted to BLAST, and the resulting alignment scores, e-values, and match percentages were retrieved for comparison. This provide insight into the closest known sequences in the database, helping to confirm the bacterial identity by matching our consensus sequence with similar bacterial sequences already cataloged in the NCBI database.

#### Analysis of BLAST Results

We will analyse and evaluate the 10 results based on BLAST parameters such as query coverage, percent identity, E-value, and database matches.

**BLAST Results**

![Blast Results](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/Soil_bacteria_DNA_analysis_RancaUpas_WestJava_Indonesia/blast_result_pandas.PNG)

**Query Coverage**

* Low Coverage (28.8%): A query coverage of 28.8% means only a small portion of the query sequence aligns with the database sequences. This suggests that the sequence may be incomplete, or there is a significant mismatch between query and the available database entries. Moreover, the low coverage diminishes confidence in these matches as they represent only a fraction of the query sequence. 

**Percent Identity**

* Moderate Identity (76.1% - 77.9%): Percent identities ranging from 76.1% to 77.9% indicate that your query shares some similarities with the database sequences, but they are far from identical. For bacterial identification using 16S rRNA, a percent identity above 97%-99% is typically required for species-level identification, and 95%-97% for genus-level identification. These values suggest the query sequence might belong to a distant or uncharacterized relative of the listed species or even a novel bacterium.

**E-value**

* Significant Matches (1.39e-28 to 9.37e-31): The E-values are extremely low, which indicates the matches are statistically significant and unlikely to have occurred by chance. Despite low query coverage and moderate identity, the matches are real and relevant. However, they represent partial similarities rather than complete sequence identity.

**Database Matches**

* Most of the matches are described as Uncultured bacteria or Aerococcus sp.
* Uncultured Bacteria: Many entries are uncultured bacteria, which means they were identified from environmental samples.
* Aerococcus: Some matches, such as Aerococcus sp. or Aerococcus viridans, suggest that the sequence might belong to a bacterium within this genus. Furthermore, Aerococcus species are generally found in environmental samples like soil, water, or air and can sometimes be associated with clinical or agricultural contexts.


### Conlusion

Based on the current data, the sequence cannot be conclusively identified, and additional analysis or data collection is recommended. The matches suggest environmental or soil-dwelling bacteria related to Aerococcus, but the low coverage raises questions about the completeness of the alignment.

### Recommendations

There are some recommendations for the improvement of our result, such as:

* Use more specialized databases: Consider running the BLAST search against specialized 16S rRNA databases (e.g., SILVA, RDP, or Greengenes) that may contain more comprehensive entries for environmental bacteria.
* Expand analysis: Supplement the BLAST results with phylogenetic analysis or clustering methods to compare the query sequence against closely related bacteria.

## Asset
* [Notebook for Analysis](https://github.com/harishmuh/bioinformatics_biopython_projects/blob/main/Soil_bacteria_DNA_analysis_RancaUpas_WestJava_Indonesia/RancaUpas_Bacterial%20Sequence%20Analysis.ipynb)


