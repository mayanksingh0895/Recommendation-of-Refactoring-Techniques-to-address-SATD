<h1 align="center">Recommending Refactoring method for a given SATD comment </h1>

## Objective:
Our main goal of this project is to perform a study on self admitted technical debts and find a method to handle this 
problem with efficiency. As a team, we decided to come up with an efficient and effective machine learning model that 
is trained on the SATD comments to predict the respective refactoring method for a novice developer to address the 
refactoring task and make the code base more reliable.


## About data source:
The data was accumulated using multiple plugins created at RIT. This data was saved as an SQL file. There was a 
relationship with the projects and SATD entities with respect to the project IDs. This is a primary key in the projects 
entity and a foreign key in the SATD entity. We were also able to understand the data better by looking at each entity. 
The projects' entity consisted of the project name and its url. The refactoring entity had various commits and 
refactoring IDs and the type of refactorings which is the most important for this project as this is target variable. 
The SATD entity carried the SATD comments which is also important for this project as this is used as the input variable. 
[<img src='https://github.com/Praveen271195/Software-Engineering-for-Data-Science/blob/main/SQL_structure.png' alt='Indicators' height='300'>]

### Observation from data
After the preliminary analysis of the database, we converted the file type to csv and read the csv files using pandas
and merged the tables with respect to the SATD ID. We came up with two research questions, **RQ1. Which specific 
refactoring activities occur most frequently with the removal of SATD comments?** **RQ2. Can we implement an ML solution 
to identify the appropriate refactoring activity for a given SATD comment to be removed?** Now let's discuss more about 
the input and output of the model. The SATD comments will be treated as the input and these are plain natural language 
data added by the developers to admit their debts. Features can be extracted from these comments using NLP techniques so
that the model can work on it. The expected outputs will be a recommendation of the model out of the 10 refactoring 
types available in the dataset. The goal of the model is to recommend the most accurate refactoring type to the developer.

### Basic structure of our the solution
In-order to solve the stated problem and address the issues that arise from the SATD, we have come up with a solution to
recommend the right type of refactoring to the software developer by providing the SATD comments as input to the Machine
Learning model that can give us the most accurate refactoring type. This auto-recommendation of the refactoring will 
help the novice software developers to know what kind of refactoring is suitable and will allow the developer to think 
from the recommendation front.
[<img src='https://github.com/Praveen271195/Software-Engineering-for-Data-Science/blob/main/project_flow.png' alt='Indicators' height='300'>]


## Result summary of the project
[<img src='https://github.com/Praveen271195/Software-Engineering-for-Data-Science/blob/main/Result_sum.png' alt='Indicators' height='300'>]

## Prerequisites
To start using this project with Git, you’ll need to install or have access to the following program. <br/>
- [Git](https://git-scm.com/download/) <br/>
- [Python 3.9.9](https://www.python.org/downloads/) <br/>
- [Jupyter Notebook](https://jupyter.org/install) or [Google Colab](https://colab.research.google.com/) <br/>


## Libraries
- <a href="https://pandas.pydata.org/">Pandas</a>
- <a href="https://numpy.org/">Numpy</a>
- <a href="https://seaborn.pydata.org/">Seaborn</a>
- <a href="https://matplotlib.org/stable/tutorials/introductory/pyplot.html">Matplotlib Pyplot</a>
- <a href="http://amueller.github.io/word_cloud/">Wordcloud</a>

## Getting started

### Installation

#### Git
Git can be installed using a CLI or an executable file. The installation instructions can be found at the following 
link: [Windows](https://git-scm.com/download/win) or [Mac OSX](https://git-scm.com/download/mac)


#### Python and Jupyter notebook
If you have not installed Python 3.9 already, the easiest method to install both the programs is by installing 
[anaconda](https://www.anaconda.com/) The following link provides a graphical installer link for both Windows and 
macOS [Link](https://www.anaconda.com/products/individual)

If you have already installed Python 3.9 and are an advanced user, you can install Jupyter Notebook on terminal by 
following the steps below.

	pip3 install jupyter	

### Setting up your local
In Terminal, navigate to the respective directory where you want to clone this repository and run the following command.
<br/>

   ```
   git clone https://github.com/mayanksingh0895/Recommendation-of-Refactoring-Techniques-to-address-SATD.git
   ```
### Running the environment

#### Jupyter notebook

If you have installed the Jupyter notebook via anaconda, you can run the notebook directly by double-clicking on the 
Jupyter notebook icon on the start menu on Windows or Mac, going to the app drawer and selecting the Jupyter notebook.

If you have installed Jupyter notebook via Python, you can go to Terminal and type the following code:
 
   ```
   jupyter notebook
   ```

Both the processes will open up the Jupyter notebook environment in a default web browser. 

In the application window, there will be a file explorer. Navigate to the respective folder where you have cloned the 
project and select the **" Movie Recommendation system - DSCI Final Project.ipynb "** to load up the notebook. 

#### Google colab

If you want to run this project on Google Colab, Navigate to the following [link](https://colab.research.google.com/)

In the application window, click on File->Open Notebook from the menu tab or press Ctrl + O. On the open popup model, 
click on upload file and go to the respective folder where this project is cloned and select the **" Recommendation of 
Refactoring Techniques to address SATD.ipynb "** so that it can be uploaded to Google Colab.
