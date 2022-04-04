# TCGA_clustering

## TODO: anything need to be installed first?

[pip requirements file](https://pip.pypa.io/en/stable/user_guide/)

FYI: https://git-scm.com/docs/gitignore

## TODO: Write some documentation about
 - what to open first
 - what ever comes to mind
 - https://www.markdownguide.org/basic-syntax/

Subfolders for every analisys?




# 01_LUAD_IL22_Clusters-name-me-better-please

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

