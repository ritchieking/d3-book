Appendix B: Cleaning the Population Distribution Data
==========

##Files

Name | Description
---|---------
`WPP2015_POP_F07_1_POPULATION_BY_AGE_BOTH_SEXES.XLS` | Raw global population projections from the UN Population Division. This is the raw data used to make the example age distribution bar chart in the book.

##More Information

The file in this directory is a Microsoft Excel file. You can dowload it by [clicking here](https://github.com/ritchieking/d3-book/blob/master/Appendix%20B/WPP2015_POP_F07_1_POPULATION_BY_AGE_BOTH_SEXES.XLS?raw=true).

The data cleaning steps that this chapter takes you through require two pieces of free software:

1. [Open Office](https://www.openoffice.org/)
2. [R](http://cran.r-project.org/)

Here is the R code that you have to use to transform the data into the form required for the bar chart:

    # Install and load the reshape2 package
    install.packages("reshape2")
    require("reshape2")

    # Set the working directory to the folder where your
    # CSV file is. For example:
    # setwd("/Users/ritchieking/Desktop")
    setwd("")

    # Pull in the data
    data <- read.csv("rawData.csv")

    # Melt it
    dataMelt <- melt(data, id="year")

    # Write to CSV
    write.csv(dataMelt, "allData.csv", row.names=FALSE)


