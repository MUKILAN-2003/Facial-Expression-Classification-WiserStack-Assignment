# Facial-Expression-Classification-WiserStack-Assignment

## Approach 1: CNN Model for Image Classification
This approach uses a Convolutional Neural Network (CNN) to directly classify facial expressions from grayscale images, leveraging the spatial hierarchies in the image data to learn features and predict the expression.

## Approach 2: Dual Input Model Combining Images and Facial Landmarks
This approach integrates both image data and facial landmarks as inputs, combining the CNN for image processing with an additional network to handle landmark data, aiming to improve expression recognition by leveraging geometric information about facial features.

![image](https://github.com/user-attachments/assets/4e37f49c-9404-4f5b-a507-3e83f11bbd4e)

# Evaluation and Metric on Test Data

| Metric                     | Approach 1: CNN Model for Image Classification | Approach 2: Dual Input Model (Images + Landmarks) |
|----------------------------|-----------------------------------------------|--------------------------------------------------|
| **Accuracy**               | 57.1%                                         | 45.4%                                            |
| **Precision**              | 17.0%                                         | 45.0%                                            |
| **Recall**                 | 10.0%                                         | 45.0%                                            |
| **F1 Score**               | 11.0%                                         | 43.0%                                            |
| **Confusion Matrix**       | ![image](https://github.com/user-attachments/assets/585573d6-af6c-4b5d-963c-faef0310e634) | ![image](https://github.com/user-attachments/assets/98263320-7eb5-4f64-bd8e-79f8e45c1925) |
| **Classification Report**  | ![image](https://github.com/user-attachments/assets/1321b655-8bdc-47dc-baf0-a9242331fa0a) | ![image](https://github.com/user-attachments/assets/9e465788-08e5-4624-9217-a9751da1f824) |
| **Loss (categorical_crossentropy)**                   | 1.15                                          | 1.46                                             |

## System Environment Settings

- **Python Version**: 3.10.14
- **TensorFlow Version**: 2.10.1
- **CUDA Toolkit**: 11.2
- **cuDNN**: 8.1.0
- **mediapipe** : 0.10.14
- **numpy**: 1.24.3

## Fine-Tuning with Keras Tuner
To optimize the hyperparameters used Keras Tuner to find the optimal parameters for model(weight) converge.

# Conclusion
The dual input model that combines images and facial landmarks outperforms the CNN model that uses only image data across all metrics, demonstrating the added value of incorporating geometric information about facial features.
