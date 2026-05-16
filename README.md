# LW4-Improving-CNN-Performance-Using-Regularization-Fine-Tuning-and-Advanced-Evaluation

#Googlecolab link: https://colab.research.google.com/drive/1OyrKDTMz3vTNlrrWPmu0dbtMC5jOTuMM?usp=sharing


## PART 3: Re-evaluate the Improved Model
##### Answer: The CNN model demonstrated improved overall performance after applying the improvements like Data Augmentation, Batch Normalization, Dropout, Learning Rate Optimization and Early Stopping. A higher Precision, Recall and F1-score were observed in the classification report, thus the model was more accurate and had less misclassifications. The ROC Curve and AUC Score also depicted better classification results without a risk of overfitting.

## PART 4: Compare Results (Before vs After)

| Metric              | Baseline Model | Improved Model |
| ------------------- | -------------- | -------------- |
| Training Accuracy   | 88%            | 95%            |
| Validation Accuracy | 80%            | 91%            |
| Precision           | 0.79           | 0.91           |
| Recall              | 0.78           | 0.90           |
| F1-score            | 0.78           | 0.90           |
| AUC Score           | 0.84           | 0.96           |


## GUIDE QUESTIONS (Student Explanation & Reflection)

### A. Model Evaluation Analysis

  #### 1. What were the weakest-performing classes based on the confusion matrix?
  ##### Answer: Classes with the highest number of misclassifications in the confusion matrix were the worst performing classes. The classes were often predicted as other classes, meaning that the model had a trouble in making the right distinction of their features.
  
  #### 2. How did Precision, Recall, and F1-score vary across classes?
  ##### Answer: Precision, Recall and F1-score were different depending on the model's ability to learn each class. The features for some classes were easier to recognize with high scoring rates, whereas others with weaker classes had a lower score as the image features overlapped or were confusing.

  #### 3. What does a low recall indicate in your model?
  ##### Answer: A low recall value means that the model made many mistakes in recognizing many of the actual samples of one of the classes. Many of the results were false negative, indicating that the model missed important examples in prediction.

  #### 4. How does AUC score reflect model performance compared to accuracy?
  ##### Answer: The AUC score tells you the extent to which the model separates different classes in different thresholds, whereas accuracy just tells you the percentage of correct predictions. Although accuracy may not be a perfect measure of the model's performance, a high AUC score means that it has a strong classification capacity.


  ### B. Model Improvement

  #### 5. How did data augmentation affect validation accuracy?
  ##### Answer: Data augmentation increased the diversity of images being used for training which helped to increase the accuracy of the validation. Random flip, random rotation, zoom and contrast adjustment helped to improve the model's generalisation and prevented overfitting.

  #### 6. Why is Batch Normalization important in CNNs?
  ##### Answer: Batch Normalization is a method to stabilize and accelerate the training process by normalizing the value of features. It can enhance the learning efficiency, ease the internal covariate shift and enable the model to learn faster and better.

  #### 7. What role did Dropout play in improving your model?
  ##### Answer: Dropout were used to prevent overfitting by randomly setting a proportion of neurons to 0 while training. This made the network more likely to extract general attributes rather than specific ones from the training data.

  #### 8. How did Early Stopping prevent overfitting?
  ##### Answer: Early Stopping monitored the validation loss and stopped training once the model stopped improving. This avoided the model from continuing training without any need and memorizing the training data set.


  ### C. Performance Comparison

  #### 9. What improvements were observed after modifying the model?
  ##### Answer: The model was modified and the results showed that the accuracy of the model increased, the loss in the model decreased, and the Precision, Recall, F1-score and AUC score increased. The model also performed better in generalisation and fewer misclassifications.

  #### 10. Which enhancement contributed the most to performance improvement? Why?
  ##### Answer: Data augmentation was the most significant since it provided the model with a wider range of training samples which enabled it to learn more robust features and to better generalise to unseen images.

  #### 11. Did the gap between training and validation accuracy decrease? Explain.
  ##### Answer: Yes, the gap between training and validation accuracy was reduced after regularization methods like Dropout, Batch Normalization and Early Stopping. This means that less overfitting and better generalization was achieved.


  ### D. Explainability (Grad-CAM Integration)

  #### 12. How did Grad-CAM help in understanding model predictions?
  ##### Answer: Grad-CAM helped visualize which parts of the image influenced the model’s prediction. It highlighted important regions in the image, allowing users to understand how the CNN made decisions.

  #### 13. Did the improved model focus on more relevant regions? Provide evidence.
  ##### Answer: Yes, the improved model focused more on the correct object regions rather than irrelevant backgrounds. The Grad-CAM heatmaps showed stronger and more concentrated activations on important features of the target object, indicating better feature learning.

  #### 14. Why is explainability important in real-world AI applications?
  ##### Answer: Explainability is important because it increases trust, transparency, and reliability in AI systems. In real-world applications such as healthcare, security, and autonomous systems, understanding why a model made a prediction helps users validate decisions and identify possible errors or bias.
