# Breast-cancer-detection-using-image-processing-techniques
Breast cancer is one of the frequent diagnosis diseases among women. It can be detected by clinical breast examination, yet the detection rate endures to be very low. Additionally, the abnormal areas that cannot be felt can be quite challenging to check using traditional techniques but can be easily seen on a conventional mammogram or with ultrasound. Mammography is currently the best method for detecting breast cancer at its early stage. The problem with mammography images are they are complex. Thus, image processing and features extraction techniques are used to assist radiologist for detecting tumor. Features extracted from suspicious regions in mammography images can help doctors to discover the existence of the tumor at real time thus speeding up treatment process. Detecting breast cancer can be quite a challenging job. Specially, as cancer is not a single disease but is a collection of multiple diseases. Depending on only one technique or one algorithm to detect breast cancer may not provide us with the best possible result. As one cancer differ from another, similarly every breast appears differently from another. The mammography image can also be compromised if the patient has undergone some breast surgery.
In this project, I developed a deep learning model using image processing techniques to accurately detect breast cancer and predict its stage. The workflow included key stages such as image preprocessing, segmentation, feature extraction, classification, and detection.
1. Image Preprocessing
  - Enhanced mammogram images by applying grayscale conversion and Gaussian filtering to reduce noise and improve image clarity, making feature extraction more effective.
2.Segmentation
  - Applied thresholding and region-based segmentation to isolate regions of interest (ROIs) that could potentially represent cancerous tissues, allowing the model to focus on relevant areas of the mammogram.
3.Feature Extraction
  - Used Convolutional Neural Networks (CNN) to automatically extract critical features such as texture, shape, and edge patterns from the segmented regions, differentiating between normal and abnormal tissues.
4. Classification
  - Implemented a CNN-based model to classify the extracted features into cancerous and non-cancerous categories.
5.Detection
  - The model further predicted the stage of the cancer, ranging from stage 0 (early detection) to stage 4 (advanced cancer), based on the features extracted from the mammogram.
  - This detection allowed for precise identification of the cancer’s progression, helping clinicians assess the stage and tailor treatment accordingly.
  - Breast cancer stages to be predicted :
Breast cancer stages, along with their names, are as follows:
Stage 0: Carcinoma in situ also known as ductal carcinoma in situ (DCIS), where abnormal cells are confined to the milk ducts and have not invaded surrounding breast tissue.
Stage I: Early-stage breast cancer. Cancer is small and confined to the breast tissue, with no spread to lymph nodes or distant sites.
Stage II: Locally advanced breast cancer. Cancer may be larger and may involve lymph nodes in the armpit, but hasn’t spread to distant sites.
Stage III: Locally advanced breast cancer . Cancer is larger and may have spread to multiple lymph nodes or nearby tissues, but hasn’t spread to distant sites.
Stage IV: Metastatic breast cancer . Cancer has spread beyond the breast and nearby lymph nodes to distant organs like bones, lungs, liver, or brain.

In this study, the mammography images are used for Image processing techniques. The model worked under VGG-16 CNN Deep Learning. Here the Convolutional neural network for the Image propagation and For dataset we used Machine learning classification supervised algorithms such as Decision tree, Random forest, Support vector machine, Logistic regression and in our model Random forest has the highest Efficiency up to 93%. The proposed model has the Accuracy of 91%. The best outcomes were the feature extraction, Mapping of tumor location, classification task, Finding the performance measures and Predicting the breast cancer stages.
