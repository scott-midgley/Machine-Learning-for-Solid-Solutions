## Machine learning for solid solutions

This document provides instructions for running machine learning models downloaded from GitHub repository. 

* The necessary _conda_ environment can be imported from the file 'environment.yml'.

On Linux/MacOS
```
conda env create -f environment.yml
conda activate ml-solid-solns
```

### 1.1 Data extraction

We provide the raw data (i.e. DFT outputs) with notebooks for pre-processing them. This pre-processing can take some time so we also provide pre-processed data sets ready to be used with the different fitting procedures.

#### These instructions are for extracting vasp energies and Coulomb matrix, prior to machine learning. 

It is assumed that the default directory structure, as downloaded from the repository, remains in place. 

* 'repository-data.zip' should be downloaded from Zenodo (https://doi.org/10.5281/zenodo.4736810) and unzippled in the top level of this repo.
* You can use pre-generated files if you wish, this is found in `repository-data/coulomb_matrix/input_data_cme.pkl`
* If you want to do your own pre-processing;  `data.ipynb` notebook can be found in `coulomb_matrix/data/rundir/` this can be used to generate the file required. 

#### These instructions are for extracting vasp energies and cluster correlation functions, prior to machine learning. 

* 'repository-data.zip' should be downloaded from Zenodo (URL: ) and unzippled in the top level of this repo.
* You can use pre-generated files if you wish, this is found in `repository-data/cluster_correlation_functions/input_data_ccf.pkl`
* If you wan to do your own pre-processing;  `data-ccf.ipynb` notebook can be found in `cluster_correlation_functions/data/rundir/` this can be used to generate the file required. 

### 1.2. Machine learning
Machine learning notebooks ('mlp.ipynb', 'gbdt.ipynb', 'lr-emix.ipynb' and 'lr-egap.ipynb') can be found in sub-directories.

* N.B. Users should specify the desired percentage of data to be used for training, by manually editing the second cell of the notebook, 
  prior to training the model. 
* There are various parts of the code which may be edited by users, however the two main user inputs are located in the first two cells
  of each notebook. 
