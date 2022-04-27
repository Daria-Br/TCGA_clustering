# T cells produce interleukin-22 to promote CD155-driven lung metastasis 
### Briukhovetska, Suarez-Gosalvez & Voigt et. al.
Cluster Analysis of Lung adenocarcinoma and Breastcancer Cohorts from The Cancer Genome Atlas


## How to get started:
Welcome to our Repository. Here, you can find the Jupyter Notebooks and Source Data for our Cluster Analysis of TCGA LUAD and BRCA cohorts. Gene expression and phenotypic data was obtained from The Cancer genome Atlas [(TCGA)](https://www.cancer.gov/about-nci/organization/ccg/research/structural-genomics/tcga) via [UCSC Xenabrowser](https://xenabrowser.net/). Further, you can find how we preprocessed data for [CIBERSORTx](https://cibersortx.stanford.edu/) analysis, the results tables thereof and how we handled the data for our analysis.

### How to run?

Open a console and install the python libraries necessary for running the jupyter notebook, which are listed in "requrements.txt". Then, start a jupyter notebook of your choice using the command stated below.
```bash
pip install -r ./requirements.txt
jupyter notebook LUAD_IL22_Cluster_Analysis.ipynb
```

## Useful links:
+ **Library Documentations**:
    + [jupyter](https://docs.jupyter.org/en/latest/)
    + [pandas](https://pandas.pydata.org/docs/)
    + [numpy](https://numpy.org/doc/stable/reference/generated/numpy.power.html)
    + [scipy](https://docs.scipy.org/doc/scipy/index.html)
    + [scikit-learn](https://scikit-learn.org/stable/user_guide.html)
    + [matplotlib](https://matplotlib.org/)
    + [seaborn](https://seaborn.pydata.org/)
    + [lifelines](https://lifelines.readthedocs.io/en/latest/)
    + [openpyxl](https://openpyxl.readthedocs.io/en/stable/)
    
## Repository Structure:

+ **Figure_7**: Here, you can find the clustering and main analysis of the LUAD and BRCA cohorts as found in figure 7 and supplementary figure 7 in the manuscript.
    + **LUAD_IL22_Clusters**: This is the main analysis of the LUAD dataset.
        + **LUAD_IL22_Cluster_Analysis.ipynb**: This notebook contains the clustering and survival analysis of the LUAD cohort. Parts of this analysis can be seen in Figure 7 and supplementary Figure 7 of the manuscript.
        +**LUAD_IL22.tsv**: This file contains the genomic and phenotypic data used for the analysis.
        +**LUAD_abs_stage_counts.xlsx**: Output file of LUAD_IL22_Cluster_Analysis.ipynb with absolute counts of summarized pathologic cancer stages by cluster.
    + **BRCA_IL22_Clusters**: This is the main analysis of the BRCA dataset.
        + **BRCA_IL22_HER2+.ipynb**: This notebook contains the clustering and survival analysis of the HER2+ patients of the BRCA cohort. Parts of this analysis can be seen in Figure 7 and supplementary Figure 7 of the manuscript.
        + **BRCA_IL22.tsv**: This file contains the genomic and phenotypic data used for the analysis.
        + **BRCA_HER2+_Main_summary_stages.xlsx**: Output file of BRCA_IL22_HER2+.ipynb with absolute counts of summarized pathologic cancer stages by cluster.
        + **BRCA_HER2+_Main.xlsx**: Output file of BRCA_IL22_HER2+.ipynb containing scaled genomic, phenotypic, and cluster affiliation. 


+ **Cibersortx_Analysis**: Here, you can find how we prepared datasets for CIBERSORTx analysis as seen in supplementary figure 7.
    + **LUAD_CIBERSORTx**: Preprocessing of input files for CIBERSORTx analysis of the LUAD cohort and handling of the results tables for further analysis:
        + **LUAD_CIBERSORTx.ipynb**: Notebook containing the formatting for the input file for the deconvolution and the processing of the result file for the LUAD Cohort.
        + **LUAD_all_clusters_CISO.txt**: Input file for CIBERSORTx deconvolution.
        + **LUAD_Table_for_decon.xlsx**: Table containing cluster labels from the main cluster analysis of the LUAD cohort.
        + **CIBERSORTx_Job1_Results_LUAD_all_clusters.xlsx**: CIBERSORTx results for the clustered LUAD cohort.
        + **LUAD_LM22.tsv**: Unfiltered gene expression table based on the [LM22](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5895181/) signature matrix from the LUAD cohort.
    
    + **BRCA_CIBERSORTx**: Preprocessing of input files for CIBERSORTx analysis of the BRCA cohort and handling of the results tables for further analysis:
        + **BRCA_CIBERSORTx.ipynb**: Notebook containing the formatting for the input file for the deconvolution and the processing of the result file for the BRCA Cohort.
        + **BRCA_all_clusters_CISO.txt**: Input file for CIBERSORTx deconvolution.
        + **BRCA_all_clusters_CISO.txt**: Table containing cluster labels from the main cluster analysis of the BRCA cohort.
        + **BRCA_CIBERSORTx_Job3_Results.xlsx**: CIBERSORTx results for the clustered BRCA cohort.
        + **BRCA_LM22.tsv**: Unfiltered gene expression table based on the [LM22](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5895181/) signature matrix from the BRCA cohort.
    
    
+ **Stage_Specific_Survival**: 
    + **BRCA_Stage_Specific_Survival**
        + **BRCA_Stage_Specific_Survival.ipynb**: Notebook contaning the stage specific survival analysis for the HER2 positive BRCA patients.
        + **BRCA_HER2+_Main.xlsx**: Output file from the main cluster analysis, here used as input for stage specific survival analysis.
    + **LUAD_Stage_Specific_Survival**
        + **LUAD_Stage_Specific_Survival.ipynb**: Notebook contaning the stage specific survival analysis for the LUAD patients.
        + **LUAD_pheno_analysis.xlsx**: Output file from phenotypic analysis after clustering of the patients, here used as input for stage specific survival analysis.
        
+ **Cohort_Info_Table**: This folder contains notebooks and tables used for creating a descriptive table of the cohorts.
    + **TCGA_BRCA_Further_Phenotypic_analysis**
        +  **TCGA_BRCA_Further_Phenotypic_analysis.ipynb**: Notebook for counting phenotypical features.
        + **BRCA_pheno.tsv**: Input file containing phenotypical data for the BRCA cohort.
        + **BRCA_pheno_analysis**: Output file from the phenotypic analysis.
        + **BRCA_HER2+_Main.xslx**: Output file from the main clustering analysis. Here, used for the cluster labels.
    + **TCGA_LUAD_Further_Phenotypic_analysis**
        + **TCGA_LUAD_Further_Phenotypic_analysis.ipynb**: Notebook for counting phenotypical features.
        + **Phenotypic_data_LUAD.tsv**: Input file containing phenotypical data for the LUAD cohort.
        + **LUAD_Table_for_decon.xlsx**: Output file from the main clustering analysis. Here, used for the cluster labels.
        + **LUAD_pheno_analysis.xlsx**: Output file from the phenotypic analysis.

+ **requirements.txt**: Text file containing the python libraries and version info required for running the notebooks.

