FAQ - Personal Loan Campaign
1. How should one approach the Personal Loan Campaign project?
Before starting the project, please read the problem statement carefully and go through the criteria and descriptions mentioned in the rubric.
Once you understand the task, download the dataset and import it into a Jupyter notebook to get started with the project.
To work on the project, you should start with data preprocessing and EDA using descriptive statistics and visualizations.
Once the EDA is completed and data is preprocessed, you can use the data to build a model and check its performance.

It is important to close the analysis with key findings and recommendations to the business.

2. Decision Tree arrows are missing, how to fix this?
Use the following code as a reference to resolve the issue and make necessary changes (name of the model, feature names, etc):

plt.figure(figsize=(20,30))
out = tree.plot_tree(model,feature_names=feature_names,filled=True,fontsize=9,node_ids=False,class_names=None,)
#below code will add arrows to the decision tree split if they are missing
for o in out:
     arrow = o.arrow_patch
     if arrow is not None:
        arrow.set_edgecolor('black')
        arrow.set_linewidth(1)
plt.show()
3. How to deal with "ZIPCode'' as it is a numeric value but it's also essentially a category?
You can explore the following links to deal with zip codes:

1. uszipcode (https://pypi.org/project/uszipcode/) - Python package that can help in mapping zip codes to different locations 

2. https://www.smartystreets.com/articles/zip-4-code - Description of how zip codes are created in the US. 

4. Should I create dummies for the columns that only have 0’s and 1’s?
No, it is not necessary to create dummies for these columns.

5. I'm trying to post-prune the decision tree.  But I'm getting the following error:
“ValueError: ccp_alpha must be greater than or equal to 0"
How to resolve this?
To resolve this error kindly use absolute values (positive value) of alpha. Use the following lines of code to resolve the error:

ccp_alphas, impurities = abs(path.ccp_alphas), path.impurities
6. I get the following error:
ModuleNotFoundError: No module named 'nb_black'
how do I install nb_black? 
Run the below code in the anaconda prompt

pip install nb-black
or run the below code in jupyter notebook.

!pip install nb-black 