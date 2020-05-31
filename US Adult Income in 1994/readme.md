# Adult Income Census Data Exploration

## Dataset

The data of __1994 Adult Census Income Data__ is from [Kaggle](https://www.kaggle.com/uciml/adult-census-income), extracted from the 1994 Census bureau database by Ronny Kohavi and Barry Becker (Data Mining and Visualization, Silicon Graphics).

The data consisted of 32560 observations. It contains demographic information of adults including `age`, `workclass`, `education`, etc., and other investment information like `capital-gain` and `capital-loss`. Including the dependant variable `income`, this dataset has 15 columns in total, 6 of them are numerical, the left are categorical.

For the purpose of interpretation and model building, I did some wrangling including merging minor levels in categorical columns etc. and got 12 columns of clean data with 30K+ observations.


## Summary of Findings

In the exploration, I found that except for capital change, nearly every characteritics have significant correlations with income groups. Some of the most significant ones are among the numerical values of `adult age`, `working hours per week`, and `eduaction level`. For these three numerical values, strong positive relationships can be seen. Also, for categorical values, two interesting findings can be seen in `sex` and `race`: Males takes the majority of high income group and White and Asian-Pac-Islander have similar high proportion of people in high income groups (around 30%) while other minorities have less proportions of high-income (less than or equal to 15%). These findings suggest potential discriminations in working siituations.

By digging deeper into the interactions related to either `sex` or `race`, I find that `hours-per-week` are good indicators of discrimination, and the discrimination degree are different across different `work classes`.




## Key Insights for Presentation

For the presentation, I focus on the story of adult income situation in 1994. I start by introducing the income distribution, and distribution plots of other fundamental demographic information such as age, gender, race, work-hours, education-num and workclass, so as to give the audience a contextual understanding of the dataset.

Then, I will introduce the 5 characteristics that are most important in predicting income group, they are numerical values of `adult age`, `working hours per week`, and `eduaction level`, which will be presented in boxplots; as well as categorical values of `sex` and `race`, with countplots. Then I will show the interaction effects of `hours-per-week` and `work classes` with either `race` or `sex` in FacetGrids mapped with countplots. 

To make the visualizations clear and consistent, I used blue for '<50K' income group and orange for '>50K' group uniformly.

_The HTML slide deck was generated using nbconvert and output_toggle.tpl, from this [repository](https://github.com/damianavila/blog/blob/master/posts/hide-the-input-cells-from-your-ipython-slides.ipynb)._
