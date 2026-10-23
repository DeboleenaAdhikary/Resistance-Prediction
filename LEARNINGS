1. Papers I've read for this project's approach:
-  Orcales F, Moctezuma Tan L, Johnson-Hagler M, Suntay JM, Ali J, Recto K, Glenn P, Pennings P. Using genomic data and machine learning to predict antibiotic resistance: A tutorial paper. PLoS Comput Biol. 2024 Dec 30;20(12):e1012579. doi: 10.1371/journal.pcbi.1012579. PMID: 39775233; PMCID: PMC11684616.; 
-  Moradigaravand D, Palm M, Farewell A, Mustonen V, Warringer J, Parts L. Prediction of antibiotic resistance in Escherichia coli from large-scale pan-genome data. PLoS Comput Biol. 2018 Dec 14;14(12):e1006258. doi: 10.1371/journal.pcbi.1006258. PMID: 30550564; PMCID: PMC6310291.; 
-  Nguyen M, Long SW, McDermott PF, Olsen RJ, Olson R, Stevens RL, Tyson GH, Zhao S, Davis JJ. Using Machine Learning To Predict Antimicrobial MICs and Associated Genomic Features for Nontyphoidal Salmonella. J Clin Microbiol. 2019 Jan 30;57(2):e01260-18. doi: 10.1128/JCM.01260-18. PMID: 30333126; PMCID: PMC6355527. 
2. Prefixes:
- GSE/GSM are GEO, mostly expression data (like your RNA-seq work). They rarely come with MIC values.
- SRR/ERR/DRR are raw sequencing reads in SRA.
- GCA_/GCF_ are assembled genomes.
- SAMN are BioSamples, where antibiotic test results are sometimes attached.
3. Trial and Error method:
To choose parameters that need to be tweaked in models (such as λ) without touching the test set, split the training data into, say, 5 parts. Train on 4 and check on the 5th, rotate through all 5, and average. The folds should also be grouped by lineage, and practice amongst these groups. Make sure you touche the test set only once. After final model and settings are picked, run it on the test set one time.
4. HC stands for Hierarchical Cluster. The number indicates the allele-distance threshold used to define clusters. Lower thresholds generally produce smaller, more genetically similar clusters. Higher thresholds generally produce larger clusters.
- HC0: genomes have zero allele differences under the scheme's comparison rules.
- HC5: genomes are grouped using a threshold of 5 allele differences.
- HC50: the threshold is 50 allele differences.
- HC200: the threshold is 200 allele differences.
5. 
