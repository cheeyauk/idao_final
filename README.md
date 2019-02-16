# idao_final
Repository for Final Submission for IDAO 2019 - Track 1 - Team Scrappy

This is the submission for Team Scrappy for track 1 of IDAO 2019 - for both evaluation and reference purposes. The solution is in a jupyter notebook file (idao_final.ipynb) that is run sequentially to obtain results. For this repo, only the final solution are provided so as to keep this minimal. The intermediate steps such as parameter tuning, grid search and validation of different models are omitted.

__Dependencies/Notes__
1. Please use the requirement.txt provided for relevant libraries (pip install -r requirement.txt). The code was run in Linux AMI on Amazon AWS platform, python 3.6.
2. Please note that the file utils.py has been changed slightly from that provided in competition for data processing purposes.
3. Please place all the relevant files on the root folder (same as ipynb file) with the same names ('train_part_1_v2.hdf', 'train_part_2_v2.hdf', 'test_private_v2_track_1.hdf') which the notebook will read from.

__Steps__
1. Data preprocessing - Deal with missing data,one-hot-encode for categorical values, label encoding
2. Feature engineering - Summation of relevant features (FOI, Matched_Hit columns,clusters and other columns), feature eng. by multiplying most important features from previous models, modified preprocessing script provided by Yandex, thresholding of sample weights to avoid dominance of high valued weights
3. Train/eval - using Xgboost with grid search to find best parameters, train for 300 iteration and evaluate with 3 % of total data
4. Test - repeat with test data



__Results__
The results achieved 7504 on the public test set.



