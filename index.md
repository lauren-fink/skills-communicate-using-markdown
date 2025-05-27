# This is a header
## A sub-header
### A sub-sub-header
#### Etc. 

This is a short, meaningful commit message that describes the changes I made to the file. 

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)



```{r}
# Healthcare variables 
Healthcarevariables <- c("HealthcareYearly", "HealthcareScreening", "HealthcareSpecialized",  
                         "HealthcareInformation", "HealthcareMentalHealthServices",  
                         "HealthcareSubstanceUse", "HealthcareInsurance", "HealthcareTelehealth",  
                         "HealthcareTranslation", "HealthcareCulture", "HealthcareIdentity") 
 
# Define the ordinal levels 
ordinal_levels_healthcare <- c("Strongly Agree", "Agree", "Disagree", "Strongly Disagree") 
 
# Convert the Healthcare variables to ordered factors 
for (var in Healthcarevariables) { 
  CTSA_ForExport[[var]] <- factor(CTSA_ForExport[[var]], levels = ordinal_levels_healthcare, ordered = TRUE) 
} 
 
sapply(CTSA_ForExport[Healthcarevariables], class)  # Check if they are factors 
sapply(CTSA_ForExport[Healthcarevariables], levels)  # Check the levels of each factor 
```

