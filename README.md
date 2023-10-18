# Emoji-the-Lego-face
Training different machine learning modles to morph between lego face and emoji images, and creating an AI-based tool that allows users to effortlessly apply Emoji expressions to the input Lego faces.

# Motivation
Facial expressions are an important characteristic for showcasing a character's uniqueness, as each character conveys different emotions in various expressions. Therefore, we want to develop an AI-based tool to alter the facial expressions of character images.

While there are many image generators that can modify facial expressions, the process of using prompts to generate new images can sometimes be very tedious, and providing the right prompts for these AI-based generative tools can be very time-consuming. Moreover, by only using prompts for image generation we can not directly forsee how the output results will be.

Hence, Our concept is to free users from the confines of text. We create an interface which is really simple to use by changing input characters' expression through choosing different expression,  provide a more intuitive and straightforward way to create new images without the need for cumbersome text descriptions.

# User interface
Our interface is designed to be simple and easy to use, allowing people of all ages to effortlessly create impressive emoji transition photos without the need for complex text descriptions.

When we are selecting various options, a scrollable menu will provide a simple and clear way. Therefore, we have designed the interface in a slider style, where the left grid can be used to choose the Lego character whose expression you want to change, and the right side is for selecting the desired emoji expression.

![interface](https://i.imgur.com/aLB76bO.png=120x80)

# Datasets 
In the first stage, we decided to use Variational Autoencoders as the ML model for training. Its because we want to realize how the latent space works, and how the images change in latent space. We input the Lego face and emoji datasets into the same category for encoding, bringing both types of data into a shared latent space.

Lego Face dataset:
https://github.com/iechevarria/lego-face-VAE/blob/master/dataset.zip
![lego_faces](https://i.imgur.com/OUEzqBn.png)

Emoji dataset:
https://www.kaggle.com/datasets/subinium/emojiimage-dataset/data
![emojis](https://i.imgur.com/MR0ENcr.png)

Then we selected clear images from these two datasets and combined them to create a dataset containing 1994 images.

# VAE training
We refer to and modify the VAE model in David Foster's excellent book Generative Deep Learning: Teaching Machines to Paint, Write, Compose, and Play. Our program has been uploaded in this Files as lego_face_emoji.ipynb.

After adjusting parameters and training for plenty of times, we had so far best result of morhing lego faces and emojis. The below chart is the Kl_loss of this training. We train 250 epochs with BATCH_SIZE = 512 for 1 hour. The KL loss tends to stabilize around 14 to 15 as the number of epochs increases to 250.

![Kl_loss](https://i.imgur.com/lH3FBoQ.png)

Training results:
Lastent space distribution:
![distribution](https://i.imgur.com/VO7CHtG.png)
We print the first 50 Guassian distribution with latent space result

And the following pictures are the new faces we encode from the latent space:
![newface](https://i.imgur.com/bYZnT0M.png)

Restruction:
![reconstruction](https://i.imgur.com/5UAcMcO.png)
Though the results are not very good, but we can still generate the outputs that has most of features of original inputs.

# Morphing

After training the VAE of lego faces and emojis, we randomly choose 2 spots from lego faces and emojis in latent space and plot 10 new faces on the the line connecting these two points. Creating a morphing result between two faces.
![morphing](https://i.imgur.com/z0oLSh7.png)
