---
title: "Training a Neural Network on Wave Function Collapse Generation"
date: 2025-08-23
---

# ![Project Title Image](/assets/images/posts/train-on-WFC/title-image.png)

## Project Summary

This project explores the intersection of generative algorithms and machine learning by training a neural network to predict steps in the Wave Function Collapse (WFC) algorithm. WFC is a constraint-based method commonly used for procedural terrain and map generation. Here, the goal was to teach a model to anticipate the next cell to collapse and the tile to place, given the current state of a 20x20 grid.

# ![WFC Grid Example]
| ![img1](/assets/images/posts/train-on-WFC/Figure_1.png) 
  ![img2](/assets/images/posts/train-on-WFC/Figure_10.png) 
  ![img3](/assets/images/posts/train-on-WFC/Figure_20.png)


## Approach

  - Initial run: 20 grids, ~4,000 samples, batch size 32, 10 epochs, Adam optimizer, M1 MacBook Pro.
  - Second run: 1,000 grids, ~400,000 samples, batch size 128, 30 epochs, training time ~2 min/epoch.

# ![Code Snippet Example](/assets/images/posts/train-on-WFC/model.png)
# ![Code Snippet Example](/assets/images/posts/train-on-WFC/WFC.png)
# ![Code Snippet Example](/assets/images/posts/predictions.png)

## Results & Insights

Training the neural network on the WFC algorithm revealed several key findings:

- With a small dataset (20 grids, ~4,000 samples), the model learned quickly but overfit, failing to generalize to validation data.
- Increasing the dataset size (1,000 grids, ~400,000 samples) improved validation accuracy from ~45% to nearly 50%, but overfitting still occurred after about 15 epochs.
- The model was able to learn the collapse patterns, but the limited diversity and complexity of the dataset capped its performance.
- Optimizations such as increasing batch size and using Apple Silicon MPS acceleration reduced training time from 21 minutes per epoch to under 2 minutes.
- Dropout regularization helped mitigate overfitting, but the model's accuracy plateaued, indicating a need for more complex data or model changes.


## Lessons Learned

Several important lessons emerged from this project:

- The complexity and diversity of the dataset are critical for generalization. Simple or repetitive data leads to pattern learning and overfitting.
- Neural networks can learn generative algorithm steps, but their effectiveness depends on the richness of the training data.
- Regularization (dropout) and hardware optimization (MPS, batch size) are essential for efficient training and better generalization.
- The combination of generative logic and machine learning holds promise for improving procedural content generation, but requires further experimentation.


## Next Steps

To build on this work, the following steps are recommended:

- Generate and use more complex, diverse datasets to improve model generalization.
- Experiment with additional regularization techniques and alternative neural architectures.
- Explore hybrid models that combine WFC logic with neural prediction for enhanced procedural generation.
- Apply the trained model to real-world terrain or map generation tasks and evaluate its performance.
- Share results and code for community feedback and collaboration.


## Reflection

This project demonstrates both the promise and the challenges of merging generative algorithms with machine learning. While the model learned patterns in the WFC process, true generalization will require more sophisticated data and further experimentation.

*For more details, see the codebase and notebook in this repository.*
