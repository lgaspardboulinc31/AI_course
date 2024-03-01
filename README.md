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

If the results yielded by this project are usuable in a clinical setting, the output and how it works should be interpretable and user-friendly for doctors that are not familiar with programming.  

## Data sources and AI methods

### Data sources
For this project, I would like to rely on the diversity of omics data that are available in The Cancer Genome Atlas (TCGA) project funded by NIH : https://www.cancer.gov/ccg/research/genome-sequencing/tcga. 
They possess publicly available data set for Low Grade Gliomas that can be freey retrieve along clinical data : 
  * First publication : https://www.nejm.org/doi/full/10.1056/NEJMoa1402121
  * Dataset : https://www.cbioportal.org/study/summary?id=lgg_tcga
    
This repository contains transcriptomics data from bulk tumors but also methylation, mutational and protein data. A diversity of model can be developped based on one modality to several. 

One new interest I have is in the spatial transcriptomics data. Multiple studies showed the importance of tumor microenvironnment in tumor progression and relapse. I would like thus to use this new type of data to implement machine learning models. 

### AI methods
The aim of the project is to predict relapse, which is encoded in the clinical data retrieved from TCGA. So we would apply a **classification task** to predict the categorical variable that is {0-No relapse, 1-Relapse}. We would try a diversity of algorithms and try to assess their performance. I would start with the simplest approach such as Naive Bayes classifier or logistic regression. Given the complex relationships and interactions of biological data, we might need to implement more complex method such as a neural network. 

The problem can also be seen as a **regression task** if we see the outcome not as a categorical variable but as **continuous variable** encoded in month for each patient. We could thus try to implement diverse model ranging from linear regression to more complex neural networks. 

Some peculiar interest for me would be to identify the most important features in each modality. Thus regression framework seems promising. 


## Challenges

These are some limitations : 
* Data availability : there is less than 300 patients in TCGA database, which limit the quantity of data. it also exist very few external data for validation.
* Data pre-processing : the project requires a certain amount of work before actually implementing ML algorithms (data cleaning, check information, normalization etc.)
* Features : whole transcriptomic data are of high dimension (>15,000 genes!) thus we might need perform some *feature selection* based on a-priori knowledge or other types of models (LASSO regression)
* Spatial transcriptomics features : spatial omics is still new and my idea is to create spatial features such as co-localization indexes, distances between cell-types etcs. to describe the tumor microenvironment, which require a lot of work too.
* Confounding effect : a confounder is a variable that influences both the dependent variable and independent variable, causing a spurious association. Multiple other clinical data are available and we will need to check for such effects before making any conclusion. 


## What next?

This project would grow faster and be more powerful with a fully computational biologist or computer science background expert in AI and Machine Learning. I think the help of a doctor would help to refine the biological question and interpret the results of the model, as well as give advice for its translation into clinics. 

## Acknowledgments

* Nicolas Captier for starring all my repository
