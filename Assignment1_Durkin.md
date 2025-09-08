# Assignment 1 - Penguins Dataset
# Kristen Durkin
# Course: Machine Learning 64060
# Data Source: https://raw.githubusercontent.com/allisonhorst/palmerpenguins/main/inst/extdata/penguins.csv

# Import dataset
penguins <- read.csv("penguins.csv")

# Descriptive statistics
summary(penguins$bill_length_mm)   # quantitative
summary(penguins$body_mass_g)      # quantitative
table(penguins$species)            # categorical
table(penguins$sex)                # categorical

# Transform a variable
penguins$body_mass_z <- scale(penguins$body_mass_g)

# Plot a quantitative variable
hist(penguins$body_mass_g,
     main = "Histogram of Penguin Body Mass",
     xlab = "Body Mass (g)")

# Scatterplot
plot(penguins$bill_length_mm, penguins$flipper_length_mm,
     xlab = "Bill Length (mm)",
     ylab = "Flipper Length (mm)",
     main = "Scatterplot: Bill Length vs Flipper Length")
