# R-boxplot
The script to make boxplots

df <- read.csv("C:\\Users\\USER\\Documents\\PNAN.csv")
head(df)

library(ggplot2)

df <- ggplot(df, aes(country, no))
df + geom_boxplot()
df + geom_boxplot(notch = T) 
df + geom_boxplot(outlier.shape = NA) + geom_jitter(width = 0)
#df + geom_boxplot(outlier.colour = "red", outlier.shape = 1)
