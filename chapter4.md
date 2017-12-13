---
title       : Basic Visulization
description : Basic visulization with graphs and plots in R
---
## Question 8 part 1
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 7593223698
```
`@instructions`
Create a plot of the lion population size with the year on the x-axis. Include a title, axis labels.

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@hint`


`@solution`
```{r}
plot(lion$Year, lion$Population, main="Lion Population", xlab="Year", ylab="Population")
```

`@sct`
```{r}
test_function("plot", args = c("x","y","main","xlab","ylab"))
success_msg("Great job!")
```
---
## Question 9 part 1
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: c335fd0004
```

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@instructions`
Create a plot of the black rhino population size with the year on the x-axis.

This time make it a line plot. Include a title, axis labels, and the make the line dark green. 

Use the parameter `lty=2` in the `plot` function to make the line dashed. You still need the parameter to make it a line graph.


`@hint`


`@solution`
```{r}
plot(rhino$Year, rhino$Population, main="Rhino Population", xlab="Year", ylab="Population", col="darkgreen", type="l", lty=2)
```

`@sct`
```{r}
test_function("plot", args = c("x","y","main","xlab","ylab","col","type","lty"))
success_msg("Great job!")
```


---
## Question 8 part 2
```yaml
type: MultipleChoiceExercise
lang: r
xp: 100
skills: 1
key: 13034ece3e
```
Is the `lion` population increasing or decreasing?

`@instructions`
- Constant
- Only decreasing
- Increasing then decreasing
- Only increasing
- Decreasing then increasing

`@hint`

`@pre_exercise_code`
```{r}
# The pre exercise code runs code to initialize the user's workspace.
# You can use it to load packages, initialize datasets and draw a plot in the viewer
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
plot(lion$Year, lion$Population, main="Lion Population", xlab="Year", ylab="Population")
plot(rhino$Year, rhino$Population, main="Rhino Population", xlab="Year", ylab="Population", col="darkgreen", type="l", lty=2)
```

`@sct`
```{r}
# SCT written with testwhat: https://github.com/datacamp/testwhat/wiki

msg_bad <- "That is not correct!"
msg_success <- "Exactly! That is correct!"
test_mc(correct = 3, feedback_msgs = c(msg_bad, msg_bad, msg_success, msg_bad, msg_bad))
```
---
## Question 9 part 2
```yaml
type: MultipleChoiceExercise
lang: r
xp: 100
skills: 1
key: af4d6bc1d4
```
Is the `rhino` population increasing or decreasing?

`@instructions`
- Constant
- Only decreasing
- Increasing then decreasing
- Only increasing
- Decreasing then increasing

`@hint`

`@pre_exercise_code`
```{r}
# The pre exercise code runs code to initialize the user's workspace.
# You can use it to load packages, initialize datasets and draw a plot in the viewer
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
plot(lion$Year, lion$Population, main="Lion Population", xlab="Year", ylab="Population")
plot(rhino$Year, rhino$Population, main="Rhino Population", xlab="Year", ylab="Population", col="darkgreen", type="l", lty=2)
```

`@sct`
```{r}
# SCT written with testwhat: https://github.com/datacamp/testwhat/wiki

msg_bad <- "That is not correct!"
msg_success <- "Exactly! That is correct!"
test_mc(correct = 5, feedback_msgs = c(msg_bad, msg_bad, msg_bad, msg_bad, msg_success))
```
---
## Question 10 part 1
```yaml
type: MultipleChoiceExercise
lang: r
xp: 100
skills: 1
key: 57aaa8b131
```
Looking at the two plots on the right how would you describe their relationship?

`@instructions`
- Direct
- Inverse
`@hint`

`@pre_exercise_code`
```{r}
# The pre exercise code runs code to initialize the user's workspace.
# You can use it to load packages, initialize datasets and draw a plot in the viewer
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
plot(lion$Year, lion$Population, main="Lion Population", xlab="Year", ylab="Population")
plot(rhino$Year, rhino$Population, main="Rhino Population", xlab="Year", ylab="Population", col="darkgreen", type="l", lty=2)
```

`@sct`
```{r}
# SCT written with testwhat: https://github.com/datacamp/testwhat/wiki

msg_bad <- "That is not correct!"
msg_success <- "Exactly! That is correct!"
test_mc(correct = 2, feedback_msgs = c(msg_bad, msg_success))
```
---
## Question 10 part 2
```yaml
type: MultipleChoiceExercise
lang: r
xp: 100
skills: 1
key: c88cbaad1c
```
What is a way in which we could put the two plots onto one page with one column and two rows?

`@instructions`
- use `par(mfrow=c(2,1))` followed by the plot functions.
- use `par(mfrow=c(1,2))` followed by the plot functions.
- use `par(mfrow=c(1,2))` after using the plot functions.
- use `par(mfrow=c(2,1))` after using the plot functions.
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
test_mc(correct = 1, feedback_msgs = c(msg_success, msg_bad, msg_bad, msg_bad))
```
---
## Question 11-13
```yaml
type: TabExercise
lang: r
xp: 100
skills: 1
key: 4a857e995e
```
`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
lion2 <- subset(lion, lion$Year > 1979)
rhino2 <- subset(rhino, rhino$Year < 1993)
```

***
```yaml
type: NormalExercise
xp: 30
key: 679165b49a
```

`@instructions`
Create two new data frames `lion2` and `rhino2` that contain the subset of years that overlap between the two datasets (like we did in the last assignment). These new datasets will be used for the next plot.


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
***
```yaml
type: NormalExercise
xp: 30
key: bf086dec14
```


`@instructions`
Create a line plot of the lion population sizes. On the same plot add the black rhino population sizes as points. Make the lion population line purple and the black rhino population points red. Includes a title and axis labels. You will need to set the limits of the y-axis from (0,100) otherwise the rhino points will not be visible when you add them to the plot.


`@hint`


`@solution`
```{r}
plot(lion2$Year, lion2$Population, type = "l", col = "purple", main = "Lion and Black Rhino Population", xlab = "Year", ylab = "Population", ylim = c(0,100))
points(rhino2$Year, rhino2$Population, col = "red")
```

`@sct`
```{r}
test_function("plot", args = c("x","y","main","xlab","ylab","col","type","ylim"))
test_function("points", args = c("x","y","col"))
success_msg("Great job!")
```

***
```yaml
type: NormalExercise
xp: 30
key: 1b336c48fe
```
`@instructions`
Add a legend to the top right of the plot you just made – make sure next to lion you have a purple line, and next to black rhino you have a red point.

You will need to leave the `plot` and `points` above this `legend` function for it to properly work.

`@hint`


`@solution`
```{r}
plot(lion2$Year, lion2$Population, type = "l", col = "purple", main = "Lion and Black Rhino Population", xlab = "Year", ylab = "Population", ylim = c(0,100))
points(rhino2$Year, rhino2$Population, col = "red")
legend("topright", legend = c("Lion", "Black Rhino"), col = c("purple", "red"), lty = c(1,NA), pch = c(NA,1))
```

`@sct`
```{r}
test_function("legend", args = c("x","legend","col","lty","pch"))
success_msg("Great job!")
```
---
## Question 14
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: d6724df295
```

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@instructions`
Create a barplot showing the minimum population size for black rhino and lion. 

Label the bars Lion and Rhino. Use the name `data` when creating a data frame.


`@hint`
Make a dataframe with the column names "Lion" and "Rhino" with the values containing the min values of their populations.

`@solution`
```{r}
data <- c(min(lion$Population), min(rhino$Population))
names(data) <- c("Lion", "Rhino")
barplot(data)
```

`@sct`
```{r}
test_data_frame("data", columns = c("Lion", "Rhino"))
test_function("barplot", args = "height")
success_msg("Great job!")
```
---
## Question 15
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 11ecb98d77
```

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@instructions`
Create a side-by-side boxplot of the population size for lions and black rhinos – make sure to include a title, and a label below each box to show which animal it represents.


`@hint`

`@solution`
```{r}
boxplot(lion$Population, rhino$Population, names = c("Lion", "Rhino"), main = "Population Sizes")
```

`@sct`
```{r}
test_function("boxplot", args = c("x", "names", "main"))
test_error()
success_msg("Great job!")
```
---
## Question 16
```yaml
type: TabExercise
lang: r
xp: 100
skills: 1
key: ff95841c81
```

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

***
```yaml
type: NormalExercise
xp: 30
key: b51f558984
```

`@instructions`
Create a histogram of the population size for black rhinos.


`@hint`

`@solution`
```{r}
hist(rhino$Population, main = "Rhino Population Sizes", xlab = "Population Size")
```

`@sct`
```{r}
test_function("hist", args = c("x", "xlab", "main"))
test_error()
success_msg("Great job!")
```

***
```yaml
type: NormalExercise
xp: 30
key: 60ee263ba7
```

`@instructions`
Add an orange vertical line to show the mean population size.


`@hint`

`@solution`
```{r}
hist(rhino$Population, main = "Rhino Population Sizes", xlab = "Population Size")
abline(v=mean(rhino$Population), col = "orange")
```

`@sct`
```{r}
test_function("hist", args = c("x", "xlab", "main"))
test_function("abline", args = c("v", "col"))
test_error()
success_msg("Great job!")
```