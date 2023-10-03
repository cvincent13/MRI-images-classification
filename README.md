# MRI images classification
Cardiac pathology prediction from MRI scans challenge

# Project description

The goal of the challenge is to successfully classify MRI images of the heart into 5 possible diagnostics: 
'0' - Healthy control, '1' - Myocardial infarction, '2' - Dilated cardiomyopathy, '3' - Hypertrophic cardiomyopathy, '4' - Abnormal right ventricle. 
We have the training set true classes in order to train our model.

The available data is composed of 150 patient MRI scans, 100 for the training set and 50 for the test
set. Each scan contains two 3D images, at end diastole (ED) and at end systole (ES), represented as
multiple 2D slices. Each slice has a corresponding segmentation for the Left and Right ventricle
cavities (LV and RV) and the Myocardium. In the test set, the Left ventricle cavity segmentation is
missing. Patients’ height and weight are also available.

The MRI scans are stored as NIfTI files, which we open using the nibabel python library. Patients' heigth and weight are stored in the metadata csv file, along with the target classes.

Several features are extracted from the provided segentations of the MRI scans, such as volumes and ejection fractions. Classification is then performed with several classifiers from the scikit-learn library, 
and the final results are obtained after hyperparameters optimization and model selection. 

Full details can be found in the pdf report.
