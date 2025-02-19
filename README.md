Animal Classification Project

This project involves building and training a CNN model to classify images of 10 different animals. The final model achieves 92% accuracy on the training set and 86% on the validation set. Due to hardware limitations, training was stopped early, but with 100 epochs, the model is expected to reach around 90% validation accuracy.

Dataset: 
The dataset, sourced from Kaggle, contains 26,000 images. The training process is outlined in the accompanying Jupyter Notebook, detailing data preprocessing, augmentation, and model development.

Model Development:
Initially, a simpler CNN ("old_model") was built with:
- Three Conv2D layers, each followed by pooling layers
- Flatten layer → Dense (512 neurons, ReLU)
- Dropout (0.5) → Output layer (10 neurons, Softmax)

As the model plateaued, an improved "new_model" was introduced with an additional 256-feature map layer, while retaining the previous convolutional and dense layers. This transfer allowed training continuity without restarting from scratch.

Training Strategy:
- Data augmentation & Dropout (to prevent overfitting)
- AUTOTUNE optimization for efficient hardware utilization
- Tuned learning rate instead of reducing dropout to avoid stagnation

Lessons Learned:

This project highlighted the resource-intensive nature of deep learning. While large datasets improve accuracy, computational power is a major factor. Future improvements could include increasing pooling sizes (e.g., 3×3, 5×5) and leveraging cloud computing for extended training.

Unfortunately, I cannot upload the weights of the model as they are a bit large so I uploaded them on Google Drive with the following link: https://drive.google.com/drive/folders/1tx3YwSp7AFlWOtUHOo5g63kl_RLDKZ8o?usp=sharing
