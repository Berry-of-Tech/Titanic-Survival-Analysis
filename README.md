# Titanic-Survival-Analysis

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Titanic%20image.jpg)

## 1. INTRODUCTION

The Titanic was a British luxury passenger liner that was built in 1912 and owned by the White Star Line. It was one of the largest and most opulent ships of its time, measuring 882 feet in length and weighing 46,328 gross tons. The Titanic was designed to carry up to 3,547 passengers and crew and boasted state-of-the-art amenities such as a swimming pool, gym, Turkish bath, and squash court. Tragically, the Titanic sank on its maiden voyage from Southampton, England, to New York City after striking an iceberg in the North Atlantic Ocean on April 14, 1912. The disaster resulted in the loss of over 1,500 lives, making it one of the deadliest commercial peacetime maritime disasters in modern history.

> The tool use for this project was Microsoft Excel

---

## 2. PROBLEM STATEMENT

The main objective of the analysis is to predict the survival status of passengers on board the Titanic using various features, including age, gender, ticket class, and other variables. The dataset includes information on 1309 passengers, which is a subset of the total 2,224 passengers and crew members who were on board the Titanic. The problem statement of the dataset is important because it provides insight into the factors that influenced passenger survival rates during the Titanic disaster.

---

## 3. THE DATASET

The Titanic dataset is a well-known dataset that contains information on 1309 passengers who were aboard the Titanic during its ill-fated maiden voyage. The dataset is widely used in the data science community as a benchmark dataset for classification modeling and predictive analysis.

This dataset for this study was obtained from data.world and can be downloaded from [Titanic dataset](https://data.world/nrippner/titanic-disaster-dataset)

THE DATASET DETAILS

1. survival — Survival (0 = No; 1 = Yes)
2. class — Passenger Class (1 = 1st; 2 = 2nd; 3 = 3rd)
3. name — Name
4. sex — Sex
5. age — Age
6. sibsp — Number of Siblings/Spouses Aboard
7. parch — Number of Parents/Children Aboard
8. ticket — Ticket Number
9. fare — Passenger Fare
10.cabin — Cabin
11. embarked — Port of Embarkation (C = Cherbourg; Q = Queenstown; S = Southampton)
12. boat — Lifeboat (if survived)
13. body — Body number (if did not survive and body was recovered)
14. home_dest — Destination

---

## 4. DATA CLEANING PROCESS

Before commencing the cleaning process, the data was imported into Microsoft Excel and it showed the raw data.

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Titanic%20unclean%20data.webp)

**Pclass:** The Pclass column in the Titanic dataset was originally represented as numerical values, ranging from 1 to 3, corresponding to the different passenger classes on board the ship. To make the data more interpretable, I decided to convert these numerical values into their respective class names: ‘First Class’, ‘Second Class’, and ‘Third Class’. I also renamed the ‘Pclass’ column to a more descriptive name that reflects its contents; ‘Passenger Class’.

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/P-class%20clean.webp)

Pclass column after cleaning

By converting the ‘Pclass’ values to their respective class names, I was able to create a more readable and intuitive dataset that could be easily understood by others.

**Survived:** The Survived column in the Titanic dataset indicates whether a passenger survived the sinking of the ship or not, with 1 representing survival and 0 representing death. However, the column required some cleaning and reformatting to ensure consistency and accuracy in the data.

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Survived%20clean.webp)

Survived column after cleaning

**Name:** The Name column in the Titanic dataset contained the names of all passengers on board the ship. However, the names were formatted in a way that required some cleaning and reformatting to extract useful information from the column.

Before and after cleaning the **Name** column 
![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Unclean%20Name%20column.webp)

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/clean%20full%20name.webp)

Sex: The ‘Sex’ column in the Titanic dataset contained the gender of each passenger on board the ship. However, the column required some cleaning to ensure that all values were correctly labeled as ‘Male’ or ‘Female’.

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Sex%20column%20after%20cleaning.webp)

after cleaning the **Sex** column

By cleaning the ‘Sex’ column, I was able to ensure that all values were consistently labeled, which is essential for accurate analysis and interpretation of the data.

**Age:** The Age column in the Titanic dataset contained the age of each passenger on board the ship. First, I inspected the ‘Age’ column to identify any missing or erroneous values. After inspection. I noticed that the column contained several missing values, which we needed to address before proceeding with any analysis.

Before and after cleaning the **Age** column

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/age%20before%20cleaning.webp)

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/age%20after%20cleaning.webp)

I also created the Age Group Column. The Age Bracket column in the Titanic dataset was a new column that was created to group passengers into different age categories. The aim of this column is to simplify our analysis and to make it easier to compare survival rates across different age groups.

To create the Age Bracket column, I used Excel’s ‘IF’ function to assign each passenger to the appropriate age group based on their age. For example, if a passenger’s age was between 0 and 18 years, I assigned them to the ‘Young’ age group, for those between 18 and 35 years, I assigned them to the ‘Young Adult’ group etc.

By creating the Age Bracket column, I was able to simplify our analysis and compare survival rates across different age groups. This is essential for identifying patterns and trends in the data and for drawing meaningful conclusions.

Age Bracket column

![]()

**Parch and SibSp:** The Parch and SibSp columns in the Titanic dataset contained information about the number of parents/children and siblings/spouses that each passenger had onboard the ship. I decided to combine these two columns to create a new column called ‘Family Aboard’ using SUM() Function which would provide us with a more comprehensive understanding of each passenger’s family situation.

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/family%20aboard%20clean.webp)

After creating the ‘Family Aboard’ column, I decided to create a new column called ‘Family Detail’, which would indicate whether a passenger was traveling alone or with family. If a passenger had a family size of 0, we assigned the value ‘Alone’ to the ‘Family Detail’ column to indicate that they were traveling alone. For passengers with a family size greater than 0, I assigned the value ‘Family’ to the ‘Family Detail’ column to indicate that they were traveling with family.

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Family%20details.webp)

**Ticket:** The Ticket column in the Titanic dataset contained information about the ticket number of each passenger onboard the ship. It doesn't have any effect in the analysis, so i dropped it

**Fare:** The ‘Fare’ column in the Titanic dataset contained information about the cost of each passenger’s ticket.

Before and after cleaning the Fare column

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/fare%20column%20before%20cleaning.webp)

![]()

**Embarked:** The ‘Embarked’ column in the Titanic dataset contained information about the port of embarkation for each passenger.

Before and after cleaning the embarked column

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/embarked%20before%20cleaning.webp)

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/embarked%20after%20cleaning.webp)

I replace these abbreviations with their corresponding port names by using find and replace tab.


![]()

Our new spalkling Titanic dataset

## 5. INSIGHTS

Survival Rates by Gender: From the analysis, survival rates of passengers by gender showed that a higher proportion of females survived compared to males. Specifically, 67.80%% of females survived, while only 32.20%% of males survived.

Survival Rates by Passenger Class: I also analyzed the survival rates of passengers by passenger class and found out that first-class passengers had the highest survival rate, followed by second-class passengers and third-class passengers. Specifically, 61.92% of first-class passengers survived, while only 25.53% of third-class passengers survived.

Survival Rates by Family Size: Further analysis showed the survival rates of passengers by family size. Passengers with family sizes of 1–4 had a higher survival rate compared to those with no family members onboard or those with larger families. Specifically, passengers with family sizes of 1–4 had a survival rate of 49.6%, while passengers with no family members onboard had a survival rate of 47.80%.

This is what our Dashboard looks like

![]()

## 6. CONCLUSION

My analysis of the Titanic dataset revealed that gender, passenger class, family size, and fare were significant factors in determining the survival of passengers onboard the Titanic. These findings provide valuable insights into the factors that influenced survival rates during the disaster. The cleaned and analyzed dataset can be used for further analysis and modeling to gain a deeper understanding of the Titanic disaster.

Thank you for reading!

You can reach me on:

- [LinkedIn](https://www.linkedin.com/in/alajede-mustapha-6071211a9/)
- [Twitter](https://twitter.com/Berry_Analyst)



