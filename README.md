# Emoji-the-Lego-face
Training different machine learning modles to morph between lego face and emoji images, and creating an AI-based tool that allows users to effortlessly apply Emoji expressions to the input Lego faces.

# Motivation
Facial expressions are an important characteristic for showcasing a character's uniqueness, as each character conveys different emotions in various expressions. Therefore, we want to develop an AI-based tool to alter the facial expressions of character images.

While there are many image generators that can modify facial expressions, the process of using prompts to generate new images can sometimes be very tedious, and providing the right prompts for these AI-based generative tools can be very time-consuming. Moreover, by only using prompts for image generation we can not directly forsee how the output results will be.

Hence, Our concept is to free users from the confines of text. We create an interface which is really simple to use by changing input characters' expression through choosing different expression,  provide a more intuitive and straightforward way to create new images without the need for cumbersome text descriptions.

# User interface
Our interface is designed to be simple and easy to use, allowing people of all ages to effortlessly create impressive emoji transition photos without the need for complex text descriptions.

When we are selecting various options, a scrollable menu will provide a simple and clear way. Therefore, we have designed the interface in a slider style, where the left grid can be used to choose the Lego character whose expression you want to change, and the right side is for selecting the desired emoji expression.

![Alt text](image link)

# Datasets 
In the first stage, we decided to use Variational Autoencoders as the ML model for training. We input the Lego face and emoji datasets into the same category for encoding, bringing both types of data into a shared latent space.

Lego Face dataset:

Emoji dataset:
https://www.kaggle.com/datasets/subinium/emojiimage-dataset/data
![Alt text] (https://imgur.com/MR0ENcr)

