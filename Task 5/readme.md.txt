Multimodal Housing Price Prediction Report
1. Objective of the Task

The objective of this task was to develop a multimodal machine learning model that can predict housing prices using both:

Tabular data (features like number of bedrooms, bathrooms, square footage, etc.)

Image data (photos of the houses).

By combining structured data with visual information, the model aims to capture both numerical and aesthetic aspects of housing, leading to more accurate price predictions.

2. Methodology / Approach

Dataset Used:

A CSV file containing house features (bedrooms, bathrooms, sqft, price, etc.).

A folder of corresponding house images.

Steps Performed:

Data Preprocessing:

Loaded and cleaned tabular data.

Scaled numerical features.

Prepared images by resizing and normalizing them.

Model Architecture:

CNN (Convolutional Neural Network): Used for extracting features from images.

Dense Network: Used for processing tabular features.

Fusion Layer: Combined both image features and tabular features.

Output Layer: A regression head predicting housing price.

Training & Evaluation:

Trained for 10 epochs using MSE (Mean Squared Error) as the loss function.

Evaluated performance with MAE (Mean Absolute Error) and RMSE (Root Mean Squared Error).

Split dataset into training, validation, and test sets.

3. Key Results or Observations

Training Process:

The model showed a steady decline in training and validation errors.

Validation MAE improved from ~755K → ~649K across epochs.

Final Performance (Test Set):

MAE: ~649,858

RMSE: ~888,573

Observations:

The model was able to learn meaningful patterns from both images and tabular data.

However, prediction errors are still very high (in the range of ~$650K).

Likely reasons:

Small dataset size.

Limited model complexity (simple CNN instead of pre-trained models).

Large variability in housing prices not captured fully by current features.

4. Conclusion

This project demonstrated the potential of multimodal machine learning by combining image and tabular data for housing price prediction. While the model successfully reduced errors during training, the final prediction error remains high, making it unsuitable for real-world deployment in its current form.

For future improvement:

Use pre-trained CNNs (ResNet, EfficientNet) for stronger image features.

Apply log transformation to housing prices to stabilize variance.

Add more features (e.g., location, neighborhood statistics).

Train on a larger dataset with diverse housing markets.

Despite the limitations, this task successfully highlights the importance of feature fusion in multimodal ML and provides a strong foundation for more advanced real estate price prediction models.