# Marvel & DC Character Analysis

## Applied Data Science Project 

![Marvel and DC Banner](https://github.com/gabriel-valenzuela/gabriel-valenzuela.github.io/blob/master/images/JLA-AVENGERS.jpg)

### Objective

With this data set, I am proposing that it be analyzed to determine the characteristics of future characters within both DC and Marvel Comics. At the same time, to better understand the distribution of the demographics within these characters and 
the underrepresented. The formal research questions are as follows:

What are the typical demographics of the most recent characters in DC and Marvel comics?

Is there a change in trend for certain demographics of characters?

Based on characteristics of past characters throughout the years, can you predict the next type of character in either a Marvel or DC comic?

When it comes to this data set, it allowed for an individual to sort throughout all of the characteristics, appearances of different characters throughout the DC and Marvel Comics, and the distribution of different trends of underrepresented people to see future possibilities of characters in seventy year industry of comics. With determining the possibility of certain characters in the future, the data sets will allow us to also understand character differences between the two major hero creators in the industry.  

### Data Source

https://www.kaggle.com/danoozy44/comic-characters

### Methodology

Random Forest Classifier (Preview of Model)

To see entire code for analysis, look into project folder.

```python
#train the mdodel
X_train, X_test, y_train, y_test = train_test_split(marvel_df_ip_scaled_ftrs, marvel_df_ip[response], test_size=0.30)

# Create and fir Decision Tree Model
model = DecisionTreeClassifier()
model.fit(X_train, y_train)

# Predicition of model
y_pred = model.predict(X_test)

# Accuracy of Model
accuracy = np.mean(cross_val_score(model, X_test, y_test, scoring='accuracy')) * 100
print("Accuracy: {}%".format(accuracy))

```


### Conclusion

Even though there is a high percentage towards certain aspects such as male, alive, and secret identity, there is a possibility of characters having different traits depending on the trends within the past decade or so. Because of the golden age of comics, there was a massive boom of characters that generally had the same characteristics both good and bad where characters were not killed and continued reappear on a repetitive basis. Therefore, from this analysis, I think it will provide an insight and future predictions of characters to not only understand DC and Marvel, but the attitude of the current society since comics like to mirror the culture and its audience. Based on this analysis of the characters and the history of superhero comics, we will be begin to see characters that represent the newest generation of readers to better connect with the stories being told with the villains being re-imagined to include different genders, sexes, and other characteristics that we saw from this dataset of both comic creators. 
