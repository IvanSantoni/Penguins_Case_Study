# Penguins_Case_Study
Data visualization of different kinds of penguins species using R


### Project Overview

This data analysis project aims to provide insight into the differce between differente penguins species. By analyzing various aspects of the data, we seek to identify different kind of information about the penguins physique and gain deeper understanding.

### Data Sources

Usage Data: The datasets used for this anlysis are "library('palmerpenguins')", containing detailed information about each Penguin.

### Tools

- R: Data Cleaning, Data Visualization

### Data Visualization and Cleaning

In the data cleaning and visualization phase we perform the following tasks:
1. Data loading and inspection;
2. Creation of different visuals to identify differences.

### Exploratory Data Analysis

EDA involved exploring the data to answer key question, such as:

- What is the biggest species between the penguins?
- Identify the bill mean between penguins in different island

### Data Analysis

Include some interesting code/features worked with

```r
p= ggplot(data=penguins)+
      geom_point(mapping=aes(x=flipper_length_mm,y=body_mass_g, color=species))+
      labs(title='Palmer Penguins')
```
For a linear regression line
```r
p + geom_smooth(mapping=aes(x=flipper_length_mm,y=body_mass_g))
```
To find means
```r
penguins %>% 
  group_by(island) %>% 
  drop_na() %>%  
  summarize(mean_bill_lenght_mm = mean(bill_length_mm))
```

# Results

The analysis results are the following:

1. The biggest penguins species is the Gentoo species as we can see in the following visual:

![pinguini](https://github.com/user-attachments/assets/26e36500-e902-4e56-a400-1d439f2fdb51)

2. The island with the penguins with the biggest bill is in the island of Biscoe.

### References

- [Posit Cloud](https://posit.cloud/)




