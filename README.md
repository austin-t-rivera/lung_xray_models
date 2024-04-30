# lung_xray_models

The following Jupyter Notebooks contain the code used to develop the various models architectures that we evaluated and compared to detect lung disease from chest X-Ray images:

## Preprocessing Lung X-Ray Images
#### Image_Preprocessing
Processes large amounts of X-Ray images by resizing, converting to gray scale, and normalizing brightness. Data is sampled to be balanced, in that it samples same number of images for each class, using the class with the least amount of images to be the limiting factor. Data is then split into train, validation, and test sets (80/10/10) and saved alongside the original images' respective labels into .pickle or .pkl files.

#### Image_Preprocessing_Unbalanced
Identical to the Image_Processing notebook, except that the max number of images for each given set are used, rather than setting a limiting factor for balance.

## Building Models
#### Ensemble_Model
Balanced preprocessed data is loaded into the notebook, models are established, fine-tuned, and fit until they were able to perform with over 90% validation and test accuracy for their specific classification. The ensemble consists of a larger binary CNN that determines if a lung X-Ray image is healthy or unhealthy. Three additional models were created, one for each disease of interest (Pneumonia, Covid, Tuberculosis), where they were trained on healhty and unhealthy data from their respective disease datasets.

## Unbalanced_Ensemble_Model
Identical to the Ensemble_Model notebook, except the unbalanced data is loaded in and used.

## Dual_Model
Balanced preprocessed data is loaded into the notebook, models are established, fine-tuned, and fit until they were able to perform with over 90% validation and test accuracy for their specific classification. The dual model consists of a larger binary CNN that determines if a lung X-Ray image is healthy or unhealthy. One additional three-class CNN was created to differentiate unhealthy lung images into the three diseases.

## Unbalanced_Dual_Model
Identical to the Dual_Model notebook, except the unbalanced data is loaded in and used.

## Four_Class_Model
Balanced preprocessed data is loaded into the notebook, models are established, fine-tuned, and fit until they were able to perform with over 90% validation and test accuracy for their specific classification. The four-class model consists of one large CNN that determines if a lung X-Ray images has pneumonia, covid, tuberculosis, or is healthy.

## Unbalanced_Four_Class_Model
Identical to the Four_Class_Model notebook, except the unbalanced data is loaded in and used.

## Analysis




