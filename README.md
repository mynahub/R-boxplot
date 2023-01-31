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

#The script to make boxplots

df <- read.csv("PNAN.csv") 
head(df)

library(ggplot2)

df <- ggplot(df, aes(Country, Frequency, fill=Country)) +
                  geom_boxplot()
            df+scale_fill_manual(values=c('#e6194b', '#3cb44b', '#ffe119', '#4363d8', '#800000', '#911eb4', '#46f0f0', '#f032e6', '#000075', '#808000', '#008080', '#000000'))
            df

# Better plot combining the two boxplots
library(ggplot2)
#PNAN
df <- read.csv("PNAN.csv") 
head(df)
df <- ggplot(df, aes(Country, Frequency, fill=Country)) + 
  geom_boxplot()+ 
  scale_fill_manual(values=c('#e6194b', '#3cb44b', '#ffe119', '#4363d8', '#800000', '#911eb4', '#46f0f0', '#f032e6', '#000075', '#808000', '#008080', '#000000')) 
df
#PNVD
df2 <- read.csv("PNVD1.csv") 
head(df2)
df2 <- ggplot(df2, aes(Country, Frequency, fill=Country)) +
  geom_boxplot() + 
  scale_fill_manual(values=c('#e6194b', '#3cb44b', '#ffe119', '#4363d8', '#800000', '#911eb4', '#46f0f0', '#f032e6', '#000075', '#808000', '#008080', '#000000'))
df2


ggarrange(df, df2, ncol = 1, nrow = 2, labels = c("A", "B"), common.legend = TRUE, legend = "right")
 
# Final Script
library(ggplot2)
#PNAN
df <- read.csv("PNAN.csv") 
head(df)
df <- ggplot(df, aes(Country, Frequency, fill=Country)) + 
  geom_boxplot()+ 
  theme(axis.text.x = element_text(color = "black", size = 10))+
  theme(axis.text.y = element_text(color = "black", size = 12))+ 
  scale_fill_manual(values=c('#e6194b', '#3cb44b', '#ffe119', '#4363d8', '#800000', '#911eb4', '#46f0f0', '#f032e6', '#000075', '#808000', '#008080', '#000000')) 
df
#PNVD
df2 <- read.csv("PNVD1.csv") 
head(df2)
df2 <- ggplot(df2, aes(Country, Frequency, fill=Country)) +
  geom_boxplot() + 
  theme(axis.text.x = element_text(color = "black", size = 10))+
  theme(axis.text.y = element_text(color = "black", size = 12))+
  scale_fill_manual(values=c('#e6194b', '#3cb44b', '#ffe119', '#4363d8', '#800000', '#911eb4', '#46f0f0', '#f032e6', '#000075', '#808000', '#008080', '#000000'))
df2


ggarrange(df, df2, ncol = 1, nrow = 2, labels = c("A", "B"), common.legend = TRUE, legend = "right")

