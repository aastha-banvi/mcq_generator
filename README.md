# mcq_generator
# Table of Content
•	Overview
•	Motivation
•	Technical Aspect
•	Pipeline
•	Installation
•	Run
•	Directory Tree
•	Technologies Used
•	Technologies Used
# Image
 ![Alt text](https://user-images.githubusercontent.com/17935364/94005755-5d58c880-fdbc-11ea-8c8e-a7fceac2dba3.png)
# Overview
This is the Web App that is being developed by using Flask, Machine Learning, Docker, hosted on GCP instance and focus on providing teachers with automatic mcq generationing system for the given article or passage.
# Motivation
I wanted to develop something that can utilize all of my learnings and also has little bit of uniqueness as well. So, after randomly looking at my younger brother's(5th standard) assignment regarding answering MCQ of given passage, I decided to automate the generation of MCQ in order to make the task of teachers little easy.
# Technical Aspect
This project is divided into four part:
1.	Building the core of the app using Natural Language Processing, Wordnet and ConceptNet.
2.	Desiging the frontend with the help of HTML, CSS, JavaScript.
3.	Building Flask API and Containerizing with the help of Docker.
4.	Deploying the whole Web App on Google Cloud Platform.
o	Used e2-medium VM instance with 2 vcpus and 4 gb ram.
o	will use domain for static ip in future.
# Pipeline
How MCQ queations along with wrong answer choice are generated?
1.	Firstly the user provide text and choose to generate MCQ from Full Text or Summary.
2.	Proper Noun words are extracted as keywords from text.
3.	If user selects Summary then we use Transformer model to generate summary and select respective keywords.
4.	Respective Sentences are selected of gien keywords.
5.	Word sense is calculated with pwysd library for WordNet.
6.	Related options (From same parent class) are extracted and if not found in Wordnet then ConceptNet(PartOf) is used.
7.	Keyword is replaced with ______ and data is return as response.
# Installation
The Code is written in Python 3.8. If you don't have Python installed you can find it here. If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after cloning the repository:
pip install -r requirements.txt
# Run
To run the app in a local machine, shoot this command in the project directory:
python Flask_api.py
Note:- It may download some of the required data on first run.
# Directory Tree
MCQ_Generator/
├── Dockerfile
├── extract_keywords.py
├── find_sentances.py
├── Flask_api.py
├── generate_summary.py
├── gen_mcq.py
├── KeyNotes.txt
├── README.md
├── requirements.txt
├── response.json
├── static
│   ├── ai.svg
│   ├── arrow.svg
│   ├── get mcq group.svg
│   ├── input_data.svg
│   ├── script.js
│   └── style.css
├── summary_notebook.ipynb
├── templates
│   └── index.html
└── test_articles
    ├── article.txt
    ├── Egypt.txt
    └── The Indus River Valley Civilizations.txt

# To Do
Using Abstract Summarization in order to produce difficullt multiple choice questions.
# Technologies Used 
•	Flask
•	DockerHtml
•	Css
•	javascript


