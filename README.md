# Thyroidiomics: An Automated Pipeline for Segmentation and Classification of Thyroid Pathologies from Scintigraphy Images


## Introduction
This codebase is related to our submission to EUVIP 2024:<br>
> Anonymous authors, _Thyroidiomics: An Automated Pipeline for Segmentation and Classification of Thyroid Pathologies from Scintigraphy Images_.

<p align="justify">
The objective of this study was to develop an automated pipeline that enhances thyroid disease classification using thyroid scintigraphy images, aiming to decrease assessment time and increase diagnostic accuracy. Anterior thyroid scintigraphy images from 2,643 patients were collected and categorized into diffuse goiter (DG), multinodal goiter (MNG), and thyroiditis (TH) based on clinical reports, and then segmented by an expert. A Residual UNet (ResUNet) model was trained to perform auto-segmentation. Radiomics features were extracted from both physician's (scenario 1) and ResUNet segmentations (scenario 2), followed by omitting highly correlated features using Spearman's correlation, and feature selection using Recursive Feature Elimination (RFE) with eXtreme Gradient Boosting (XGBoost) as the core. All models were trained under leave-one-center-out cross-validation (LOCOCV) scheme, where nine instances of algorithms was iteratively trained and validated on data from eight centers and tested on the ninth for both scenarios separately. Segmentation performance was assessed using the Dice similarity coefficient (DSC), while classification performance was assessed using metrics such as precision, recall, F1-score, accuracy, area under the Receiver Operating Characteristic (ROC AUC), and area under the precision-recall curve (PRC AUC). ResUNet obtained DSC values of 0.84±0.03, 0.71±0.06, and 0.86±0.02 for MNG, TH, and DG, respectively. Classification in scenario 1 achieved an accuracy of 0.76±0.04 and a ROC AUC of 0.92±0.02 while in scenario 2, classification yielded an accuracy of 0.74±0.05 and a ROC AUC of 0.90±0.02. The automated pipeline demonstrated comparable performance to physician segmentations on several classification metrics across different classes, effectively reducing assessment time while maintaining high diagnostic accuracy.
</p>
