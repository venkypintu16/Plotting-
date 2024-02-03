#Vectors are initialized with values.
frequency = c(0.6, 0.3, 0.4, 0.4, 0.2, 0.6, 0.3, 0.4, 0.9, 0.2)
bloodpressure = c(103, 87, 32, 42, 59, 109, 78, 205, 135, 176)
first = c(1,1,1,1,0,0,0,0,NA,1)
second = c(0,0,1,1,0,0,1,1,1,1)
final = c(0,1,0,1,0,1,0,1,1,1)

#boxplots
par(mfrow=c(1, 3))
boxplot(frequency, main = "Frequency", ylab = "frequency")
boxplot(bloodpressure, main = "bloodpressure", ylab = "BP values") 
boxplot(c(first, second, final), main = "Doc opinion", ylab = "VALUES", na.rm = T)

#histogram
par(mfrow=c(1, 3))
hist(frequency, main="Frequency Histogram", xlab="Frequency", ylab = "scale")
hist(bloodpressure, main="Blood Pressure Histogram", xlab="Blood Pressure", ylab = "scale")
hist(c(first, second, final), main="Doc opinion", xlab="Values", ylab = "scale")


##Explanation:
Assigning the values to vectors using c() function:
1. frequency: A vector of frequency values.
2. bloodpressure: A vector of blood pressure values.
3. first, second, final: Vectors representing binary variables (0 or 1) with some missing values (NA) in the 'first' vector.

Boxplots:
•	The code sets up a 1x3 layout for side-by-side boxplots using par(mfrow=c(1, 3)).
•	Three boxplots are created using the boxplot function for 'frequency', 'bloodpressure', and the combined binary variables ('first', 'second', 'final').
•	The missing values are excluded using (na.rm = T) which gives us clean boxplot of vector which has missing values.
•	Each boxplot has a title specified by the main argument and a y-axis label specified by the ylab argument.
•	After plotting, the layout is we can reset to the default (1x1) using par(mfrow=c(1, 1)) 

Histograms:
•	The code sets up another 1x3 layout for side-by-side histograms using par(mfrow=c(1, 3)).
•	Three histograms are created using the hist function for 'frequency', 'bloodpressure', and the combined binary variables ('first', 'second', 'final').
•	Each histogram has a title specified by the main argument and an x-axis label specified by the xlab argument & a y-axis label specified by the ylab argument.
•	Similar to the boxplots, the layout can be reseted to the default (1x1) after plotting histograms using par(mfrow=c(1, 1)).

### Results explaination:

Frequency:
• The boxplot for frequency shows a median around 0.4, with some variability in the data.
• The histogram for frequency indicates that the majority of values are concentrated around 0.4, with some values above and below this central tendency.

Blood Pressure:
• The boxplot for blood pressure shows a wide range of values. There is an outlier with a blood pressure value of 205.
• The boxplot show the blood pressure median of around the value of 85-90. 
• The histogram for blood pressure suggests a skewed distribution towards lower values, with a spike around 50-60 and a long tail towards higher values around 202.
