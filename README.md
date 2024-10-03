# XAI Assignment #5: Explainable Techniques

## Overview
This project implements local explanations for individual predictions made by a pre-trained ResNet18 model on the MNIST dataset using LIME (Local Interpretable Model-agnostic Explanations). The goal is to interpret how the model arrives at its predictions and to visualize what may influence these predictions. 

## Dataset Used
The dataset utilized for this project is the MNIST dataset, which consists of 70,000 handwritten digits (0-9) represented as 28x28 pixel grayscale images. For the purpose of this assignment, the images were transformed to fit the input requirements of the ResNet18 model by converting them to RGB format and resizing them to 224x224 pixels.

## Explainable Technique Used
The explainable technique I chose was LIME, which is a powerful technique for generating local explanations for individual predictions made by complex models. LIME perturbs the input image to observe how these changes affect the model's output, allowing us to highlight the most important features for the model's prediction.

## Results
The model's predictions were visualized alongside the LIME explanations. For example, when presented with a handwritten digit "7," the model predicted it as "1." The LIME explanation highlighted the areas of the image that influenced this prediction, showing how the model was likely misled by similar features between the two digits.

### Visualization
![image](https://github.com/user-attachments/assets/3fd65f79-8e02-476d-b351-1a631299c260)
*Left: Original Image (True Label: 7, Predicted Label: 1). Right: LIME Explanation highlighting influential features.*

## Strengths and Limitations

### Strengths
- **Model-Agnostic**: LIME can be applied to any black-box model, making it versatile for various architectures.
- **Local Explanations**: Provides specific insights into individual predictions, making it useful for understanding particular cases.
- **Visual Intuition**: The visual output is intuitive and helps users grasp the model's decision-making process quickly.

### Limitations
- **Computationally Expensive**: Generating LIME explanations can be slow, particularly with larger datasets or more complex models.
- **Hyperparameter Sensitivity**: The results may vary based on the choice of segmentation algorithm and the number of perturbation samples used during the explanation process.

## Improvements
- **Experiment with Segmentation Algorithms**: Explore different segmentation techniques to observe variations in the generated explanations.
- **Compare Other XAI Techniques**: Implement alternative explanation methods such as SHAP or Anchors for comparison and to gain additional insights.
- **Broader Analysis**: Analyze a more extensive range of images from the MNIST dataset to better understand the model's overall behavior.

## Conclusion
This project emphasizes the need for explainability in machine learning. Using LIME provided insights into how the ResNet18 model makes predictions, which can help identify areas for improvement and build trust in its outputs.

## Credits
Used Claude AI for documentation and code comments.
