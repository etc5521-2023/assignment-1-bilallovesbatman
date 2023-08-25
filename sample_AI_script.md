# AI

## Q2

- Me: the wday variable has one spelling mistake for Wed as Wad in my cafe dataset. I am unable to find a way to fix that.

AI: # Assuming 'cafe' is your data frame
library(dplyr)

cafe <- cafe %>%
  mutate(wday = ifelse(wday == "Wad", "Wed", wday))
  
Here, we're using the mutate() function from the dplyr package to modify the "wday" column. The ifelse() function checks if the value is "Wad"; if it is, it replaces it with "Wed"; otherwise, it keeps the original value.

This approach should work regardless of whether the "wday" column is of character or factor type.

- Me: I made a boxplot from my cafe data. I want it to look more presentable. Please, help:

boxplot(cafe$revenue, cafe$expend, cafe$precip, cafe$mint, cafe$maxt)

AI: Certainly, you can enhance the presentation of your boxplot using various customization options available in R. Here's an example of how you can create a more presentable boxplot using the boxplot() function with improved aesthetics:

r
Copy code
# Assuming 'cafe' is your data frame
boxplot(cafe$revenue, cafe$expend, cafe$precip, cafe$mint, cafe$maxt,
        main = "Box Plots of Numeric Variables",
        names = c("Revenue", "Expend", "Precip", "Mint", "Maxt"),
        ylab = "Value",
        col = c("skyblue", "lightgreen", "lightcoral", "lightpink", "lightseagreen"),
        notch = TRUE,
        outline = FALSE,
        horizontal = TRUE,
        cex.axis = 0.8,
        cex.lab = 1.2)
In this example:

col sets the colors of the individual box plots.
notch enables notched boxes for improved comparison of medians.
outline specifies whether to show individual data points outside the whiskers.
horizontal rotates the box plots to be horizontal.
cex.axis adjusts the size of axis labels.
cex.lab adjusts the size of axis and title labels.
Feel free to customize these options further to match your preferences and the context of your presentation.




# Resources used

## Q2

- https://towardsdatascience.com/a-basic-guide-to-initial-and-exploratory-data-analysis-6d2577dfc242

- https://etav.github.io/articles/ida_eda_method.html

## Q3

- http://www.numbat.org.au/thenumbat#:~:text=During%20the%20hot%20summer%20months,sensitive%20to%20temperature%20and%20light.

