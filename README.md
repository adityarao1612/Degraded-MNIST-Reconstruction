# Degraded-MNIST-Reconstruction
reconstruction of degraded mnist numbers using Conditional Convolutional Auto Encoder. Experimenting with different loss functions, training size and architecture.

Mnist images are degraded using a custom mask to remove parts of image which is then fed to the model to train it to reconstruct it to the original image.

All GIFS are outputs for test dataset.

### LR - 0.005
### Epochs - 200

## Training size (1000 images - 100 images/class)

### Loss Function- MAE

![gif MAE](https://github.com/adityarao1612/Degraded-MNIST-Reconstruction/assets/92964413/c0486273-12c1-4f83-a7ad-41c22ab6387c)

### Loss Function- SSIM

![gif Ssim](https://github.com/adityarao1612/Degraded-MNIST-Reconstruction/assets/92964413/8ad11d8a-9637-48f2-838d-10c0c6bef619)


## Training Size (150 images - 15 images / class )

### Loss Function- MAE

![gif MAE 150training images](https://github.com/adityarao1612/Degraded-MNIST-Reconstruction/assets/92964413/2bb19d2c-92ba-4b50-a06e-a88e2438ed64)

### Loss Function- SSIM

![gid Smim 150 ](https://github.com/adityarao1612/Degraded-MNIST-Reconstruction/assets/92964413/8bfea7ae-68fa-4e00-8831-d213fdef7c61)

## Findings:

1)using SSIM is much better than MAE as loss function. Output images are more confident when SSIM is used.

2)For MNIST dataset, even 15 images per class is enough to train a decent model. This is due to simplicity of the dataset. The shapes of numbers are simple and the mnist image size is small (28x28) therefore the training data need not be large though it is preferred.
