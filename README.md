# Reconstruct Gender-Neutral Superheros in Frida Kahlo's Narrative 

DSC160 Data Science and the Arts - Final Project - Generative Arts - Spring 2020

Project Team Members: 
- Weihua Zhao wez205@ucsd.edu
- Tianran Qiu tiq004@ucsd.edu
- Zishun Jin zij034@ucsd.edu
- Yijun Liu yil724@ucsd.edu
- Da Gong dagong@ucsd.edu

## Abstract

(10 points) 

For the project proposal, please write a short abstact addressing the questions below. You need to replace the entire contents of this section with one to two paragraphs addressing the following:

- What is your concept for a generative art project? 
- What methods/networks/techniques will you employ (include links to technical precedents/code bases)
- What training data (if any) will you use for your project? 
- What kind of results do you hope that your system will produce?
- How will you present your result/what form will your output take?
- What if any challenges to you think may arise as you are working with this?
- How are you expanding on topics we have covered in class? 
- Why is it interesting? (personally, culturally, politically, other)
- List three papers / art projects that are references for this work.

In this art project, we aim to recreate faces of superheroes in Frida Kahlo's portraits. Technically, we will recreate superhero faces using Deep Convolutional Generative Adversarial Network and then use CycleGAN to transfer the faces to a Frida Kahlo style. We plan to use web scraping to collect both superheros from both Marvel and D.C. universe and Frida Kalho's portraits. If things go as we plan, we will create gender-neutral style superheros and present them sequentially in a video in which we showed how they are created. Possible chanllenges might arise in creating visually pleasant, high resolution portraits since we are new to this area and have no actual experience in applying what we learned in real world problems. 
To expand on the scope of classroom topics, we recreate faces of humans instead animals and combine the techniques of DCGAN with CycleGAN and refine the feminine qualities mathematically. We are interested in this topic primarily because we noticed that superheros movies were subconsciously promoting toxic masculinity and the under-representation of feminine qualities; Frida Kahlo was an artist who was famous for exploring sexuality, gender and Politics in her paintings. We want to combine the masculinity within superheros pictures with the fluidity of gender in Kahlo' paintings to create gender-neutral superheros. 
 - https://towardsdatascience.com/face-generator-generating-artificial-faces-with-machine-learning-9e8c3d6c1ead
 - https://brokenwallsandnarratives.wordpress.com/2017/05/18/exploring-frida-the-sexuality-gender-and-politics-of-frida-kahlo/
 - https://junyanz.github.io/CycleGAN/

## Data and Model

(10 points) 

In the final submission, this section will describe both the data you use for this project and any pre-existing models/neural nets. For each you should provide the name, a textual description, and a link. If there is a paper (for neural net) link that as well.
- Such and such Neural Net. The short description of this neural net. 
  - [link to code]().
  - [Title of Paper with Link](). 
- Training data. Short description of training data including bibliographic info. [link to data]().

## Code

(20 points)

This section will link to the various code for your project (stored within this repository). Your code should be executable on datahub, should we choose to replicate your result. This includes code for: 

- code for data acquisition/scraping
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
