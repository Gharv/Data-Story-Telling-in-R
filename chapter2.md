---
title       : Basic Data Management in R
description : Introduction to data management in R
---
## Question 19-20

```yaml
type: MultipleChoiceExercise
lang: r
xp: 50
skills: 1
key: b52c9b6065
```

How would you import the 'lionCrater' file into R and save it as a dataframe named `lion`.

`@instructions`
- lion <- import("lionCrater.csv")
- lion <- read.csv("lionCrater.csv")
- lion <- read.csv("lionCrater")
- lion <- import("lionCrater")

`@hint`


`@pre_exercise_code`
```{r}
# The pre exercise code runs code to initialize the user's workspace.
# You can use it to load packages, initialize datasets and draw a plot in the viewer
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@sct`
```{r}
# SCT written with testwhat: https://github.com/datacamp/testwhat/wiki

msg_bad <- "That is not correct!"
msg_success <- "Exactly! That is correct!"
test_mc(correct = 2, feedback_msgs = c(msg_bad, msg_success, msg_bad, msg_bad))
```

---
## Question 21
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: '8286898109'
```

`@instructions`
Display the structure of the `lion` data frame.

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
```

`@solution`
```{r}
str(lion)
```

`@sct`
```{r}
test_function("str")
success_msg("Great job!")
```

---
## Question 22
```yaml
type: MultipleChoiceExercise
lang: r
xp: 100
skills: 1
key: 5a12104ef1
```

Which of the following are not ways to display the data in column 1 of the `lion` data frame?

`@instructions`
- lion[1]
- lion["Year"]
- lion$Year
- lion$1

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
```

`@sct`
```{r}
# SCT written with testwhat: https://github.com/datacamp/testwhat/wiki

msg_bad <- "That is not correct!"
msg_success <- "Exactly! That is correct!"
test_mc(correct = 4, feedback_msgs = c(msg_bad, msg_bad, msg_bad, msg_success))
```
---
## Question 23
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 149ed4c1cc
```

`@instructions`
How do you access the 5th row of data in the `lion` data frame?

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
```

`@solution`
```{r}
lion[5,]
```

`@sct`
```{r}
test_output_contains("lion[5,]")
success_msg("Great job!")
```
---
## Question 24
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: '7613493535'
```

`@instructions`
Display the first 6 rows of the `rhino` data frame.

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@solution`
```{r}
head(rhino)
```

`@hint`
Use the `head` function

`@sct`
```{r}
test_output_contains("head(rhino)")
success_msg("Great job!")
```
---
## Question 25
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 1cdf2ff2d4
```

`@instructions`
Display the last 6 rows of the `rhino` data frame.

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@solution`
```{r}
tail(rhino)
```

`@hint`
Use the `tail` function

`@sct`
```{r}
test_output_contains("tail(rhino)")
success_msg("Great job!")
```
---
## Question 26
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: '57432426e4'
```

`@instructions`
How many rows are in the `rhino` data frame?

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@solution`
```{r}
nrow(rhino)
```

`@hint`
Use the `nrow` function

`@sct`
```{r}
test_output_contains("nrow(rhino)")
success_msg("Great job!")
```
---
## Question 27
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 2ad69fcc4e
```

`@instructions`
How many columns are in the `rhino` data frame?

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@solution`
```{r}
ncol(rhino)
```

`@hint`
Use the `ncol` function

`@sct`
```{r}
test_output_contains("ncol(rhino)")
success_msg("Great job!")
```
---
## Question 28
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 4a857e995e
```

`@instructions`
Look at the Year column for both `lion` and `rhino`. Which years overlap?
Create two new data frames `lion2` and `rhino2` that only contain the overlapping years.

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@solution`
```{r}
lion2 <- subset(lion, lion$Year > 1979)
rhino2 <- subset(rhino, rhino$Year < 1993)
```

`@hint`
Use `subset` and the `>` and `<` operators on the `Year` columns of each data frame. 

`@sct`
```{r}
test_object("lion2")
test_object("rhino2")
success_msg("Great job!")
```
---
## Question 29
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: '43922e3161'
```

`@instructions`
Create a new data frame called `lion3` that only contains the years when the population is over 50 individuals. 

How many rows are in this new data frame using an R function?

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@solution`
```{r}
lion3 <- subset(lion, lion$Population > 50)
nrow(lion3)
```

`@hint`
Use `subset` and the `>` and `<` operators on the `Population`.
Use `nrow` to find number of rows.

`@sct`
```{r}
test_object("lion3", incorrect_msg = "Make sure you created the object `lion3`, use the hint if necessary.")
test_output_contains("nrow(lion3)", incorrect_msg = "Did you find the number or rows in `lion3`?")
success_msg("Great job!")
```
---
## Question 30
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: fc1458c516
```

`@instructions`
Create a new data frame called `rhino3` that only contains the years when the population of rhinos is less than 12 individuals. 

How many rows are in this new data frame?

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@solution`
```{r}
rhino3 <- subset(rhino, rhino$Population < 12)
nrow(rhino3)
```

`@hint`
Use `subset` and the `>` and `<` operators on the `Population`.
Use `nrow` to find number of rows.

`@sct`
```{r}
test_object("rhino3", incorrect_msg = "Make sure you created the object `rhino3`, use the hint if necessary.")
test_output_contains("nrow(rhino3)", incorrect_msg = "Did you find the number or rows in `rhino3`?")
success_msg("Great job!")
```