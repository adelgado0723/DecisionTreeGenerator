# [Decision Tree Generator](https://github.com/adelgado0723/portfolio/tree/master/DecisionTreeGenerator/src)


## Contents


## About

Decision Trees are a way of finding correlations in people's behavior from data about their habits. This program builds a decision tree based on a given input file and then proceeds to classify a user-provided tuple of data. 
		
### Examples:	

- The majority of customers that buy diapers, buy beer as well
		
- The majority of customers that are students, regardless of credit, buy a laptop computer


## Step 1 - User Prompted to Select Input File

### Prompt

The program prompts the user fo choose an input file containing the data that is to be used for generating a decision tree.

![Selection Prompt](media/screenshots/2_select_file_prompt.png)

### File Chosen

The program uses *Java*'s ***Jfilechooser*** object for allowing the user to choose the input file through a GUI.

![File Chooser GUI](media/screenshots/3_file_selector.png)

### Contents of in.txt

The first row of the input file provides the names of attributes while the rest of the rows are collected data points corresponding to those attributes. In this example input file the attributes are:

- age
- income
- student
- credit_rating
- buys_computer

Reading the second row, we can see it belongs to a customer who falls in the ***youth*** age class, the ***high*** income class, the ***no*** student class, the ***fair*** credit rating class, and the ***no*** buys_computer class. So this person is young, makes high income, is not a student, has a fair credit rating, and *did not buy a computer*.

![Sample Input](media/screenshots/1_sample_input.png)

## Step 2 - Decision Tree is Displayed

Here, the decision tree is displayed in a JTextArea object. The root of the tree will be the attribute with the highest calculated entropy and is used to produce the first *split* in the tree. Entropy is an estimate of the information that could be gained by splitting  that decision tree using a given attribute. In the image below, we can see that the attribute with the highest calculated entropy was ***age*** and the possible classes include ***{youth, middle_aged, senior}***. The attribute with the highest entropy is selected in order to keep the tree as small as possible.

![Example1](media/screenshots/4_decision_tree.png)

## Step 3 - Query Tuple is Provided
![Example1](media/screenshots/5_providing_tuple.png)

## Step 4 - Prediction is Displayed

A simple prediction is displayed in the 
![Example1](media/screenshots/6_prediction.png)


## Demo
![Demo](media/demo.gif?raw=true)
