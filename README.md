# Book_recomender_system

A recomender sytem to predict user's reading interest by using content-base, KNN, and Matrix Factorization
Quick Guide

Almost libraries is already installed by Google Colab. Else if you run this on your local, please run "pip install -r requirements.txt"

Data:

     train1.csv: training set
     
     test1.csv: test set
     
     userid.json: A dictionary stores user's id and and their order
     
     bookid.json: A dictionary stores book's id and and their order
     
     mean_ratings.json: An array stores user's mean ratings.
     
     similarity_matrix.h5: similarity matrix for KNN
     
     normalize_matrix_MF.csv: normalize data for MF
     
     normalize_sparse_matrix.npz: normalize data for KNN
     
     MF_final_parameter_X_W_b_d_version2.npz: checkpoint for MF(W, X, b, d)
     
     Sai_so2.npz: RMSE_train, RMSE_test, loss on 100 epochs
     
===========================================================================

KNN: 

Notebook: KNN.ipynb

To training: 

      Run normalize_Y() and similarity().
      
      Then we will save the 2 matrices to the file for convenient inference.
      
To evaluate:

      Run cell in notebook: Evaluate on test set
      
To infer:

      Run print_recommendation_for_1_user() with input parameter is specific user's id.
      
=======================================================================================

Matrix Factorization:

Notebook: MatrixFactorization.ipynb

To training: 

      Run normalize_Y() and fit().
      
      Then we will save the checkpoint to the file for convenient inference.

To evaluate:

      Run evaluate_RMSE() with input is Y_data_test.
      
 To infer:
 
      Run pred_for_user() with input parameter is specific user's id.
