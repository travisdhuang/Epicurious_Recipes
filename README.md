# Epicurious Recipes 
Machine Learning Study on a Dataset of Epicurious Recipes

Data provided by Hugo Darwood via Kaggle: https://www.kaggle.com/hugodarwood/epirecipes
- In the interest of meeting a 3 week deadline, emphasis was placed on developing algorithms rather than data collection
- There are several APIs available for recipe databases but are limiting due to cost and # of calls
- Webscraping was also contemplated but ultimately foregone due to time considerations

### Goals:
##### 1.  Predict user rating based on features of each recipe: Supervised Learning
- Higher or lower rating based on similar recipes (classifier)
- Estimated score (regressor)

##### 2.  Recipe recommendation engine: classification model
- Will take some input (base ingredients, cuisine style, nutritional content) and return a classifier
- Collaborative filtering ( If a person A likes item 1, 2, 3 and B like 2,3,4 then they have similar interests and A should like item 4 and B should like item 1)

### Challenges

Features are a mess

![alt text](https://github.com/travisDhuang/Epicurious_Recipes/blob/master/recipes_eda.png)

Rating distribution is NOT normalized

![alt text](https://github.com/travisDhuang/Epicurious_Recipes/blob/master/rating_distribution.png)

Feature Engineering: 680 columns
- Ingredients are already label encoded
- Nutrition content useful, but not relevant in recommendations based on user taste preferences

Initial EDA yields some pretty strange outliers:

![alt text](https://github.com/travisDhuang/Epicurious_Recipes/blob/master/salty_outliers.png)


Linearly Separable Data?
- Binary classification and linear models will have a hard time if data is not linearly seperable
- Use tree based models if so

Danger of over fitting: if model is trained on specific inputs, it will not be applicable to others
- Clustering
- Build a 'user' similarity matrix
 


#### Similarity Metrics
1.  Cosine Similarity
2.  Pearson Similarity
3.  Jaccard Similarity
