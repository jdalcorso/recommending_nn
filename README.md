## NN-based model for recommending system on implicit feedback dataset

In this small repository we have a report and some notebooks about a comparison between two NN-based recommending systems and the neighborhood-based collaborative filtering, applied on an implicit feedback dataset.

Notebooks has been used to obtain the results in the report, in particular
- `MLP` consists in data preprocessing, creation, training and testing of NN-based models which are namely Multi-Layer Perceptron (MLP) and Generalized Matrix Factorization (GMF)
- `CF_implicit` consists in data preprocessing, creation, training and testing for neighborhood-based Collaborative Filtering (CF)
- `DataVisualization` shows the results and allows to create plots that has been used in the report

In order to create, train and test a model, just run the notebooks, paying attention to:
- Remember to copy the dataset `ratings_1m.dat` in the folder you wish to use notebooks
- In `MLP`  notebook the boolean variable `GMF` switches whether or not to create a GMF or an MLP (the latter corresponds to `GMF=False`)
- Remember to copy `MLP_architecture.txt` in the folder you wish to use `MLP` notebook. That text file should contain a string like "x,y,z" where the letters are numbers representing the dimension of each layer of the MLP. More than three numbers (layers) are possible but has not been tested yet.
- `MLP_architecture.txt` while using `GMF=False` only cares about the first number of the string which represents the dimension of the embedding vectors of the GMF model
- Using `CF_implicit` you can switch from `ItemItemRecommender` to `CosineRecommender`to change the similarity metric used. Just delete and replace the function as you wish.
- Using `CF_implicit` you can also modify the parameter in `ItemItemRecommender` or `CosineRecommender`representing the number of neighbors
- Other interesting parameters that could be changed are the number of epochs and batch size in `MLP`

More instructions and information can be found in the notebooks.

For an analysis of setup, metrics and results refer to the `report`