# 94887_AlzheimersDisease
Contains the codes and dataset used for the Alzheimer's Disease project.
![flowchart](https://user-images.githubusercontent.com/55336627/118058703-d06b7b00-b35c-11eb-9a70-0a5430a23227.png)

- Data pre-processing (yellow):  
Run file 1_data_cleaning.ipynb  
in: filted_adni_merge  
in: df_cleaned  
in: df_dx_imputed  
out: df_cleaned  
out: df_dx_imputed  
out: df_all_imputed  
out: df_ohe_corrected  

- EDA (red):  
Run file 2_EDA.Rmd, 3_feature_vs_feaure_eda.ipynb  
2 in: df_ohe_corrected  
2 in: adni_wind  
2 In：new_points_log_scaled  
3 in: df_all_imputed  

- Cohort selection (red):  
Run 4_label_processing.Rmd  
in: df_ohe_corrected  
in: adni_label_v6  
out: adni_label_wind  
  
- Min-max scaler and log scaler  (green):  
Run 5_data_processing.ipynb   
in: adniwind  
out: df_log _caled  

- Mean comparison (green):  
Run 6_feature_comparison_and_importance.ipynb  
in: df_log_scaled  
out: diff_sig_merged  

- Compare model results (blue):  
Run 7_Model_all4models.Rmd  
in: df_log_scaled  

- Shint app (puprle):  
Run server.R from app_randomforest final.zip  
in: new patients_.csv when prompted to upload new patient data  
