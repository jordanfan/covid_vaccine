# VAERS

## About / Synopsis

Physicians report patients' adverse side effects associated with a vaccine to the Vaccine Adverse Event Reporting System. The goal of the project is to create a side effect severity predictor to determine if a coronavirus vaccine (Pfizer, Moderna, J&J) is safe to administer to a patient. 

## Data Sources
* The data is retrieved from https://vaers.hhs.gov/data/datasets.html
    * Data used to train models was last pulled on 2021-05-02
* VAERS data use guide: https://vaers.hhs.gov/docs/VAERSDataUseGuide_November2020.pdf
* Drug Names: https://www.fda.gov/drugs/drug-approvals-and-databases/drugsfda-data-files
* Drug Stems: https://druginfo.nlm.nih.gov/drugportal/jsp/drugportal/DrugNameGenericStems.jsp

## Notebooks
* Drug Stem Cleaning: Process drug stem nomenclature and their drug groups
* Data Processing: combines patients' coronavirus vaccination records with their demographics, medical history, and symptoms. Convert medication a patient is taking to its active ingredients and drug group. 
* Data Exploration: visualization of side effect severity across different non-text features
* Models and Blending: various models using TF-IDF word features as input 
* BioClinical Bert: implementation of BioClinical BERT model using original medical text
* BioClinical Bert 2: implementation of BioClinical BERT model with medical text and addition of active ingredients and drug groups 