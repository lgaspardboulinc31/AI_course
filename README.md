# AI_course
A repository for my AI idea as final project of [Building AI course](https://buildingai.elementsofai.com/)

# Project Title

Predicting IDH-mutant gliomas relapse with omics data

## Summary

Brain tumors are rare tumors but often remains incurable. Particularly, IDH-mutant glioma are relapsing over 10-15 years and there is to date no treatment for complete remission.
The idea of the project is to be able to develop predictive model of reccurence based on omics data. It would help to strartify the patients and eventually lead to the identification of important features of relapse. I plan to develop machine learning technique to build a predictor of relapse and unravel feature importances. If the model work, It could help clinical practice.


## Background

Brain tumors are rare tumors but often remains incurable. Particularly, IDH-mutant glioma are relapsing over 10-15 years and there is to date no treatment for complete remission. Miller et al. [1](10.1093/neuonc/noz016) demonstrated that these tumors degenerate from an indolent course to an accelerated malignant phase with a shortening of the time between diagnosis/first reccurencce and first/second recurrence. Significant work has been achieve in the classification of diffuse gliomas along the enhancment of omics data. Recent changes in classification ([Louis et al.](10.1093/neuonc/noab106)) asked the need to re-assess previous work and reclassification taks led on famous TCGA database showed that WHO CNS5 classification of gliomas have dramatically influenced the usability of the previously discovered and validated biomarkers, sometimes making them ineffective ([Zakharova et al.](10.3390/ijms24010157)). 

Not a lot of work have been performed to tackle the challenges of the relapsing tumors, how fast they relapse and which features might be important to identify patient with fastest relapse. I would thus like to propose a project and try to see if we can predict relapse and relapse speed from pre-treatment omics data. It would shed new lights on relapse mechanisms and maybe help clinical practice to identify high-risks patients and better tailored treatment. 

I am working in a lab where we are interested in such tumors and are used to perform bio-informatics analysis. However, I have never devlopped a fully machine learning based project. It is thus challenging task.

## How is it used?

The output of the model will likely have different use in fundamental and translational research in oncology.

In fundamental research : 
* Identification of specific features driving relapse
* Development of in vitro and in vivo models to obtain more mechanistic clues

In translational resarch : 
* Stratification of patient based on feature weights
* New biomarkers for relapse

If the results yielded by this project are usuable in a clinical setting, the output and how it works should be interpretable and user-friendly for doctors. 

Describe the process of using the solution. In what kind situations is the solution needed (environment, time, etc.)? Who are the users, what kinds of needs should be taken into account?

Images will make your README look nice!
Once you upload an image to your repository, you can link link to it like this (replace the URL with file path, if you've uploaded an image to Github.)
![Cat](https://upload.wikimedia.org/wikipedia/commons/5/5e/Sleeping_cat_on_her_back.jpg)

If you need to resize images, you have to use an HTML tag, like this:
<img src="https://upload.wikimedia.org/wikipedia/commons/5/5e/Sleeping_cat_on_her_back.jpg" width="300">



## Data sources and AI methods
Where does your data come from? Do you collect it yourself or do you use data collected by someone else?
If you need to use links, here's an example:
[Twitter API](https://developer.twitter.com/en/docs)


## Challenges

What does your project _not_ solve? Which limitations and ethical considerations should be taken into account when deploying a solution like this?

## What next?

How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 


## Acknowledgments

* list here the sources of inspiration 
* do not use code, images, data etc. from others without permission
* when you have permission to use other people's materials, always mention the original creator and the open source / Creative Commons licence they've used
  <br>For example: [Sleeping Cat on Her Back by Umberto Salvagnin](https://commons.wikimedia.org/wiki/File:Sleeping_cat_on_her_back.jpg#filelinks) / [CC BY 2.0](https://creativecommons.org/licenses/by/2.0)
* etc
