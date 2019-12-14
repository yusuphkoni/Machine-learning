# PYTHON FASHION_ MNIST_CGAN 
### Generation_animation
![MNIST_cGAN_gneration_animation](https://user-images.githubusercontent.com/48430890/70844605-1631c480-1e87-11ea-9092-fc207b7f9599.gif)

### Training_hist example
![MNIST_cGAN_training_hist](https://user-images.githubusercontent.com/48430890/70844677-efc05900-1e87-11ea-9a93-8ec9ad8e928a.png)


# PYTHON MNIST_CGAN 
### Generation_animation
![MNIST_cGAN_gneration_animation](https://user-images.githubusercontent.com/48430890/70844740-7a08bd00-1e88-11ea-81b9-558617972820.gif)
### Training example
![MNIST_cGAN_train_hist](https://user-images.githubusercontent.com/48430890/70844749-a45a7a80-1e88-11ea-9c7a-3b5bc954d330.png)

# RSTUDIO FASHION_MNIST
## Build the discriminator
> discriminator <- build_discriminator()

> discriminator %>% compile(
+   optimizer = optimizer_adam(lr = adam_lr, beta_1 = adam_beta_1),
+   loss = list("binary_crossentropy", "sparse_catego ..." ... [TRUNCATED] 

## Build the generator
> generator <- build_generator(latent_size)

> generator %>% compile(
  optimizer = optimizer_adam(lr = adam_lr, beta_1 = adam_beta_1),
  loss = "binary_crossentropy"

## Training ----------------------------------------------------------------
 for(epoch in 1:epochs){  
 num_batches <- trunc(num_train/bat .... [TRUNCATED] 
 epoch 1/50  3m [=============================================================================================] 100%  0s

Testing for epoch 01:
     generator (train) : loss 1.89 |  0.77 |  1.12
      generator (test) : loss 1.06 |  0.96 |  0.10
 discriminator (train) : loss 1.75 |  0.67 |  1.08
  discriminator (test) : loss 1.00 |  0.59 |  0.41


# RSTUDION MNIST

