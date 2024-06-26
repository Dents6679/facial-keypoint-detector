# Facial Landmark Detection using Ridge Regression

This repository contains code for detecting 44 facial landmarks in images using a Ridge Regression model.

The code for this project can be found in `face_keypoint_detector.ipynb`.
The report for this project can be found in `face_keypoints.pdf`.

### Methodology

1. **Data Pre-processing**:
   - **Resizing**: Tested various image sizes, found 256x256 was optimal.
   - **Greyscaling**: Simplifies data by removing color information.
   - **Histogram Equalisation**: Enhances edge contrast.
   - **Gaussian Blurring**: Applied with a 5-pixel kernel for noise reduction.

2. **HOG Gradient Detection**:
   - Used to convert images into histograms of gradients.
   - Optimal parameters: 32x32 cell size with 12 gradient orientations.

3. **Ridge Regression**:
   - Chosen for its regularisation to reduce overfitting.
   - Optimal alpha value found to be 10.

4. **Alternative Approach**:
   - Predicts 5 subset landmarks first, then the remaining 44 from those 5.

### Results

- **Standard Detector**: Mean Euclidean distance of 5.88 pixels between ground truth and predicted values.
- **Alternative Detector**: Mean Euclidean distance of 5.96 pixels between ground truth and predicted values.

### Conclusion

The standard detector, despite its simplicity, effectively identifies facial features on unseen data. Improvements could involve using more advanced optimisation techniques and addressing specific prediction errors.
