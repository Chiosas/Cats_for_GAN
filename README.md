# Cats for GAN
Generative adversarial network (GAN) model on cat's images

### **Content**

![Cat](https://cdn.dribbble.com/users/4491324/screenshots/8586953/shot-cropped-1574950787604.png)

The dataset contains 64x64 resized rgb images of cat faces.

*Format:* JPG images.

*Volume:* Total number of cats' images is almost 16,000.

We will use the dataset to build an image generative adversarial network (GAN) model.

### **Mode Collapse problem**
Techniques used to fight "Mode Collapse" in the model:
- lower learning rate,
- different learning rates and different optimizers for generator (Adam, 1e-4) and discriminator (RMSprop, 3e-4),
- label smoothing (set to 0.9 for real images),
- momentum (0.8) parameter in Batch Normalization layer.

A few more tricks to try out:
- adding noise for real and fake images,
- spectral normalization.
