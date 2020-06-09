# Reconstruct Gender-Neutral Superheros in Frida Kahlo's Narrative 

DSC160 Data Science and the Arts - Final Project - Generative Arts - Spring 2020

Project Team Members: 
- Weihua Zhao wez205@ucsd.edu
- Tianran Qiu tiq004@ucsd.edu
- Zishun Jin zij034@ucsd.edu
- Yijun Liu yil724@ucsd.edu
- Da Gong dagong@ucsd.edu

## Abstract


Pop culture is filled with symbolic representations. One of the most significant and powerful representations is the imagery of superheroes. If you dissect the notion of prevalent superheroes, it is not difficult to notice that most of them are white males with extreme gender characteristics, such as masculinity. This single-handed over-representation brings us to the topic of this art project. To reconstruct the gender characteristics of superheroes and diversify them, in this art project, we aim to recreate faces of superheroes in Frida Kahlo's perspective, who was an artist famous for exploring sexuality, gender and Politics in her paintings. 
To collect data, we decided to use web scraping to collect superheros of both Marvel and D.C. universes from https://www.superherodb.com/characters/ and Frida Kalho's portraits from https://www.frida-kahlo-foundation.org/. Firstly, we will use the marvel heroes datasets as our training data to recreate new superhero faces using Deep Convolutional Generative Adversarial Network with PyTorch. After finishing recreating new faces, we will use CycleGAN to transfer superheroes faces in a Frida Kahlo style, by which we aim to emphasize femininity and lessen the masculinity.If things go as we plan, we will create gender-neutral style superheros and present them sequentially in a video in which we showed how they are created. 
Possible challenges might arise in creating visually pleasant, high resolution portraits since we are new to this area and have no actual experience in applying what we learned in real world problems. Other challenges might include the detailed criteria of femininity. To expand on the scope of classroom topics, we recreate faces of humans instead of animals and combine the techniques of DCGAN with CycleGAN and refine the feminine qualities mathematically. 
We are interested in this topic primarily because we noticed that superheros movies were subconsciously promoting toxic masculinity and the under-representation of feminine qualities. Judith Butler once said gender was socially constructed. To rephrase her saying, sex is a biological characteristic, while gender is socially constructed. In this art project, we aim to reconstruct the gender notions of superheroes. We want to redefine the faces of superheros through combining the masculinity within old superheros with the fluidity of gender in Kahlo' paintings to create gender-neutral superheros. 


 - https://towardsdatascience.com/face-generator-generating-artificial-faces-with-machine-learning-9e8c3d6c1ead
 - https://brokenwallsandnarratives.wordpress.com/2017/05/18/exploring-frida-the-sexuality-gender-and-politics-of-frida-kahlo/
 - https://junyanz.github.io/CycleGAN/
 - Butler, Judith. “Performative Acts and Gender Constitution: An Essay in Phenomenology and Feminist Theory.” Theatre Journal, vol. 40, no. 4, 1988, pp. 519–531. JSTOR, www.jstor.org/stable/3207893. Accessed 26 May 2020.


## Data and Model

(10 points) 
- These are the example code and pre-existing models that we used. 
  - [DCGAN](https://github.com/roberttwomey/ml-art-code/blob/master/week8/DCGAN_Pytorch/dcgan_train.ipynb).
  This pre-existing DCGAN (Deep Convolution Generative Adversarial Networks) model is based on Pytorch. As [this paper](https://arxiv.org/abs/1511.06434) indicates, DCGAN is an unsupervised learning model that could work perfectly on learning a hierarchy of representations from object parts to scenes in both the generator and discriminator. 
  - [Style Transfer](https://github.com/roberttwomey/dsc160-code/blob/master/examples/style_transfer_tensorflow/style_transfer_keras.ipynb). 
  When transfering superheroes into the style of Frida's works, we refer to this code example. This transformer is based on tensorflow and the benefit of this model is its feedforward attribute -- train a network to do the stylizations for a given painting beforehand so that it can produce stylized images instantly.
- Training data. Our Data are collected in different websites.
  - [Marvel Superheroes Dataset](https://www.marvel.com/characters): This website contains 2587 images from Marvel world.
  - [DC Superheroes Dataset](https://www.dccomics.com/characters): This website contains 191 images from DC world.
  - [Kaggle Superheroes Dataset](https://www.kaggle.com/vibster2397/superheroes). This website contains 2045 images from Marvel world. <br/>
We collected superheroes from those website by hand.
  - [Frida Kahlo Dataset](https://www.wikiart.org/en/frida-kahlo): This website contains 99 paintings by Frida Kahlo.<br/>
  We scrape wikiart page to get the artworks from Frida Kahlo, a Mexican painter famous for her depiction on neutral-gender style self-portraits.
  

## Code

(20 points)

This section will link to the various code for your project (stored within this repository). Your code should be executable on datahub, should we choose to replicate your result. This includes code for: 

- Data Acquisition/ Scraping
  * [Scraping](/code/scrape_frida_arts.ipynb): This is the code we used for scraping Frida's artworks from Wiki-art.
- code for preprocessing
- training code (if appropriate)

- generative methods

Link each of these items to your .ipynb or .py files within this seection, and provide a brief explanation of what the code does. Reading this section we should have a sense of how to run your code.

## Results

(30 points) 

This section should summarize your results and will embed links to documentation to significant outputs. This should document both process and show artistic results. This can include figures, sound files, videos, bitmaps, as appropriate to your generative art idea. Each result should include a brief textual description, and all should be listed below: 

- image files (`.jpg`, `.png` or whatever else is appropriate)
- audio files (`.wav`, `.mp3`)
- written text as `.pdf`

## Discussion

(30 points, three to five paragraphs)

The first paragraph should be a short summary describing your results.

The subsequent paragraphs could address questions including:
- Why is this culturally innovative?
- How does your generative computational approach differ from traditional art/music/cultural production? 
- How do your results relate to broader social, cultural, economic political, etc., issues? 
- What are the ethical concerns for this form of generative art? 
- In what future directions could you expand this work?

## Team Roles

Provide an account of individual members and their efforts/contributions to the specific tasks you accomplished.

## Technical Notes and Dependencies

Any implementation details or notes we need to repeat your work. 
- Additional libraries you are using for this project
- Does this code require other pip packages, software, etc?
- Does this code need to run on some other (non-datahub) platform? (CoLab, etc.)

## Reference

All references to papers, techniques, previous work, repositories you used should be collected at the bottom:
- Papers
- Repositories
- Blog posts
