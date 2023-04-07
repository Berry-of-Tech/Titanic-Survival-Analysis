# Titanic-Survival-Analysis

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/titanic%20image%20WEBP.webp)

## 1. INTRODUCTION

Titanic was a British passenger liner, operated by the White Star Line, which sank in the North Atlantic Ocean on 15 April 1912 after striking an iceberg during her maiden voyage from Southampton, England, to New York City, United States. Of the estimated 2,224 passengers and crew aboard, more than 1,500 died, making it the deadliest commercial peacetime maritime disasters in modern history.

> The tool used for this project was Microsoft Excel

---

## 2. PROBLEM STATEMENT

The main objective of the analysis is to find the survival status of passengers on board the Titanic using various features, including age, gender, ticket class, and other variables. The dataset includes information on 1309 passengers, which is a subset of the total 2,224 passengers and crew members who were on board the Titanic.

---

## 3. THE DATASET

The Titanic dataset is a well-known dataset that contains information on 1309 passengers who were aboard the Titanic during its ill-fated maiden voyage. The dataset is widely used in the data science community as a benchmark dataset for classification modeling and predictive analysis.

This dataset for this study was obtained from data.world and can be downloaded from [Titanic dataset](https://data.world/nrippner/titanic-disaster-dataset)

**THE DATASET DETAILS**

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

---

**Pclass:** The Pclass column in the Titanic dataset was represented as numerical values, ranging from 1 to 3, corresponding to the different passenger classes on board the ship. I decided to convert these numerical values into their respective class names: ‘First Class’, ‘Second Class’, and ‘Third Class’ for easy understanding. I also renamed the ‘Pclass’ column to a more descriptive name that reflects its contents; ‘Passenger Class’.

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/P-class%20clean.webp)

Pclass column after cleaning.

---

**Survived:** The Survived column in the Titanic dataset indicates whether a passenger survived the sinking of the ship or not where '1' representing survival and '0' representing death. However, the column required some cleaning and reformatting to ensure consistency and accuracy in the data.

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Survived%20clean.webp)

Survived column after cleaning

---

**Name:** The Name column in the Titanic dataset contained the names of all passengers on board the ship. However, the names were split by delimiter to show only the fullname of the passengers.

Before and after cleaning the **Name** column

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Unclean%20Name%20column.webp)

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/clean%20full%20name.webp)

---

**Sex:** The Sex column in the Titanic dataset contained the gender of each passenger on board the ship. However, the column required some cleaning to ensure that all values were correctly labeled as **Male** or **Female**.

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Sex%20column%20after%20cleaning.webp)

Before cleaning the **sex** column

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Sex%20column%20after%20cleaning.png)

After cleaning the **Sex** column using the Proper() function

---

**Age:** The Age column in the Titanic dataset contained the age of each passenger on board the ship. First, I checked the datatype of the Age column and identify any missing values. After inspection. I noticed that the column contained several missing values, which I needed to complete before proceeding with any analysis.

Before and after cleaning the **Age** column

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/age%20before%20cleaning.webp)

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/age%20after%20cleaning.webp)

I also created the Age Bracket Column. The Age Bracket column in the Titanic dataset was a new column that was created to group passengers into different age categories. The aim of this column is to simplify our analysis and to make it easier to compare survival rates across different age groups on the dashboard.

To create the Age Bracket column, I used The **IF** statement to assign each passenger to the appropriate age group based on their age. For example, if a passenger’s age was between 0 and 18 years, I assigned them to the ‘Young’ age group, for those between 18 and 30 years, I assigned them to the ‘Young Adult’ group etc.

**Age Bracket column**

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Age%20bracket%20column.png)

---

**Parch and SibSp:** The Parch and SibSp columns in the Titanic dataset contained information about the number of parents/children and siblings/spouses that each passenger had onboard the ship. I decided to combine these two columns to create a new column called ‘Family Aboard’ using SUM() Function which would provide us with a more comprehensive understanding about family on board.

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/family%20aboard%20clean.webp)

I also created the **Family Detail** to know whether a passenger was traveling alone or with family. If a passenger had a family size of 0, I assigned the value ‘Alone’ to the ‘Family Detail’ column to indicate that they were traveling alone. For passengers with a family size greater than 0, I assigned the value ‘Family’ to the ‘Family Detail’ column to indicate that they were traveling with family.

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Family%20details.webp)

---

**Ticket:** The Ticket column in the Titanic dataset contained information about the ticket number of each passenger onboard the ship. It doesn't have any effect in the analysis, so i dropped it

---

**Fare:** The Fare column in the Titanic dataset contained information about the cost of each passenger’s ticket.

Before and after cleaning the Fare column

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/fare%20column%20before%20cleaning.webp)

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Clean%20Ticket%20Fare.png)

---

**Embarked:** The ‘Embarked’ column in the Titanic dataset contained information about the port of embarkation for each passenger.

Before and after cleaning the embarked column

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/embarked%20before%20cleaning.webp)

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/embarked%20after%20cleaning.webp)

I replaced these abbreviations with their corresponding port names by using find and replace tab.

Our new spalkling Titanic dataset

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Clean%20titanic%20dataset.png)



## 5. INSIGHTS

- Survival Rates by Gender: From the analysis, survival rates of passengers by gender showed that a higher proportion of females survived compared to males. Specifically, 67.80%% of females survived, while only 32.20%% of males survived.

- Survival Rates by Family Size: Further analysis showed the survival rates of passengers by family size. Passengers with family size had a higher survival rate compared to those with family members onboard or those with larger families. Specifically, passengers with family sizes had a survival rate of 52.2%, while passengers with no family members onboard had a survival rate of 47.80%.

- It's known that Ryerson Author Larned is the highest paying passenger with a fee of $524.75

This is what our Dashboard looks like

![](https://github.com/Berry-of-Tech/Titanic-Survival-Analysis/blob/main/Titanic%20Survival%20Dashboard.jpg)

## 6. CONCLUSION

My analysis of the Titanic dataset revealed that gender, passenger class, family size, and fare were significant factors in determining the survival of passengers onboard the Titanic. These findings provide valuable insights into the factors that influenced survival rates during the disaster. The cleaned and analyzed dataset can be used for further analysis and modeling to gain a deeper understanding of the Titanic disaster.

Thank you for reading!

You can reach me on:

- [LinkedIn](https://www.linkedin.com/in/alajede-mustapha-6071211a9/)
- [Twitter](https://twitter.com/Berry_Analyst)



