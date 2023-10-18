# Emoji-the-Lego-face
Training different machine learning modles to morph between lego face and emoji images, and creating an AI-based tool that allows users to effortlessly apply Emoji expressions to the input Lego faces.

# Motivation
Facial expressions are an important characteristic for showcasing a character's uniqueness, as each character conveys different emotions in various expressions. Therefore, we want to develop an AI-based tool to alter the facial expressions of character images.

While there are many image generators that can modify facial expressions, the process of using prompts to generate new images can sometimes be very tedious, and providing the right prompts for these AI-based generative tools can be very time-consuming. Moreover, by only using prompts for image generation we can not directly forsee how the output results will be.

Hence, Our concept is to free users from the confines of text. We create an interface which is really simple to use by changing input characters' expression through choosing different expression,  provide a more intuitive and straightforward way to create new images without the need for cumbersome text descriptions.

# User interface
Our interface is designed to be simple and easy to use, allowing people of all ages to effortlessly create impressive emoji transition photos without the need for complex text descriptions.

When we are selecting various options, a scrollable menu will provide a simple and clear way. Therefore, we have designed the interface in a slider style, where the left grid can be used to choose the Lego character whose expression you want to change, and the right side is for selecting the desired emoji expression.

![interface|300*200](https://attachments.office.net/owa/chiu119%40purdue.edu/service.svc/s/GetAttachmentThumbnail?id=AAMkADFiMzQ0ZmNmLWVlZDUtNDQ2YS04MDUyLTgzNDYyNWIxZDlkYwBGAAAAAAASMAPuO3%2F%2FR7IblUJ4z%2FAaBwCtWUJ8w2yHTYlpKMyZJqCYAAAAAAEMAACtWUJ8w2yHTYlpKMyZJqCYAAB6GBCnAAABEgAQAIMLgwZztKREpmlPpiSzhok%3D&thumbnailType=2&token=eyJhbGciOiJSUzI1NiIsImtpZCI6IjczRkI5QkJFRjYzNjc4RDRGN0U4NEI0NDBCQUJCMTJBMzM5RDlGOTgiLCJ0eXAiOiJKV1QiLCJ4NXQiOiJjX3VidnZZMmVOVDM2RXRFQzZ1eEtqT2RuNWcifQ.eyJvcmlnaW4iOiJodHRwczovL291dGxvb2sub2ZmaWNlLmNvbSIsInVjIjoiZDRlZWMyNWU2NmE1NGY5MmI0NzdiYTI0NWVmOTZjMTAiLCJzaWduaW5fc3RhdGUiOiJbXCJrbXNpXCJdIiwidmVyIjoiRXhjaGFuZ2UuQ2FsbGJhY2suVjEiLCJhcHBjdHhzZW5kZXIiOiJPd2FEb3dubG9hZEA0MTMwYmQzOS03YzUzLTQxOWMtYjFlNS04NzU4ZDZkNjNmMjEiLCJpc3NyaW5nIjoiV1ciLCJhcHBjdHgiOiJ7XCJtc2V4Y2hwcm90XCI6XCJvd2FcIixcInB1aWRcIjpcIjExNTM4MDExMjUwMTk3MzUzMDBcIixcInNjb3BlXCI6XCJPd2FEb3dubG9hZFwiLFwib2lkXCI6XCIyMTFlMTQ2Mi0xYzY3LTRmMTUtOWYyYi03NDI5OTMxMjUyMzRcIixcInByaW1hcnlzaWRcIjpcIlMtMS01LTIxLTI1MDM2MTM2NTEtNTU2MjkxNjgyLTM4MTcyNzAwNC01NjU2MzY2OVwifSIsIm5iZiI6MTY5NzY0NTk2NSwiZXhwIjoxNjk3NjQ2NTY1LCJpc3MiOiIwMDAwMDAwMi0wMDAwLTBmZjEtY2UwMC0wMDAwMDAwMDAwMDBANDEzMGJkMzktN2M1My00MTljLWIxZTUtODc1OGQ2ZDYzZjIxIiwiYXVkIjoiMDAwMDAwMDItMDAwMC0wZmYxLWNlMDAtMDAwMDAwMDAwMDAwL2F0dGFjaG1lbnRzLm9mZmljZS5uZXRANDEzMGJkMzktN2M1My00MTljLWIxZTUtODc1OGQ2ZDYzZjIxIiwiaGFwcCI6Im93YSJ9.uO4Q-5XAj3Q7GvqR4NwAweAITOUR5sSUaB2aDctlSDyyANcwPVKGwd7rc6gqs8-KianjyH7MnsgwplLfNg0t_nkPEkJ8FyEYHsAxUVr3VqL5V5a4xITr3pofF56JMy7TCmz23v0V7laaIMbeby4hkfR6LkhYjPSlN_2hS7vQ5yW3nsWxgLYwKEgPKDHU2IMAHcI8vSdajb_o-n6bFVKwaKL06LT4hMVtZqMwHjs0Ns7qczLtL0L7p2FBPk1qWiNOcOx8WL1sefZsbwzzpUdlMH4Mzijtl6IUiBwo4OmtecYSzEl5xcmI8s59wnJP68te7HbM8uZLQN9WqG8uGmhN-w&X-OWA-CANARY=GGf6UqRXEEi4QxWEBg7jSFDJ1wH2z9sYrr_R1wV2CWmCucNjxa6YMlSDCMtMOFUAi2Os3-Dthbg.&owa=outlook.office.com&scriptVer=20231006004.18&animation=true)

# Datasets 
In the first stage, we decided to use Variational Autoencoders as the ML model for training. We input the Lego face and emoji datasets into the same category for encoding, bringing both types of data into a shared latent space.

Lego Face dataset:
https://github.com/iechevarria/lego-face-VAE/blob/master/dataset.zip
![plot]()

Emoji dataset:
https://www.kaggle.com/datasets/subinium/emojiimage-dataset/data
![plot]()

# VAE training
We refer to and modify the VAE model in David Foster's excellent book Generative Deep Learning: Teaching Machines to Paint, Write, Compose, and Play. 

