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
## Loade mnist data, and force it to be of shape (..., 1, 28, 28) wi .... [TRUNCATED] 
> mnist$train$x <- (mnist$train$x - 127.5)/127.5
> mnist$test$x <- (mnist$test$x - 127.5)/127.5
> mnist$train$x <- array_reshape(mnist$train$x, c(60000, 1, 28, 28))
> mnist$test$x <- array_reshape(mnist$test$x, c(10000, 1, 28, 28))
> num_train <- dim(mnist$train$x)[1]
> num_test <- dim(mnist$test$x)[1]

## Training ----------------------------------------------------------------
 for(epoch in 1:epochs){  
 num_batches <- trunc(num_train/bat .... [TRUNCATED] 
 epoch 1/50  3m [=============================================================================================] 100%  0s

Testing for epoch 01:
generator (train) : loss 1.89 |  0.77 |  1.12
generator (test) : loss 1.06 |  0.96 |  0.10
discriminator (train) : loss 1.75 |  0.67 |  1.08
discriminator (test) : loss 1.00 |  0.59 |  0.41
![Rplot fashion mnist epoch 1](https://user-images.githubusercontent.com/48430890/70845401-91987380-1e91-11ea-8ffa-5204d9cc94ad.png)

Testing for epoch 50:
generator (train) : loss 0.70 |  0.70 |  0.00
generator (test) : loss 0.68 |  0.67 |  0.00
discriminator (train) : loss 0.83 |  0.70 |  0.13
discriminator (test) : loss 0.83 |  0.70 |  0.14
![Rplot fashion mnist epoch 50](https://user-images.githubusercontent.com/48430890/70845403-95c49100-1e91-11ea-8bab-87dd65181cf9.png)


# RSTUDION MNIST
## Build the discriminator
discriminator <- build_discriminator()
discriminator %>% compile(
optimizer = optimizer_adam(lr = adam_lr, beta_1 = adam_beta_1),
+ loss = list("binary_crossentropy", "sparse_catego ..." ... [TRUNCATED] 

## Build the generator
generator <- build_generator(latent_size)
generator %>% compile(
+  optimizer = optimizer_adam(lr = adam_lr, beta_1 = adam_beta_1),
+  loss = "binary_crossentropy"
+ )
latent <- layer_input(shape = list(latent_size))
image_class <- layer_input(shape = list(1), dtype = "int32")
fake <- generator(list(latent, image_class))


## Loade mnist data, and force it to be of shape (..., 1, 28, 28) wi .... [TRUNCATED] 
mnist$train$x <- (mnist$train$x - 127.5)/127.5
mnist$test$x <- (mnist$test$x - 127.5)/127.5
mnist$train$x <- array_reshape(mnist$train$x, c(60000, 1, 28, 28))
mnist$test$x <- array_reshape(mnist$test$x, c(10000, 1, 28, 28))
num_train <- dim(mnist$train$x)[1]
num_test <- dim(mnist$test$x)[1]


## Training ----------------------------------------------------------------
for(epoch in 1:epochs){  
num_batches <- trunc(num_train/bat .... [TRUNCATED]
Testing for epoch 01:
generator (train) : loss 3.04 |  0.98 |  2.05
generator (test) : loss 1.57 |  0.93 |  0.64
discriminator (train) : loss 2.18 |  0.61 |  1.57
discriminator (test) : loss 1.23 |  0.67 |  0.56
![mnist epoch 1](https://user-images.githubusercontent.com/48430890/70845182-d373ea80-1e8e-11ea-8d63-d77834f81422.png)


Testing for epoch 50:
generator (train) : loss 0.70 |  0.70 |  0.00
generator (test) : loss 0.73 |  0.73 |  0.00
discriminator (train) : loss 0.72 |  0.70 |  0.02
discriminator (test) : loss 0.70 |  0.69 |  0.01
![mnist epoch 50](https://user-images.githubusercontent.com/48430890/70845257-9c520900-1e8f-11ea-8d83-98abbcb72bb2.png)
