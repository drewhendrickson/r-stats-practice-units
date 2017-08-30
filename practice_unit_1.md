# Practice Unit 1

Background reading is Chapter 3 and 4 in the LSR textbook.

## Loading Data

First let's load some data from a comma-separated-value file. We are going to use a function called `read.csv` This is also covered in Section 4.5 in the LSR textbook.

```R
data <- read.csv("sample_data.csv", stringsAsFactors = FALSE)
```

## Inspecting data types

```R
data <- read.csv("sample_data.csv", stringsAsFactors = FALSE)
```

## Inspecting the data

Finally, let's take a look at the first few entries in our dataset. We will use the function `head` which shows the first N rows of the dataframe.

```R
head(data)
```

We could also use the `tail` function that shows the last N rows:

```R
tail(data)
```

## Saving the data

R gives us many ways to save data. `save.image()` is a function that will save all of your variables to a single file. `save()` will save one or more variables to a file. We can also use `write.csv()` or `write.txt()` to write csv or text files that can be read by other programs (SPSS, excel, python, etc.).

Let's save our file as an rData file:

```R
save(data, file = "sample_data.Rdata")
```

## Variable names

We can print out the names of all the variables in our dataframe:

```R
names(data)
```

And interestingly we can save the list of names into a variable:

```R
my_names <- names(data)
my_names
```

Finally, we can change a value of `my_names` and then update the names in our dataframe:

```R
my_names[3] <- "awesome_person"
names(data) # these shouldn't have changed yet
names(data) <- my_names
names(data) # now they should be updated
```
