## Machine learning for solid solutions

This document provides instructions for running machine learning models downloaded from GitHub repository. 

1. Machine learning with Coulomb matrix

- The necessary Anaconda environment can be imported from the file 'environmnet.yml'.

- Before running the any notebook, users should paste the full system path for the repository directory into the first cell of the notebook.

- Before running machine learning models, users may specify the percentage of the data to be used for training, by commenting/uncommenting 
  the second cell of the notebook as necessary. 

- Other alterations may be made to notebooks to manipulate the names of results files etc.

- The following instructions describe the recommended workflow of data extraction and preprocessing, followed by ML training.

### 1.1 Data exraction

- These instructions are for extracting vasp energies and CME's, prior to machine learning. 

- It is assumed that the default directory structure, as downloaded from the repository, remains in place. 

- 'repository-data.zip' should be downloaded from Zenodo (URL: ) and unzippled in the top level of this repo.

- The 'vasp-energies.csv' data file should be placed inside 'datadir'. The 'structure_files' directory should also be placed inside 'datadir'.
  Such that 'repository\coulomb_matrix\data\datadir\vasp-energies.csv', and 'repository\coulomb_matrix\data\datadir\structure_files\<POSCAR FILES>'.

- The 'data.ipynb' notebook should be launched and run from within 'rundir', where outputs will also be saved. 

### 1.2. Machine learning

- Machine learning notebooks ('mlp.ipynb', 'gbdt.ipynb', 'lr-emix.ipynb' and 'lr-egap.ipynb') should be launched from their
  respective directories. 

- N.B. Users should specify the desired percentage of data to be used for training, by manually editing the second cell of the notebook, 
  prior to training the model. 

- There are various parts of the code which may be edited by users, however the two main user inputs are located in the first two cells
  of each notebook. 

- Results will be printed as a .xlsx file in the relevant directory. 

