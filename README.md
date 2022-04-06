# T cells produce interleukin-22 to promote CD155-driven lung metastasis 
### Briukhovetska, Suarez-Gosalvez & Voigt et. al.
Cluster Analysis of Lung adenocarcinoma and Breastcancer Cohorts from The Cancer Genome Atlas


## How to get started:
Welcome to our Repository. Here, you can find the Jupyter Notebooks and Source Data for our Cluster Analysis of TCGA LUAD and BRCA cohorts. Gene expression and phenotypic data was obtained from The Cancer genome Atlas [(TCGA)](https://www.cancer.gov/about-nci/organization/ccg/research/structural-genomics/tcga) via [UCSC Xenabrowser](https://xenabrowser.net/).

### How to run?

How to start a Jupyter Notebook and install the necessary libraries by example of the main LUAD clustering analysis:
```bash
pip install -r ./requirements.txt
jupyter notebook LUAD_IL22_Cluster_Analysis.ipynb
```
### Repository Structure:

+ **Figure_7**: Here, you can find the clustering and main analysis of the LUAD and BRCA cohorts
    + **LUAD_IL22_Clusters**: This is the main analysis of the LUAD dataset.
        + **LUAD_IL22_Cluster_Analysis.ipynb**: This notebook contains the clustering and survival analysis of the LUAD cohort. Parts of this analysis can be seen in Figure 7 and supplementary Figure 1 of the manuscript.
        +**LUAD_IL22.tsv**: This file contains the genomic and phenotypic data used for the analysis.
        +**LUAD_abs_stage_counts.xlsx**: Output file of LUAD_IL22_Cluster_Analysis.ipynb with absolute counts of summarized pathologic cancer stages by cluster.
    + **BRCA_IL22_Clusters**: This is the main analysis of the BRCA dataset.
        + **BRCA_IL22_HER2+.ipynb**: This notebook contains the clustering and survival analysis of the HER2+ patients of the BRCA cohort. Parts of this analysis can be seen in Figure 7 and supplementary Figure 1 of the manuscript.
        + **BRCA_IL22.tsv**: This file contains the genomic and phenotypic data used for the analysis.
        + **BRCA_HER2+_Main_summary_stages.xlsx**: Output file of BRCA_IL22_HER2+.ipynb with absolute counts of summarized pathologic cancer stages by cluster.
        + **BRCA_HER2+_Main.xlsx**: Output file of BRCA_IL22_HER2+.ipynb containing scaled genomic, phenotypic, and cluster affiliation. 
+ **Cibersortx_Analysis**: Here, you can find how we prepared gene matrices for the CIBERSORTx deconvolution tool.
    + **LUAD_CIBERSORTx.ipynb**: Notebook containing the formatting for the input file for the deconvolution and the processing of the result file for the LUAD Cohort.
    + **BRCA_CIBERSORTx.ipynb**: Notebook containing the formatting for the input file for the deconvolution and the processing of the result file for the BRCA Cohort.
    + **LUAD_all_clusters_CISO.txt**: Input file for CIBERSORTx deconvolution.
    + **BRCA_all_clusters_CISO.txt**: Input file for CIBERSORTx deconvolution.
    + **LUAD_Table_for_decon.xlsx**: Table containing cluster labels from the main cluster analysis of the LUAD cohort.
    + **BRCA_all_clusters_CISO.txt**: Table containing cluster labels from the main cluster analysis of the BRCA cohort.
    + **CIBERSORTx_Job1_Results_LUAD_all_clusters.xlsx**: CIBERSORTx results for the clustered LUAD cohort.
    + **BRCA_CIBERSORTx_Job3_Results.xlsx**: CIBERSORTx results for the clustered BRCA cohort.
    + **LUAD_LM22.tsv**: Unfiltered gene expression table based on the [LM22](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5895181/) signature matrix from the LUAD cohort.
    + **BRCA_LM22.tsv**: Unfiltered gene expression table based on the [LM22](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5895181/) signature matrix from the BRCA cohort.
    
    
+**Stage_Specific_Survival**:
+**Cohort_Info_Table**: This folder contains notebooks and tables used for creating a descriptive table of the cohorts.
+**requirements.txt**: Text file containing the python libraries and version info required for running the notebooks.

 
     
    




## TODO: anything need to be installed first?

[pip requirements file](https://pip.pypa.io/en/stable/user_guide/)

FYI: https://git-scm.com/docs/gitignore

## TODO: Write some documentation about
 - what to open first
 - what ever comes to mind
 - https://www.markdownguide.org/basic-syntax/


## How to run?

```bash
pip install -r ./requirements.txt
jupyter notebook LUAD_IL22_Clusters
```


## How to make things better?
 - Create a subfolder and put all the related files together
 - Write down a section in this README.md about this subfolder and how to run a notebook in there
 - Fix all the absolute paths to the files in the notebook to the relative ones: `r"C:\Users\jjjjo\Desktop\Phenotypic_data_LUAD.tsv -> Phenotypic_data_LUAD.tsv`
 - Add Markdown cells whenever possible, with some meaningful text: about the experiment, back-reference to the paper and whatever might help
 - Follow the rule: one cell = one output. Join cells that do not produce output, split if necessery or a Markdown Cell is needed in-between.
 - Once a notebook is proven to work correctly, add a snippet to remove future warning:
 ```python
# import warnings filter
from warnings import simplefilter
# ignore all future warnings
simplefilter(action='ignore', category=FutureWarning)
 ```

