# Missing_lab_tests

We created a model to detect missing lab tests which are crucial in increasing the accuracy of Automatic Diagnosis using MIMIC-III dataset and medical data from Wikidata.

MIMIC-III is a freely accesible dataset which is available on https://physionet.org/content/mimiciii/1.4/.
To gain access to the dataset,please perform the following steps.

  1. Create an account on https://physionet.org/register/
  2. Complete required tainings 
  3. Request access using certificate
 
After gaining access to the MIMIC-III dataset, we used D_ICD_DIAGNOSES.csv file to extract diseases and all the labtests associated with it and also NOTEEVENTS.csv file to perform Automatic Diagnosis.

Follow the steps for replicate the results:

step 1: Load the CSV file DIAGNOSES_ICD.csv to the Lab_Tests.ipynb file.
We extracted Diseases and all the related labtests associated with it in different batches, each of around 10000 records due to limitations in run time. Alternatively you can also generate the dataset using SPARQL queries in wikidata Query.txt

Step 2:Load the CSV file NoteEvents or you can manually enter summaries of patient behaviour in the Automatic_diagnosis.ipynb to generate all the possible diagnoses based on patients labtests, symptoms and risk factors.

step 3: Use the file generated in the step 1 along with the output predicted in step 2 in Missing_labtests.ipynb to find the missing lab tests

The web application is created using Ngrok a cross-platform application that exposes local server ports to the Internet.

To run the web application on your local machine run the Missing_Lab_Tests.ipynb file, a link will be generated which will take you the User Interface.

