---
title: "Improving an Image Classifier: Regularization, Learning Rates, and Optimizer Tuning"
date: 2025-07-27
---

This project presents a progressive deep learning experiment conducted using the MNIST digit classification dataset. The objective was to design a basic multi-layer perceptron (MLP) architecture and improve its generalization performance across several stages. Using a structured experimental framework, we introduced regularization techniques, learning rate adjustments, and optimizer comparisons to evaluate their impact on model accuracy and validation loss. All visualizations and experiments were conducted in Python using TensorFlow and Keras, and the results were recorded for reproducibility and interpretation.

## Initial Model

We began with a baseline multi-layer perceptron (MLP) model consisting of fully connected layers and ReLU activations. The model had a total of 196,895 trainable parameters and used the Adam optimizer. Training was conducted over 10 epochs, and validation loss was monitored to detect signs of overfitting. The best performance was observed after epoch 6, where the validation loss reached a minimum of 0.0788. After this point, the model began to memorize the training data, and performance on the validation set deteriorated. This experiment highlighted the need for regularization techniques to extend the model’s generalization window.

An example plot of the validation and training loss over time for this model is shown below.

![Initial Model](/assets/images/posts/model-iteration/initial-model.png)


## Adding Dropout Layers

To address the overfitting observed in the initial model, we introduced dropout layers into the architecture. Dropout randomly disables a fraction of the neurons during training, forcing the network to learn redundant and distributed representations. All other hyperparameters and architectural choices were kept constant to isolate the effect of this change. The modified model achieved its best validation loss at epoch 8, recording a value of 0.0700. This indicates that dropout successfully delayed the onset of overfitting and allowed the model to train effectively for a longer duration.

The training and validation loss plots for this model reflect this delayed overfitting behavior.

![Dropout Model](/assets/images/posts/model-iteration/drop-out.png)

## Learning Rate Tuning

In the next stage of experimentation, we explored how the learning rate affects model training dynamics. While the optimizer and network structure remained the same as in the previous model, we experimented with several learning rate values: 0.01, 0.001, 0.0001, and 0.00001. A smaller learning rate often helps in fine-tuning weight updates and avoiding overshooting local minima. The model trained with a learning rate of 0.001 demonstrated the best generalization performance, with the highest accuracy achieved around epoch 10. This experiment reinforced the importance of learning rate selection in training deep networks.

The figure below compares the loss curves across the different learning rate configurations.

![Learning Rate Comparison](/assets/images/posts/model-iteration/learning-rate.png)

## Optimizer Experiments

In the final phase of the project, we evaluated the impact of different optimizers on model performance. While Adam had been our default choice throughout previous experiments, we now included comparisons with SGD with momentum, RMSprop, and NADAM. Each optimizer was used to train a fresh instance of the model with identical architecture and hyperparameters. While both SGD and RMSprop performed worse than Adam on our validation metrics, NADAM emerged as the most effective optimizer, achieving the best overall performance in terms of validation loss and accuracy.

The chart below summarizes the differences between optimizers.

![Optimizer Comparison](/assets/images/posts/model-iteration/optimizer-comp.png)

## Notebook and Source Code

The full implementation, including training loops, visualization code, and experimental details, can be found in the accompanying Jupyter notebook. It is available in the GitHub repository linked below. Readers are encouraged to review the notebook for further technical insight and reproducibility.

[View the GitHub Repository](https://github.com/MylesTym/model_iteration)

## Summary

The table below provides a consolidated view of the best results from each configuration tested throughout the project. It demonstrates how each experimental adjustment contributed to improving model generalization and mitigating overfitting.

| Configuration                        | Best Val Loss | Notes                        |
|-------------------------------------|----------------|------------------------------|
| Initial Model                       | 0.0788         | Overfitting after epoch 6    |
| + Dropout                           | 0.0700         | Delayed overfitting          |
| + Dropout + LR Tuning               | Improved       | Best at LR = 0.001, epoch 10 |
| Final (NADAM Optimizer)             | Best Overall   | Outperformed Adam baseline   |

This project represents a clear and structured investigation into improving neural network performance through a series of controlled experiments. It demonstrates not only the technical ability to implement and train deep learning models but also the analytical rigor to iterate, measure, and interpret performance in a meaningful way. The process reflects the core strengths expected of a data science graduate—critical thinking, reproducibility, and a results-driven mindset.
