# COVXAI

It is a deep Learning Based COVID-19 Diagnosis Using Learner-Wise Relevance Propagation

## Introduction
COVXAI is a deep learning project that aims to diagnose COVID-19 based on CT scan images using the learner-wise relevance propagation (LRP) technique. The project is built using the PyTorch framework, and the dataset used is the Sarskov CT scan dataset.


## Methodology
The dataset was split, and various transformations were added to the training dataset for increased variance. A pre-trained VGG16 model was selected from the torchvision model zoo and trained using the Adam optimizer for 60 epochs. After obtaining satisfactory results, the model was passed through the LRP layer to get a better understanding of how the model arrived at its output.

LRP is a technique that assigns relevance scores to input features, indicating how much each feature contributes to the model's output. The relevance of the output layer is propagated back through the network to the input layer using a set of rules that distribute the relevance scores based on the contribution of the input features to the activation of the output layer.

Passing some images from the test dataset through the LRP layer along with the model provided insight into how the vision model works under the hood. It revealed which parts and features of the image were most relevant when the model classified an image as COVID-19 or non-COVID-19, allowing for a better understanding of how the deep learning model makes its predictions.


## Conclusion
Overall, COVXAI is a promising project that shows the potential of deep learning and LRP in diagnosing COVID-19 using CT scan images. The insights gained from the LRP layer can be useful for feature selection, model debugging, and improving the interpretability of deep learning models in medical diagnosis applications.
