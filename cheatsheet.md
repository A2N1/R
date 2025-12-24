# R Cheat Sheet – COMPLETE LEARNING VERSION 📘 (R 4+)

This cheat sheet covers **core R concepts**, data types, vectors, data frames, functions, packages, and modern R features.  
Suitable for beginners and refreshers (Data Analysis / Statistics).

---

## Table of Contents

- [R Cheat Sheet – COMPLETE LEARNING VERSION 📘 (R 4+)](#r-cheat-sheet--complete-learning-version--r-4)
  - [Table of Contents](#table-of-contents)
  - [1. Basics](#1-basics)
  - [2. Variables \& Data Types](#2-variables--data-types)
  - [3. Operators](#3-operators)
  - [4. Control Structures](#4-control-structures)
  - [5. Functions](#5-functions)
  - [6. Vectors](#6-vectors)
  - [7. Lists](#7-lists)
  - [8. Matrices \& Arrays](#8-matrices--arrays)
  - [9. Data Frames](#9-data-frames)
  - [10. Factors](#10-factors)
  - [11. Packages \& Libraries](#11-packages--libraries)
  - [12. Apply Family](#12-apply-family)
  - [13. Plotting](#13-plotting)
  - [14. Statistical Functions](#14-statistical-functions)
  - [15. Strings \& Regular Expressions](#15-strings--regular-expressions)
  - [16. Dates \& Times](#16-dates--times)
  - [17. File I/O](#17-file-io)
  - [18. Modern R Features](#18-modern-r-features)
  - [19. Best Practices](#19-best-practices)
  - [End](#end)

---

## 1. Basics

~~~r
# Print
print("Hello World")
cat("Hello World\n")

# Comments
# single-line
# multi-line with multiple lines starting with #
~~~

---

## 2. Variables & Data Types

~~~r
# Assignment
x <- 10
y = 5

# Basic types
num <- 3.14       # numeric
int <- 5L         # integer
bool <- TRUE      # logical
text <- "R"       # character
null_val <- NULL  # null
na_val <- NA      # missing value
~~~

---

## 3. Operators

~~~r
# Arithmetic
5 + 3
5 - 3
5 * 3
5 / 2
5 %% 2     # modulo
5 ^ 2      # exponent

# Comparison
1 == 1
1 != 2
3 > 2

# Logical
TRUE & FALSE
TRUE | FALSE
!TRUE
~~~

---

## 4. Control Structures

~~~r
x <- 5

if (x > 0) {
  print("Positive")
} else if (x < 0) {
  print("Negative")
} else {
  print("Zero")
}

# Switch
role <- "admin"
switch(role,
       admin = print("Admin"),
       user = print("User"),
       print("Guest"))
~~~

---

## 5. Functions

~~~r
# Function definition
add <- function(a, b) {
  return(a + b)
}

greet <- function(name = "Guest") {
  paste("Hello", name)
}

# Anonymous function
sapply(1:5, function(x) x^2)
~~~

---

## 6. Vectors

~~~r
v <- c(1, 2, 3, 4)

# Access
v[1]       # first element
v[2:4]     # range

# Operations
v * 2
v + 1
v > 2
~~~

---

## 7. Lists

~~~r
lst <- list(name="Max", age=30, scores=c(90, 80, 70))
lst$name
lst$scores[2]
~~~

---

## 8. Matrices & Arrays

~~~r
# Matrix
m <- matrix(1:6, nrow=2, ncol=3)
m[1,2]      # row 1, column 2

# Array
a <- array(1:8, dim=c(2,2,2))
a[1,2,1]
~~~

---

## 9. Data Frames

~~~r
df <- data.frame(
  name = c("Max","Anna"),
  age = c(30,25),
  active = c(TRUE,FALSE)
)

df$name
df[1, "age"]
~~~

---

## 10. Factors

~~~r
gender <- factor(c("male","female","male"))
levels(gender)
table(gender)
~~~

---

## 11. Packages & Libraries

~~~r
# Install package
install.packages("dplyr")

# Load package
library(dplyr)
~~~

---

## 12. Apply Family

~~~r
# Apply over rows/columns
apply(matrix(1:6,2,3), 1, sum)
lapply(list(1,2,3), function(x) x^2)
sapply(list(1,2,3), function(x) x^2)
tapply(c(1,2,3,4), c("a","a","b","b"), sum)
~~~

---

## 13. Plotting

~~~r
# Base plot
x <- 1:10
y <- x^2
plot(x, y, type="b", col="blue", main="Plot", xlab="X-axis", ylab="Y-axis")

# Histogram
hist(x)
~~~

---

## 14. Statistical Functions

~~~r
mean(x)
median(x)
sd(x)
var(x)
summary(x)
cor(x, y)
~~~

---

## 15. Strings & Regular Expressions

~~~r
text <- "Hello R"

nchar(text)
toupper(text)
tolower(text)
substr(text, 1, 5)

grepl("R", text)
gsub("R", "World", text)
~~~

---

## 16. Dates & Times

~~~r
today <- Sys.Date()
now <- Sys.time()

format(today, "%Y-%m-%d")
as.Date("2025-12-24")
~~~

---

## 17. File I/O

~~~r
# Read CSV
data <- read.csv("data.csv")

# Write CSV
write.csv(data, "output.csv", row.names=FALSE)

# Read table
read.table("file.txt", header=TRUE)
~~~

---

## 18. Modern R Features

~~~r
# Pipes (magrittr or tidyverse)
library(dplyr)
data %>% filter(age > 20) %>% select(name, age)

# Tidyverse functions for concise data manipulation
~~~

---

## 19. Best Practices

- Use consistent style (tidyverse style guide)
- Comment your code
- Vectorize operations instead of loops
- Handle missing data carefully
- Use packages for efficient workflows
- Keep functions small and reusable
- Always check data types

---

## End
