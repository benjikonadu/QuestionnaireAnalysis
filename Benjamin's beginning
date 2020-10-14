#Analyze data with raw likert scores
konadu baah
rm(list= ls())

setwd("/Users/user/Downloads/")
OrdinalData <- read.csv("Benji's Data.csv")[-1]

#This would assign values to some parameters later on in our functions
xpos <- c(0.7, 1.85, 3.1, 4.25, 5.5)
ypos <- c(5, 5, 5, 5, 5)
lab <- c("Very Dissatisfied", "Dissatisfied",  "Neither sat. nor Dissat.", "Satisfied", "Very Satisfied")

#Creating a PDF file directly for all plots 
pdf(file = "Benji's Plots.pdf")

#This function would merge the barplot and text functions together
Benji <- function(x){
  Final <- barplot(table(x), col = "grey", main = variable.names(x), xlab = "Likert Scores", ylab = "Number of Participants", ylim = c(0, 125), border = "NA", mgp=c(2,.5,0))
  text(xpos, ypos, labels = lab , adj = 0.05, srt = 90)
  
}
#realigning all value on the Y-axis horizontally
par(las = 1)

#A loop for our great plots :)
for (i in 1:15) {
  Benji(OrdinalData[i])
}

#bye plots :)
dev.off()
