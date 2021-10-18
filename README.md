# Stocks Anlaysis with Excel And VBA 

## Overview of Project

This repository contains the analysis of a set of data on different schools within the same district.
The goal is to modify the analysis as the math and reading grade data has been altered for 9th graders.

The analysis consists of comparing how this change affects the data the general summary

- Schools District Resume
- High performing schools based on Overall percetage pass
- Resume of scores by grades
- Resume of scores by school spending per student
- Resume of scores by school size
- Resume of scores by school type 


## Nan for cleaning the data.

The first challenge was to select all the 9th graders of the Thomas High School and discard only the math and reading scores since we know they have been altered.
The challenge was to place a NaN in those cells since all the other data is important for the analysis.

```ruby
    student_data_df.loc[(student_data_df["school_name"]=="Thomas High School") & (student_data_df["grade"]=="9th"), "reading_score"]=np.NaN
```

In order to achive that, with the previous section of code looks in the "clean" student_data_df dataframe for rows equal to "Thomas High School " and "9th" grades with the operator "&"

Then using the Numpy library the  NaN fuction set the grades into NaN 



## Results

-  ### Schools District Resume

    The first step was to determine the number of erroneous data that were converted to Nan


    ```ruby
    nineth_studets_ths = school_data_complete_df.loc[(school_data_complete_df["school_name"] == "Thomas High School")&(school_data_complete_df["grade"]=="9th"), "student_name"].count()
    ```

The data says that 461 score´s where corrupted and set to NaN

- ### Average Math Score
The average math score data shows a difference of only 0.05% compared to the data frame with the wrong data

- https://github.com/dani1925/School_District_Analysis/blob/main/resources/AMS_challenge.jpeg

the corrected dataframe shows that the average math score was 83.35% while in the data frame with wrong data it was 83.4% 

- ### Average Math Score in THS

Something similar happens with the averge reading score, the variation between dataframes does not exceed 0.05%

 in the corrected dataframe the average was 83.89%


 - ### Scores by Grade 
as expected, the 9th graders scores from THS are Not a number in the data frame, while the other schools remain unchanged

- https://github.com/dani1925/Election_Analysis/blob/main/image1.JPG?raw=true




### Conclusion

If we carefully observe each of the reported analyzes, it is noted that there is not a great variation in the results.

Of the set of 39,179 rows of data, only 461 were slightly modified. This means that only 1.17% of the data was modified and it is not enough to move the average significantly from any field of study.
