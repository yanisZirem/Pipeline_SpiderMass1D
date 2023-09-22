# Pipeline_SpiderMass1D

This Python script written in jupyter notebook performs analysis on mass spectrometry data. It includes various functions for data preprocessing, machine learning model selection, visualization, peak picking, and statistical analysis of significant features.

## Functions and Usages

1. **import_data(data_file):**
    - Imports data from a CSV file.

2. **process_data(data_file):**
    - Performs data preprocessing.
    - Splits the data into features (X) and target (y).
  
3. **plot_mean_spectra(data_file):**
    - Display mean spectra of eacu class
    
4. **lazy_predict(X_train, y_train, X_test, y_test):**
    - Performs lazy prediction on the dataset using various machine learning models.
    - Returns a summary of model performance.

5. **find_and_build_best_model(models, X_train, y_train):**
    - Finds the best machine learning model based on Lazy Predict results.
    - Builds and returns the best model as a pipeline.

6. **confusion_matrix_scores_classification_report(pipeline, X_test, y_test):**
    - Displays scores, confusion matrix, and classification report for a given model.

7. **cross_validate_and_report(pipeline, X, y):**
    - Performs K-fold cross-validation for the model.
    - Displays cross-validation scores, classification report, and confusion matrix.

8. **eli5_feature_importance(pipeline, X_train, top_features=40):**
    - Shows feature importances using Eli5 for one sample in the train set.
    - Returns a summary of feature contributions.

9. **save_contributions(csv_name, pipeline, X_train):**
    - Saves feature contributions in CSV format for all samples in the train set.
  
10. **plot_pca(data, num_components=2,custom_colors=custom_colors) :**
    - plot_pca: Performs Principal Component Analysis (PCA) and creates scatter plots for visualizing data in reduced dimensions.

11. **peak_picking(ms_data, min_sn=10):**
    - Performs peak picking on mass spectrometry data using Signal-to-Noise ratio.
    - Returns a DataFrame with picked peaks.

12. **create_heatmap(data):**
    - Creates a heatmap based on the data, clustering by class.

13. **significant_features(data, alpha=0.05):**
    - Conducts statistical analysis to find significant features.
    - Returns a list of significant feature columns.

14. **boxplot_significant_features(data, mz_values, class_colors=None, test='Kruskal'):**
    - Creates box plots for significant features.
    - Displays statistical annotations.

15. **violin_significant_features(data, mz_values, class_colors=None, test='Kruskal'):**
    - Creates violin plots for significant features.
    - Displays statistical annotations.
    - 
16. **one_box_plot(data, mz, test='Kruskal', class_colors=None):**
    - Creates box plots for one mz feature.
    - Displays statistical annotations.

17. **violin_box_plot(data, mz, test='Kruskal', class_colors=None):**
    - Creates violin plots for one mz feature.
    - Displays statistical annotations.
## Usage

1. Update the `data_file` variable in the script with the path to your mass spectrometry data file.

2. Run the script using a Python interpreter
