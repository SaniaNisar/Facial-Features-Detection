# 👁️‍🗨️ Facial Feature Detection
It detects facial attributes from an image (uploaded or captured), specifically:
- 👩‍🦰 Gender Detection  
- 👓 Glasses Detection  
- 👕 Shirt Color Detection

### The dataset:
https://www.kaggle.com/datasets/jangedoo/utkface-new/data

The UTKFace dataset is well-suited for your facial feature detection task, as it contains over 20,000 images labeled with age, gender, and ethnicity, which satisfies the requirements for:
- 1000+ face images
- Balanced gender
- Racial diversity

### Step 1: Data Collection - TASK 1.ipynb
Face datasets from:
- #### Kaggle:
    - UTKFace – labeled with age, gender, ethnicity.
    - Downsampling for removing biasness on race and gender
1) Download the dataset from the above mentioned link or use the script in the TASK 1.ipynb, once downloaded, use From the Kaggle version of UTKFace, the folder you want is:
`
datasets/UTKFace/utkface_aligned_cropped/
`
This folder contains all the .jpg images with names like 25_0_2_20170116174525125.jpg.chip.jpg.
I will be using this folder for the images.
2) Run the script TASK 1.ipynb to print stats and plot the distribution. Next, it includes the downsampling to remove biasness.
3) Saving the cleaned metadata to 'balanced_utkface_metadata.csv'

### Step 2: Data Preprocessing - genderClassifier.ipynb and shirtColorClassifier.ipynb
1) Face Detection using OpenCV 
2) Shirt Color Detection:
   - Crop below face → extract shirt region
   - Use dominant color detection via KMeans or color histogram
