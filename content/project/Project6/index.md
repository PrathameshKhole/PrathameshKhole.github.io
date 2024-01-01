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

In this project, my primary focus was on developing and fine-tuning a robust model backbone for a challenging machine learning task — classifying approximately 1000 images across 100 distinct classes. This task presented a unique challenge due to the limited size of the dataset, which often leads to models overfitting. To address this, I leveraged the advanced capabilities of Swin Transformers, a recent and powerful innovation in the field of deep learning, particularly known for its effectiveness in handling complex vision-based tasks.

I integrated Swin Transformers from the 'timm' library, a widely respected repository for image models in Python. My experimentation encompassed various configurations of Swin Transformers, notably 'swin_base_patch4_window7_224' and 'swin_large_patch4_window7_224'. The selection of these models was based on a strategic balance between computational efficiency and accuracy. The experimentation yielded encouraging results — the base model achieved an accuracy of over 60%, while the large model surpassed 70%. Remarkably, the Swin Transformer maintained consistent performance, peaking at an accuracy of 73.7%.

To mitigate the risk of overfitting due to the small dataset size, I adopted a balanced split approach for dataset preparation. This involved ensuring an equal representation of images from each class in both training and validation sets, thus maintaining uniformity and preventing class bias.

In tackling the optimization process, I employed both Stochastic Gradient Descent (SGD) and AdamW optimizers. Comparative testing revealed that SGD outperformed AdamW for this specific dataset. Optimal training accuracy was generally reached around the 19th or 20th epoch, beyond which the model tended to overfit, leading to a drop in accuracy. Consequently, I limited the training to 20 epochs.

The initial learning rate was set at 0.0001, accompanied by Cosine Annealing for learning rate scheduling. This approach effectively modulated the learning rate, significantly aiding the model's convergence.

A pivotal aspect of my strategy was the extensive use of data augmentation techniques to compensate for the limited dataset. I implemented methods like CutMix, MixUp, Random Erase, and Random Crop. These techniques introduced substantial variations in the training images, enhancing the model's resilience against overfitting and preparing it to handle a diverse array of visual scenarios. This comprehensive approach to model training and augmentation was instrumental in boosting the model's accuracy and its ability to generalize across various classes, despite the data constraints.