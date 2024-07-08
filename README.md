# degraded-MNIST-reconstruction
reconstruction of degraded mnist numbers using Conditional Convolutional Auto Encoder. Experimenting with different loss functions, training size and architecture.

Mnist images are degraded using a custom mask to remove parts of image which is then fed to the model to train it to reconstruct it to the original image.

All GIFS are outputs for test dataset.

### LR - 0.005
### Epochs - 200

## Training size (1000 images - 100 images/class)

### Loss Function- MAE

![gif MAE](https://github.com/adityarao1612/degraded-MNIST-reconstruction/assets/92964413/cc7799af-117f-47f1-b8c6-795ebf7aabf4)

### Loss Function- SSIM

![gif Smim](https://github.com/adityarao1612/degraded-MNIST-reconstruction/assets/92964413/cb553a5e-5209-4867-a9e0-0b277db9bb2b)


### Loss Function- MAE + SSIM

![gif smim+MAE](https://github.com/adityarao1612/degraded-MNIST-reconstruction/assets/92964413/d26ca845-d754-49a1-ba34-61850f0c241a)


## Training Size (150 images - 15 images / class )

### Loss Function- MAE
![gif MAE 150training images](https://github.com/adityarao1612/degraded-MNIST-reconstruction/assets/92964413/bf7e8a4a-fc32-4b43-a7d8-e67a8ebef367)

### Loss Function- SSIM
![gid Smim 150 ](https://github.com/adityarao1612/degraded-MNIST-reconstruction/assets/92964413/f8d3048d-a0e5-4524-a351-b42bb34633de)

### Loss Function- MAE + SSIM
![gif Smim + MAE 150](https://github.com/adityarao1612/degraded-MNIST-reconstruction/assets/92964413/6d9d1167-43f4-43cd-872f-48d00ca5a84a)


## Findings:
#using SSIM is much better than MAE as loss function. Output images are more confident when SSIM is used.

#For MNIST dataset, even 15 images per class is enough to train a decent model. This is due to simplicity of the dataset. The shapes of numbers are simple and the mnist image size is small (28x28) therefore the training data need not be large though it is preferred.
