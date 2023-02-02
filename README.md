# Assign4
Programming Structure in R
# Create the rows
Freq <- c(0.6, 0.3, 0.4, 0.4, 0.2, 0.6, 0.3, 0.4, 0.9, 0.2)
Bloodp <- c(103, 87, 32, 42, 59, 109, 78, 205, 135, 176)
First <- c(1, 1, 1, 1, 0, 0, 0, 0, NA, 1)
Second <- c(0, 0, 1, 1, 0, 0, 1, 1, 1, 1)
FD <- c(0, 1, 0, 1, 0, 1, 0, 1, 1, 1)
inpatient.df <- data.frame(Freq, Bloodp, First, Second, FD)
inpatient.df

# Create side-by-side boxplot
boxplot(inpatient.df$Bloodp ~ inpatient.df$First, main = "1st MD Rating of BP Patients", xlab = "1st MD Rating", ylab = "Blood Pressure")
boxplot(inpatient.df$Bloodp ~ inpatient.df$FD, main = "FD Ratings of BP Patients", xlab = "FD Rating", ylab = "Blood Pressure")

# Create side-by-side histogram
hist(inpatient.df$Bloodp, main = "Patient Blood Pressure", xlab = "Blood Pressure")

# Discuss the outcome of results

# Regarding patients Blood Pressure and calculation of the mean of final decision ratings
mean(FD)
mean(Freq)
