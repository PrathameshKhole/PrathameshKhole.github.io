---
title: Image Classifcation using Transfer Learning
summary: Solved and implemented image classifcation using Transfer Learning with PyTorch and Hugging Face models
tags:
  - Deep Learning
date: "2023-12-01"

# Optional external URL for project (replaces project detail page).
# external_link: https://example.org

image:
  caption: Hugging Face Logo
  focal_point: Smart

# slides = "ORAMSlides".
# slides: example
---

In this segment of the project, I focused on developing and fine-tuning the model backbone for a machine learning task, specifically utilizing the advanced capabilities of Swin Transformers. The Swin Transformer, a recent innovation in the field of deep learning, is known for its effectiveness in handling various vision-based tasks. My work involved integrating Swin Transformers from the 'timm' library, a popular repository for image models in Python.

I experimented with different configurations of Swin Transformers, particularly 'swin_base_patch4_window7_224' and 'swin_large_patch4_window7_224'. These models differ in terms of their capacity and complexity, and my experiments aimed to find the optimal balance between accuracy and computational efficiency. The results were encouraging, with the base model achieving an accuracy of over 60%, and the large model surpassing 70%. Notably, the Swin transformer displayed consistent performance across various trials, with the highest recorded accuracy being 73.7%.

A key aspect of my approach was the use of a balanced split for dataset preparation. This method involves selecting an equal number of images from each class to create a balanced training and validation set. Such an approach ensures that all classes are equally represented during the training process, thereby preventing the model from developing a bias towards more frequently occurring classes.

In terms of optimization techniques, I employed both Stochastic Gradient Descent (SGD) and AdamW optimizers. Through comparative testing, I found that SGD yielded better results than AdamW for this particular dataset. The model's best training accuracy was typically reached around the 19th or 20th epoch. Beyond this point, the model tended to overfit, and accuracy started to decline. Therefore, I settled on training the model for 20 epochs.

The learning rate was initially set to 0.0001, with Cosine Annealing used for learning rate scheduling. This approach helped in adjusting the learning rate in a strategic manner, enhancing the model's ability to converge to an optimal solution.

Furthermore, I incorporated more intensive data augmentation techniques, including CutMix, Random Erase, and Random Rotation. These augmentations introduce a variety of alterations to the training images, making the model more robust and less prone to overfitting. They simulate a range of visual variations, thereby preparing the model to handle diverse and unforeseen image conditions in real-world scenarios. This comprehensive approach to model training and augmentation played a crucial role in enhancing the model's accuracy and generalization capabilities.