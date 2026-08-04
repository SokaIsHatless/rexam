# rexam
# Line Plot and scatter plot
temp <- c(23,25,25,26,27,28,30,26,29,32,33,34,35,38,39,42,43,44,45,45.5,45,46,44,44,41,37,40)
day  <- 1:27          # 1,2,3,...,27  — one x-value per temperature
#scatterlot
plot(day, temp,
     main = "Scatterplot of Temperature over 27 Days",
     xlab = "Day", ylab = "Temperature (°C)",
     col = "blue")

# pch = 19 means plotting character


# line plot

plot(day, temp,
     type = "l",
     main = "Line Plot of Temperature over 27 Days",
     xlab = "Day", ylab = "Temperature (°C)",
     col = "red", lwd = 2)


# format

plot(x, y,
     type = ,   # "p" points, "l" line, "b" both
     pch  = ,   # point shape (0–25)
     col  = ,   # colour
     lwd  = ,   # line thickness




## PIECHART AND BARCHART

# gender <- c(1,2,1,2,1,1,1,2,1,1,2,1,2,2,2,1,1,2,2,2,2,1,2,1,1,1,1,2,1)
counts = table(gender)
# barchart
barplot(counts,main="bar char of gender", xlab = 'gender',ylab='frequency',col = c('blue','pink'), 
        names.arg = c('boy', 'girl'))

# pie chart

pie(counts,
    main = "Pie Chart of Gender",
    labels = c("Male", "Female"),
    col = c("skyblue", "pink"))

# histogram
hist(gender, main=' histogram of gender')


#formulas
barplot(height,
        names.arg = ,   # labels under each bar
        col       = ,   # bar colours
        main      = ,   # chart title
        xlab      = ,   # x-axis label
        ylab      = ,   # y-axis label
        horiz     = )   # TRUE = horizontal bars (default FALSE)

pie(x,
    labels = ,   # text for each slice
    col    = ,   # slice colours
    main   = ,   # chart title
    radius = )   # size of the pie (−1 to 1, default 0.8)


hist(x,
     breaks = ,   # number of bins (or a rule/vector)
     col    = ,   # bar colour
     main   = ,   # title
     xlab   = ,   # x-axis label
     freq   = )   # TRUE = counts (default), FALSE = density
     main = ,   # title
     xlab = ,   # x-axis label
     ylab = )   # y-axis label

## MATH OPERATIONS

     x <- matrix( nrow=3 , ncol=3, data=c(1,2,3,4,5,6,7,8,9))
print(dim(x))   # prints the dimension of x 
print(mode(x))   # prints the type of data stored in x 
print(diag(x))   # prints the diagonal of x 
print(t(x))    #prints the transpose of x 

print( t(x)  %*% x)  # we use this for matrix multipliplication
print ( crossprod(x))   # this is the same as multiplying a matrix with its transpose


# b part matrix y

y <- matrix( nrow=3 , ncol=3, data=c(2,4,6,8,10,12,14,15,18))
print(y)
print(solve(x))  # prints inverse of y
#solve(y)
eigen(y)

a <- matrix(nrow=3 , ncol = 3, data = c(11:19))
print(a)
print(cbind(x,y))
print(x)
print(x[2,])  #prints 2nd row, here blank means all elements
# if we use a - sign in front of 2, it will delete that entire row




## CORRELATION

# Data
x <- c(10,20,30,40,50)
y <- c(15,25,35,45,55)

# Correlation
result <- cor(x,y)

# Display result
print(result)


## regression

# Input data
x <- c(10,20,30,40,50)
y <- c(15,25,35,45,55)

# Create regression model
model <- lm(y ~ x)

# Display regression model
model

# Summary of regression
summary(model)

# Plot the data
plot(x, y,
     main = "Linear Regression",
     xlab = "X values",
     ylab = "Y values",
     col = "blue",
     pch = 19)

# Draw regression line
abline(model, col = "red", lwd = 2)
