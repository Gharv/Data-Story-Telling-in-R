---
title       : Getting Started in R
description : Basic operations in R
---
## Question 3

```yaml
type: MultipleChoiceExercise
lang: r
xp: 50
skills: 1
key: d302313e72
```

Which of the following would not give help for the function `subset`?

`@instructions`
- ?subset
- help("subset")
- explain("subset")
- help(subset)

`@hint`
The quotes are options with the help functions.

`@pre_exercise_code`
```{r}
# The pre exercise code runs code to initialize the user's workspace.
# You can use it to load packages, initialize datasets and draw a plot in the viewer
```

`@sct`
```{r}
# SCT written with testwhat: https://github.com/datacamp/testwhat/wiki

msg_bad <- "That is not correct!"
msg_success <- "Exactly! That is correct!"
test_mc(correct = 3, feedback_msgs = c(msg_bad, msg_bad, msg_success, msg_bad))
```

---
## Question 4-6

```yaml
type: TabExercise
lang: r
xp: 100
skills: 1
key: 1a97476379
```

The next few exercises show R operations as a calculator. You can leave previous answers in the script of remove them, which ever you like.


***

```yaml
type: NormalExercise
xp: 30
key: bc4a2bbcc3
```

`@instructions`

What is the sum of 15 and 32?

`@pre_exercise_code`
```{r}
```

`@solution`

```{r}
15+32
```

`@sct`

```{r}
test_output_contains("47", incorrect_msg = "Did you use the + sign?")
success_msg("Great job!")
```

***

```yaml
type: NormalExercise
xp: 30
key: 41991a7e2c
```

`@instructions`

What is the product of 34 and 543?

`@solution`

```{r}
34*543
```

`@sct`

```{r}
test_output_contains("18462", incorrect_msg = "Did you use the * sign?")
success_msg("Great job!")
```

***

## Filter

```yaml
type: NormalExercise
xp: 30
key: 30b93ba90b
```

`@instructions`

What is 2 to the 4th?

`@solution`

```{r}
2^4
```

`@sct`

```{r}
test_output_contains("16", incorrect_msg = "Did you use the ^ sign?")
success_msg("Great job!")
```

---
## Question 7-10
```yaml
type: TabExercise
lang: r
xp: 100
skills: 1
key: 7d047bdbba
```

The next few exercises show how to create vectors. You can leave previous vectors in the script file or remove them.


***

```yaml
type: NormalExercise
xp: 30
key: 02e4519ff9
```

`@instructions`
Create a vector of the numbers 3,8,4,2 and give it the name A.

`@solution`
```{r}
A <- c(3,8,4,2)
```

`@sct`
```{r}
test_object("A")
success_msg("Great job!")
```

***

```yaml
type: NormalExercise
xp: 30
key: 7c70b4fc74
```

`@instructions`
Create a vector of the characters monkey, rat, snake, and give it the name B.

`@solution`
```{r}
B <- c("monkey","rat","snake")
```

`@sct`
```{r}
test_object("B")
success_msg("Great job!")
```

***

```yaml
type: NormalExercise
xp: 30
key: 685d270736
```

`@instructions`
Create a vector of the sequence of numbers between 89 and 143, and give it the name C.

`@solution`
```{r}
C <- seq(89,143)
```

`@sct`
```{r}
test_object("C")
success_msg("Great job!")
```

***


```yaml
type: NormalExercise
xp: 30
key: 06da48b049
```

`@instructions`
Create a vector containing 15 of the number 3 - use the `rep` command, and give it the name D.

`@solution`
```{r}
D <- rep(3,15)
```

`@sct`
```{r}
test_object("D")
success_msg("Great job!")
```
---
## Question 11
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 3d04e59d32
```

`@instructions`
What is the 3rd element in the vector A?

`@pre_exercise_code`
```{r}
A <- c(3,8,4,2)
B <- c("monkey", "rat", "snake")
C <- seq(89,143)
D <- rep(3,15)
```

`@solution`
```{r}
A[3]
```

`@sct`
```{r}
test_output_contains("A[3]")
success_msg("Great job!")
```
---
## Question 12
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: aa3b8ca8ac
```

`@instructions`
What are the last two elements of the vector B?

`@pre_exercise_code`
```{r}
A <- c(3,8,4,2)
B <- c("monkey", "rat", "snake")
C <- seq(89,143)
D <- rep(3,15)
```

`@solution`
```{r}
B[2:3]
```

`@sct`
```{r}
test_output_contains("B[2:3]")
success_msg("Great job!")
```
---
## Question 13
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: '1604e01848'
```

`@instructions`
What is the 4th and 30th element in the vector C?

`@pre_exercise_code`
```{r}
A <- c(3,8,4,2)
B <- c("monkey", "rat", "snake")
C <- seq(89,143)
D <- rep(3,15)
```

`@solution`
```{r}
C[c(4,30)]
```

`@sct`
```{r}
test_output_contains("C[c(4,30)]")
success_msg("Great job!")
```
---
## Question 14
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: d3f2d560ce
```

`@instructions`
What is the sum of all of the elements in the vector D?

`@pre_exercise_code`
```{r}
A <- c(3,8,4,2)
B <- c("monkey", "rat", "snake")
C <- seq(89,143)
D <- rep(3,15)
```

`@solution`
```{r}
sum(D)
```

`@sct`
```{r}
test_output_contains("sum(D)")
success_msg("Great job!")
```

---
## Question 15
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 3fa0c07dad
```

`@instructions`
Add the character "bird" to the end of vector B.

`@pre_exercise_code`
```{r}
B <- c("monkey","rat","snake")
```

`@solution`
```{r}
B[4] <- "bird"
```

`@sct`
```{r}
test_object("B")
success_msg("Great job!")
```

---
## Question 16
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: '9239851366'
```

`@instructions`
Change the first element in vector D to the number 5.

`@pre_exercise_code`
```{r}
D <- rep(3,15)
```

`@solution`
```{r}
D[1] <- 5
```

`@sct`
```{r}
test_object("D")
success_msg("Great job!")
```

---
## Question 17
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 748c21e2e1
```

`@instructions`
Multiple vector A by 3 and save the results as vector A2.

`@pre_exercise_code`
```{r}
A <- c(3,8,4,2)
```

`@solution`
```{r}
A2 <- A*3
```

`@sct`
```{r}
test_object("A2")
success_msg("Great job!")
```

---
## Question 18
```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: 65474b7e80
```

`@instructions`
Add 5 to every element of vector C and save the results as vector C2.

`@pre_exercise_code`
```{r}
C <- seq(89,143)
```

`@solution`
```{r}
C2 <- C+5
```

`@sct`
```{r}
test_object("C2")
success_msg("Great job!")
```