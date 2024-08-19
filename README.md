**Brain Tumor Classification (MRI)** #

Project Overview ##

This project focuses on the classification of MRI brain images into three types of cancer: glioma, meningioma, and pituitary, or identifying them as non-cancerous. The goal of this project is to assist in the early detection and diagnosis of brain tumors, potentially improving treatment outcomes and patient prognosis. Gliomas, meningiomas, and pituitary tumors are among the most common types of brain tumors, each with distinct characteristics and treatment approaches. Accurate classification is crucial for appropriate medical intervention.

Data Partitioning##

The dataset was divided into training, validation, and test sets to ensure robust model evaluation. Initially, we split the data into 20% for testing and 80% for training. Then, from the training data, we further split 20% for validation and used the remaining 80% for training the model.

Training Set: Used for training the model.
Validation Set: Used to tune hyperparameters and make decisions about the model architecture.
Test Set: Used to evaluate the final model's performance.

Model and Techniques##

We utilized a neural network with transfer learning, leveraging the DenseNet121 architecture. Transfer learning allows us to build on the knowledge from a pre-trained model, improving performance and reducing training time. Specific steps included:

1.Transfer Learning: Initialized the model with pre-trained DenseNet121 weights.
2.Additional Layers: Added a dropout layer and a dense layer.
3.Hyperparameter Tuning: Conducted a hyperparameter search specifically for the dropout rate to identify the optimal setting. The best-performing parameter was selected, and other parameters were left at their default values.
4.Fine-Tuning: Unfroze and fine-tuned the last 10 layers of the DenseNet121 network to achieve optimal results.

Performance##

The model achieved an accuracy of 0.86 on the validation set and 0.88 on the test set. These performance metrics indicate the model's effectiveness in classifying MRI brain images into the specified categories.

