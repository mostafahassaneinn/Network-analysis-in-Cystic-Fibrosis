# Network-analysis-in-Cystic-Fibrosis
Finding altered pathways and associated diseases in Cystic Fibrosis

## Project Description
### Background
Cystic fibrosis (CF) is one of the most severe autosomal recessive diseases. 
CF has been showing signs of becoming a more complicated illness than previously believed. 
By improving the clinical management of the disease, the patients' median predicted survival has increased until reaching the age of 50 years in some cases. 
CF transmembrane regulator (CFTR) is responsible for many pathological disease features. 
Therefore, it is important to get some insights about the hidden altered processes that can complicate the health state of cystic fibrosis patients. 

### Rationale
What are the associated diseases and pathways in cystic fibrosis?

### Study design 
![Alt text for screen readers](https://github.com/mostafahassaneinn/Network-analysis-in-Cystic-Fibrosis/blob/main/outputs/study_design.png)

### Input Data
Pre-processed dataset of human gene expression profiles obtained from Gene Expression Omnibus (GEO), identified by the accession number GSE40445

### Used Tools
- Cytoscape
- R
- GEO2R tool within GEO

### Methods
Differential gene expression analysis
Girvan-Newman (GN) algorithm
Enrichment analysis
Integration using DISEASES database
Filter out all non-informative interactions 
Filter for only the differentially expressed genes
Filter for only diseases with score >= 1 & connected to 8 genes or more
A Network of the first neighbours of the cystic fibrosis node --> adding pathways
A Network of the first and second neighbours of the cystic fibrosis node --> adding rare diseases

### Results
140 DEGs within Padj <0.05
![Alt text for screen readers](https://github.com/mostafahassaneinn/Network-analysis-in-Cystic-Fibrosis/blob/main/outputs/DEGs_volcano_plot.png)
#### Protein-protein interaction network of DEGs using STRING database
![Alt text for screen readers](https://github.com/mostafahassaneinn/Network-analysis-in-Cystic-Fibrosis/blob/main/outputs/DEGs.png)

#### Filter out genes with no connections
![Alt text for screen readers](https://github.com/mostafahassaneinn/Network-analysis-in-Cystic-Fibrosis/blob/main/outputs/DEGs_Filterd.png)

#### Functional enrichment analysis on main components and enrichment map
![Alt text for screen readers](https://github.com/mostafahassaneinn/Network-analysis-in-Cystic-Fibrosis/blob/main/outputs/Enrichment%20Map%20-%202ndC-%20DEGs.png)

#### Genes-Diseases network construction and Network extension with rare genetic diseases
![Alt text for screen readers](https://github.com/mostafahassaneinn/Network-analysis-in-Cystic-Fibrosis/blob/main/outputs/Gene_Diseses_rare_diseases.png)

#### Genes-Pathways network construction
![Alt text for screen readers](https://github.com/mostafahassaneinn/Network-analysis-in-Cystic-Fibrosis/blob/main/outputs/Gene_pathways.png)
*Gene-pathway network illustrates the genes that are directly connected to cystic fibrosis (CF) and pathways that are linked to these differentially expressed genes* 

### Conclusion
In conclusion, the data demonstrates that Cystic Fibrosis pathogenesis involves a complex molecular cross-talk where lipid metabolic shifts and purinergic/G-protein signaling alterations are deeply interconnected. This state is driven by core hubs like EP300 and manifests phenotypically through disruptions in epithelial barrier integrity (CLDN1), hyper-reactive interferon/immune pathways (IFNGR2), and metabolic elements (INSIG1, MAOB).
