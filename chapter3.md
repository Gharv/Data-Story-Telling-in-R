---
title       : Descriptive Statistics
description : Basic statistics
---
## Question 2
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 3d04e59d32
```

`@instructions`
What is the minimum and maximum population size for lions?

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@hint`
Use the `min` and `max` functions.

`@solution`
```{r}
min(lion$Population)
max(lion$Population)
```

`@sct`
```{r}
test_output_contains("min(lion$Population)")
test_output_contains("max(lion$Population)")
success_msg("Great job!")
```
---
## Question 3
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 6df8d8ee36
```

`@instructions`
What is the mean, median, and standard deviation of the population size of lions?

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@hint`
Use the `mean`, `median` and `sd` functions.

`@solution`
```{r}
mean(lion$Population)
median(lion$Population)
sd(lion$Population)
```

`@sct`
```{r}
test_output_contains("mean(lion$Population)")
test_output_contains("median(lion$Population)")
test_output_contains("sd(lion$Population)")
success_msg("Great job!")
```

---
## Question 5
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: d8aa660933
```

`@instructions`
What are the quantile (0%,25%,50%,75%,100%) population sizes for black rhinos?

`@pre_exercise_code`
```{r}
lion <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/lionCrater.csv")
rhino <- read.csv("https://raw.githubusercontent.com/Gharv/Questions/master/blackRhinoCrater.csv")
```

`@hint`
Use the `quantile` function.

`@solution`
```{r}
quantile(rhino$Population)
```

`@sct`
```{r}
test_output_contains("quantile(rhino$Population)")
success_msg("Great job!")
```
---
## Question 6-7

```yaml
type: MultipleChoiceExercise
lang: r
xp: 50
skills: 1
key: d302313e72
```

Which descriptive statistic is not displayed with the `summary` function

`@instructions`
- 0% Quantile
- Mean
- 75% Quantile
- Standard Deviation
- Max

`@hint`
0% quantile is equivalent to the minimum as is the 100% quantile and the maximum.

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
test_mc(correct = 4, feedback_msgs = c(msg_bad, msg_bad, msg_bad, msg_success, msg_bad))
```