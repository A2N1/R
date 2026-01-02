# Basic Commands
### Help & Documentation
- help(function)              # Show documentation for a function
- ?function                   # Shortcut for `help`
- help.search("topic")        # Search for functions on a topic
- args(function)              # See the arguments a function requires

### Workspace
- getwd()                     # Show the current working directory
- setwd("path")               # Change working directory
- ls()                        # Show objects in the workspace
- rm(object)                  # Remove an object
- rm(list = ls())             # Clear the workspace
- read.csv("file.csv")        # Import data from a CSV
- write.csv(df, "file.csv")   # Export data to a CSV
- saveRDS(obj, "file.rds")    # Save a single R object (efficient)
- readRDS("file.rds")         # Load a saved R object

### Packages
- install.packages("package") # Install a package
- library(package)            # Load a package
- update.packages()           # Update all installed packages

---

# Data Structures
### Vectors
- c(1, 2, 3)                  # Create a vector
- seq(1, 10, by = 2)          # Create a sequence
- rep(1, times = 5)           # Repeat elements
- length(vector)              # Length of a vector

### Matrices
- matrix(1:6, nrow = 2, ncol = 3) # Create a matrix
- t(matrix)                     # Transpose a matrix

### Lists
- list(a = 1, b = 2)           # Create a list

### Data Frames
- data.frame(a = 1:3, b = c("X", "Y", "Z")) # Create a data frame
- head(df)                     # Show the first few rows of a data frame
- tail(df)                     # Show the last few rows
- str(df)                      # Structure of a data frame
- summary(df)                  # Summary of a data frame

### Factors
- factor(c("A", "B", "A"))     # Create a factor
- levels(factor)               # Show levels of a factor

# Data Manipulation
### Indexing
- vector[2]                   # Access the second element of a vector
- matrix[1, 2]                # Access the element at row 1, column 2
- dataframe$column            # Access a column in a data frame

### Filtering
- subset(df, column > 10)     # Filter rows based on a condition

### Sorting
- sort(vector)                # Sort a vector
- order(df$column)            # Get sorted indices based on a column

### Merging
- merge(df1, df2, by = "column") # Merge two data frames by a common column

# Statistics & Calculations
### Basic Operations
- mean(vector)                # Calculate the mean
- median(vector)              # Calculate the median
- sd(vector)                  # Calculate the standard deviation
- sum(vector)                 # Sum of the elements

### Tables
- table(vector)               # Create a frequency table

### Random Numbers
- runif(10, min = 0, max = 1) # Generate random numbers from a uniform distribution
- rnorm(10, mean = 0, sd = 1) # Generate random numbers from a normal distribution

# Plotting & Visualization
### Basic Plots
- plot(x, y)                  # Create a scatter plot
- hist(vector)                # Create a histogram
- boxplot(vector)             # Create a box plot

### Labels & Titles
- plot(x, y, main = "Title", xlab = "X-Axis", ylab = "Y-Axis")

### Colors & Layout
- barplot(vector, col = "blue") # Create a bar plot with color

# Programming
### Loops
- for (i in 1:10) { print(i) }   # For loop
- while (condition) { ... }       # While loop

### Functions
- my_function <- function(x) { return(x^2) }  # Create a function
- my_function(2)                            # Call the function
