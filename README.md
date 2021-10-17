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


## Single for Loop


## Results

### Stocks Analysis 

### Run time Analysis

## Summary
