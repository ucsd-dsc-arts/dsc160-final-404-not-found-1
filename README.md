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
- Data Acquisition/ Scraping
  * [Scraping](/code/scrape_frida_arts.ipynb): This is the code we used for scraping Frida's artworks from Wiki-art.
- code for preprocessing
  * [DCGAN](/Final_Project_Group_404-not-found.ipynb): We preprocessed import data through the libray of torchvision.datasets. All imported image is scaled and normalized for applying pytorch algorithm.
- training code / generative methods
  * [DCGAN](/Final_Project_Group_404-not-found.ipynb): This is the code we used to train the DCGAN model, from this code, we generated new superheroes based on our input DC and Marvel datasets.
  * [Style transfer](/style_transfer_keras.ipynb): We used this style transfer to combine the style of Frida Kahlo into the new-generated superheroes from DCGAN.

## Results

[![500 EPOCHS RESULT](http://img.youtube.com/vi/o9a6aOox2I0/0.jpg)](https://www.youtube.com/watch?v=o9a6aOox2I0 "500 EPOCHS RESULT")

We compiled the samples of 500 epochs results into one video. In the video, we can see that the generated result improves over the time. However, about one minute into the video, we can see that there are lots of duplicated resulting images. In order to have satisfying results from DCGAN, we acquire a database much larger than 3000 images. However, our database is limited as the number of heroes in comics are limited. To achieve better results, we duplicated the data base three times. It could be the reason that we have similar resulting images. Among the resulting faces we got, there are many faces that are recognizable and gender neutral. This result on the top right is like an alien version of Valkyrie. However, it also contains masculinity. This is clearly a strong gender-neutral superheroes.
We also used a method called styler transfer. Here is the result after using style transfer. The resulting images of gender neutral heroes are more recognizable comparing to results from DCGAN. However, the resulting image shares great similarity with the original images. It is more like apply frida image as a filter on top of the hero images. We do not really see the application of gender neutral process in the resulting images. 

This section should summarize your results and will embed links to documentation to significant outputs. This should document both process and show artistic results. This can include figures, sound files, videos, bitmaps, as appropriate to your generative art idea. Each result should include a brief textual description, and all should be listed below: 

These are the generated superheros from the 500 epochs we generated:
![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-404-not-found-1/blob/master/results/results/WeChat%20Image_2020060704331512.png)
![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-404-not-found-1/blob/master/results/results/WeChat%20Image_2020060704331573.png)
![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-404-not-found-1/blob/master/results/results/WeChat%20Image_2020060704331515.png)
![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-404-not-found-1/blob/master/results/results/WeChat%20Image_2020060704331538.png)
![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-404-not-found-1/blob/master/results/results/WeChat%20Image_2020060704331517.png)
![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-404-not-found-1/blob/master/results/results/WeChat%20Image_2020060704331527.png)
![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-404-not-found-1/blob/master/results/results/WeChat%20Image_2020060704331535.png)
![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-404-not-found-1/blob/master/results/results/WeChat%20Image_202006070433155.png)
![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-404-not-found-1/blob/master/results/results/WeChat%20Image_2020060704331570.png)
![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-404-not-found-1/blob/master/results/results/WeChat%20Image_2020060704331540.png)
![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-404-not-found-1/blob/master/results/results/WeChat%20Image_2020060704331559.png)
This is result from the 451th epoch, which contains some human faces:
![alt text](https://github.com/ucsd-dsc-arts/dsc160-final-404-not-found-1/blob/master/results/500EPOCHs/fake_samples_epoch_451.png)

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
- Weihua Zhao:
- Tianran Qiu:
- Zishun Jin:
- Yijun Liu:
- Da Gong: Da Gong is in charge of using DCGAN provided by PyTorch to generate new superhero images. Before deciding which algorithm is using for this project, he is responsible for discovering all possible ways and estimates every way's time costs and complex cost. Overall, he is constantly sharing ideas with other teammates and make decisions for this project with other teammates.


## Technical Notes and Dependencies

Any implementation details or notes we need to repeat your work. 
- Additional libraries you are using for this project
None. All libraries are listed in all notebooks.
- Does this code require other pip packages, software, etc?
We used only latest version of pytorch, tensorflow and scipy.
- Does this code need to run on some other (non-datahub) platform? (CoLab, etc.)
None. Due to the relatively small calculation need, any platform with individual GPU can run all notebooks.


## Reference

All references to papers, techniques, previous work, repositories you used should be collected at the bottom:
- Alec Radford, et al. “Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks.” ArXiv.org, Cornell University, 7 Jan. 2016, arxiv.org/abs/1511.06434.
- Pytorch. “Pytorch/Examples.” GitHub, 21 May 2020, github.com/pytorch/examples/tree/master/dcgan.
- Professor Robert Twomey, "dsc160-code/Style_Transfer", https://github.com/roberttwomey/dsc160-code/tree/master/examples/style_transfer_tensorflow
- Professor Robert Twomey, "ml-art-code/DCGAN_Pytorch", https://github.com/roberttwomey/ml-art-code/tree/master/week8/DCGAN_Pytorch

