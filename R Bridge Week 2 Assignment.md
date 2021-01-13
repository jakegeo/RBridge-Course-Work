---
title: "R Bridge Week 2 Assignment"
author: "Jacob George"
date: "1/9/2021"
output: html_document
---



## R Markdown


#### Question#1: Use the summary function to gain an overview of the data set.Then display the mean and median for at least two attributes.
```

HealthInsurance <-read.csv("C:/Users/JG/Downloads/HealthInsurance.csv")
HealthInsurance
summary(HealthInsurance)

#Age Attribute
mean(HealthInsurance$age)
median(HealthInsurance$age)

#Family Attribute
mean(HealthInsurance$family)
median(HealthInsurance$family)
```

#### Question#1 Solution
```

> summary(HealthInsurance)
       X           health               age           limit              gender         
 Min.   :   1   Length:8802        Min.   :18.00   Length:8802        Length:8802       
 1st Qu.:2201   Class :character   1st Qu.:30.00   Class :character   Class :character  
 Median :4402   Mode  :character   Median :39.00   Mode  :character   Mode  :character  
 Mean   :4402                      Mean   :38.94                                        
 3rd Qu.:6602                      3rd Qu.:48.00                                        
 Max.   :8802                      Max.   :62.00                                        
  insurance           married            selfemp              family          region         
 Length:8802        Length:8802        Length:8802        Min.   : 1.000   Length:8802       
 Class :character   Class :character   Class :character   1st Qu.: 2.000   Class :character  
 Mode  :character   Mode  :character   Mode  :character   Median : 3.000   Mode  :character  
                                                          Mean   : 3.094                     
                                                          3rd Qu.: 4.000                     
                                                          Max.   :14.000                     
  ethnicity          education        
 Length:8802        Length:8802       
 Class :character   Class :character  
 Mode  :character   Mode  :character  
 
> #Age Attribute
> mean(HealthInsurance$age)
[1] 38.93683
> median(HealthInsurance$age)
[1] 39
> 
> #Family Attribute
> mean(HealthInsurance$family)
[1] 3.093501
> median(HealthInsurance$family)
[1] 3 
                                      
```

#### Question#2: Create a new data frame with a subset of the columns and rows.  Make sure to rename it.
```
New_Df <- subset(HealthInsurance, select = c(health, age, limit, gender, insurance, married, selfemp, family, region, ethnicity, education))
New_Df

```

#### Question#2 Solution
```
  health age limit gender insurance married selfemp family    region ethnicity  education
1     yes  31    no   male       yes     yes     yes      4     south      cauc   bachelor
2     yes  31    no female       yes     yes      no      4     south      cauc highschool
3     yes  54    no   male       yes     yes      no      5      west      cauc        ged
4     yes  27    no   male       yes      no      no      5      west      cauc highschool
5     yes  39    no   male       yes     yes      no      5      west      cauc       none
6     yes  32    no female        no      no      no      3     south      afam   bachelor
7      no  56   yes female       yes     yes      no      2      west      cauc highschool
8     yes  60    no female       yes     yes      no      2     south      cauc highschool
9     yes  62    no   male       yes     yes      no      2     south      cauc highschool
10    yes  52    no female        no     yes      no      2 northeast      afam highschool
11    yes  50    no   male       yes     yes      no      2 northeast      afam highschool
12    yes  44    no   male       yes      no      no      1   midwest      cauc     master
13    yes  26    no female        no     yes     yes      3     south      cauc        phd
14    yes  38   yes   male        no     yes      no      7      west      cauc       none
15    yes  48    no   male       yes     yes      no      8     south      cauc      other
16    yes  48    no female       yes     yes      no      8     south      cauc       none
17    yes  53    no   male        no     yes     yes      2   midwest      cauc       none
18    yes  50    no female        no     yes      no      2   midwest      cauc highschool
19    yes  23    no female        no      no      no      1   midwest      cauc highschool
20    yes  43    no female       yes      no      no      2     south      cauc highschool
21    yes  40    no female       yes      no      no      4   midwest      cauc highschool
22    yes  25    no   male        no      no      no      1      west      cauc highschool
23    yes  27    no   male        no     yes      no      3      west      cauc   bachelor
24    yes  53    no   male       yes     yes      no      6 northeast      afam       none
25    yes  40    no female       yes     yes      no      6 northeast      afam       none
26     no  22   yes female       yes      no      no      2 northeast      afam highschool
27    yes  51   yes   male        no     yes      no      3      west      cauc       none
28     no  27    no   male        no      no      no      3      west      cauc       none
29     no  58   yes female        no     yes      no      3      west      cauc       none
30    yes  45    no   male       yes     yes      no      4      west      cauc       none
31    yes  18    no   male       yes      no      no      4      west      cauc       none
32    yes  31    no   male       yes     yes      no      2     south      cauc      other
33    yes  31    no female       yes     yes      no      2     south      cauc highschool
34    yes  27    no   male        no      no      no      1     south      cauc   bachelor
35    yes  61    no   male       yes      no      no      1     south      cauc highschool
36    yes  33   yes female       yes      no      no      1      west      cauc   bachelor
37    yes  40    no female       yes      no      no      1      west      cauc   bachelor
38     no  43   yes   male       yes     yes      no      4   midwest      cauc highschool
39    yes  44    no female       yes     yes      no      4   midwest      cauc   bachelor
40     no  55    no   male       yes     yes     yes      2     south      cauc highschool
41    yes  52    no female       yes     yes      no      2     south      cauc        ged
42    yes  30    no female       yes     yes      no      5     south      cauc highschool
43    yes  33    no   male       yes     yes      no      5     south      cauc highschool
44    yes  28    no   male       yes     yes      no      3     south      cauc       none
45     no  28    no female       yes     yes      no      3     south      cauc highschool
46    yes  31    no   male       yes     yes      no      2      west      cauc highschool
47    yes  39   yes female        no     yes     yes      2      west      cauc      other
48    yes  22    no   male        no      no      no      6     south      cauc highschool
49    yes  21    no female        no      no      no      6     south      cauc highschool
50    yes  42    no female        no     yes     yes      3   midwest      afam highschool
51     no  61   yes female       yes      no      no      3 northeast      cauc highschool
52    yes  36    no   male       yes     yes      no      4      west      cauc highschool
53    yes  27    no   male       yes     yes      no      3      west      cauc   bachelor
54    yes  46    no   male       yes     yes      no      4   midwest      cauc highschool
55    yes  38    no female       yes     yes      no      4   midwest      cauc highschool
56    yes  29    no   male       yes     yes      no      5      west     other       none
57    yes  33    no   male        no      no      no      1      west      cauc   bachelor
58    yes  60    no   male       yes     yes      no      2     south      afam      other
59    yes  60    no female       yes     yes      no      2     south      afam      other
60    yes  35    no   male       yes      no      no      1      west     other highschool
61    yes  30    no female       yes      no      no      3   midwest      afam highschool
62    yes  61   yes   male       yes     yes     yes      2   midwest      cauc highschool
63    yes  58    no female       yes     yes      no      2   midwest      cauc highschool
64    yes  46    no female       yes      no      no      3     south      afam highschool
65    yes  55    no female        no      no      no      1      west      cauc highschool
66    yes  20   yes female        no      no      no      3   midwest      cauc highschool
67    yes  44    no   male       yes     yes      no      3   midwest      cauc highschool
68    yes  43    no female       yes     yes      no      3   midwest      cauc highschool
69    yes  26   yes   male       yes     yes      no      3     south      cauc highschool
70    yes  45    no   male       yes     yes     yes      5   midwest      cauc      other
71    yes  39    no female       yes     yes     yes      5   midwest      cauc      other
72    yes  21    no   male       yes      no      no      5   midwest      cauc highschool
73    yes  53    no female       yes      no      no      2     south      cauc      other
74    yes  18    no   male       yes      no      no      2     south      cauc       none
75    yes  31    no   male       yes     yes      no      2     south      cauc highschool
76    yes  33    no female        no     yes      no      2     south      cauc highschool
77    yes  27    no female       yes      no      no      2     south      cauc      other
78    yes  47    no   male       yes     yes      no      4   midwest      cauc highschool
79    yes  55    no   male       yes     yes      no      2   midwest      cauc     master
80    yes  53    no female       yes     yes      no      2   midwest      cauc highschool
81    yes  29    no female       yes     yes      no      2   midwest      cauc     master
82    yes  34    no   male       yes     yes      no      4   midwest      cauc highschool
83    yes  34    no female       yes     yes      no      4   midwest      cauc      other
84     no  38   yes female       yes      no      no      1      west      cauc highschool
85    yes  49    no   male       yes     yes      no      2   midwest      cauc highschool
86    yes  32    no female       yes     yes      no      2   midwest      cauc      other
87    yes  47    no   male        no     yes      no     10     south      cauc       none
88    yes  20    no   male        no     yes      no     10     south      cauc       none
89    yes  53    no female       yes      no      no      1   midwest      cauc highschool
90    yes  56    no   male       yes      no     yes      2 northeast      cauc highschool
[ reached 'max' / getOption("max.print") -- omitted 8712 rows ]

```


#### Question#3: Create new column names for the new data frame.
```
colnames(New_Df) <- c('Healthy', 'AGE', 'Insurance_Limit', 'Gender' , 'Qualified_Insurance', 'Marital_Status', 'Self_Employed', 'Household_Size', 'Geo_Location', 'Ethnicity', 'Education_Level')
New_Df

```


#### Question#3 Solution (Partial Solution shown for the first 20 entries of each attribute)
```
   Healthy AGE Insurance_Limit Gender Qualified_Insurance Marital_Status Self_Employed
1      yes  31              no   male                 yes            yes           yes
2      yes  31              no female                 yes            yes            no
3      yes  54              no   male                 yes            yes            no
4      yes  27              no   male                 yes             no            no
5      yes  39              no   male                 yes            yes            no
6      yes  32              no female                  no             no            no
7       no  56             yes female                 yes            yes            no
8      yes  60              no female                 yes            yes            no
9      yes  62              no   male                 yes            yes            no
10     yes  52              no female                  no            yes            no
11     yes  50              no   male                 yes            yes            no
12     yes  44              no   male                 yes             no            no
13     yes  26              no female                  no            yes           yes
14     yes  38             yes   male                  no            yes            no
15     yes  48              no   male                 yes            yes            no
16     yes  48              no female                 yes            yes            no
17     yes  53              no   male                  no            yes           yes
18     yes  50              no female                  no            yes            no
19     yes  23              no female                  no             no            no
20     yes  43              no female                 yes             no            no

 Household_Size Geo_Location Ethnicity Education_Level
1               4        south      cauc        bachelor
2               4        south      cauc      highschool
3               5         west      cauc             ged
4               5         west      cauc      highschool
5               5         west      cauc            none
6               3        south      afam        bachelor
7               2         west      cauc      highschool
8               2        south      cauc      highschool
9               2        south      cauc      highschool
10              2    northeast      afam      highschool
11              2    northeast      afam      highschool
12              1      midwest      cauc          master
13              3        south      cauc             phd
14              7         west      cauc            none
15              8        south      cauc           other
16              8        south      cauc            none
17              2      midwest      cauc            none
18              2      midwest      cauc      highschool
19              1      midwest      cauc      highschool
20              2        south      cauc      highschool
```




#### Question#4: Use the summary function to create an overview of your new data frame.  The print the mean and median for the same two attributes. Please compare.
```
summary(New_Df)

#Age Attribute
mean(New_Df$AGE)
median(New_Df$AGE)

#Family Attribute
mean(New_Df$Household_Size)
median(New_Df$Household_Size)

```




#### Question#4 Solution
```
> summary(New_Df)
   Healthy               AGE        Insurance_Limit       Gender          Qualified_Insurance
 Length:8802        Min.   :18.00   Length:8802        Length:8802        Length:8802        
 Class :character   1st Qu.:30.00   Class :character   Class :character   Class :character   
 Mode  :character   Median :39.00   Mode  :character   Mode  :character   Mode  :character   
                    Mean   :38.94                                                            
                    3rd Qu.:48.00                                                            
                    Max.   :62.00                                                            
 Marital_Status     Self_Employed      Household_Size   Geo_Location        Ethnicity        
 Length:8802        Length:8802        Min.   : 1.000   Length:8802        Length:8802       
 Class :character   Class :character   1st Qu.: 2.000   Class :character   Class :character  
 Mode  :character   Mode  :character   Median : 3.000   Mode  :character   Mode  :character  
                                       Mean   : 3.094                                        
                                       3rd Qu.: 4.000                                        
                                       Max.   :14.000                                        
 Education_Level   
 Length:8802       
 Class :character  
 Mode  :character  
                   
                   
> #Age Attribute
> mean(New_Df$AGE)
[1] 38.93683
> median(New_Df$AGE)
[1] 39
> #Family Attribute
> mean(New_Df$Household_Size)
[1] 3.093501
> median(New_Df$Household_Size)
[1] 3

For the same attributes of Age and Family size in both the original data frame and new data frame we made, there is no difference in the mean and median values. We will get a mean of 38.93683 and median of 39 for Age and a mean of 3.093501 and median of 3 for Family. If we decided to modify our new data frame to show specific data, we can include a condition to do just that. For example, we can say we want to only consider individuals in the column Health to be "Yes" and exclude individuals marked as "No". In our existing data frame, we would need to include "health == yes". The query would look like: 
New_Df <- subset(HealthInsurance, health == 'yes', select = c(age, limit, gender, insurance, married, selfemp, family, region, ethnicity, education))
New_Df
                  
```


#### Question#5: For at least 3 values in a column please rename so that every value in that column is renamed.  For example, suppose I have 20 values of the letter “e”in one column.  Rename those values so that all 20 would show as “excellent”.
```
New_Df$Education_Level <- with(New_Df, replace(Education_Level, Education_Level == 'highschool', 'HighSchool_Diploma'))
New_Df
New_Df$Education_Level <- with(New_Df, replace(Education_Level, Education_Level == 'bachelor', 'Bachelors_Degree'))
New_Df
New_Df$Education_Level <- with(New_Df, replace(Education_Level, Education_Level == 'master', 'Masters_Degree'))
New_Df

```


#### Question#5 Solution (Partial Solution shown for the first 20 entries of each attribute)
```
 Healthy AGE Insurance_Limit Gender Qualified_Insurance Marital_Status Self_Employed
1      yes  31              no   male                 yes            yes           yes
2      yes  31              no female                 yes            yes            no
3      yes  54              no   male                 yes            yes            no
4      yes  27              no   male                 yes             no            no
5      yes  39              no   male                 yes            yes            no
6      yes  32              no female                  no             no            no
7       no  56             yes female                 yes            yes            no
8      yes  60              no female                 yes            yes            no
9      yes  62              no   male                 yes            yes            no
10     yes  52              no female                  no            yes            no
11     yes  50              no   male                 yes            yes            no
12     yes  44              no   male                 yes             no            no
13     yes  26              no female                  no            yes           yes
14     yes  38             yes   male                  no            yes            no
15     yes  48              no   male                 yes            yes            no
16     yes  48              no female                 yes            yes            no
17     yes  53              no   male                  no            yes           yes
18     yes  50              no female                  no            yes            no
19     yes  23              no female                  no             no            no
20     yes  43              no female                 yes             no            no

Household_Size Geo_Location Ethnicity    Education_Level
1               4        south      cauc   Bachelors_Degree
2               4        south      cauc HighSchool_Diploma
3               5         west      cauc                ged
4               5         west      cauc HighSchool_Diploma
5               5         west      cauc               none
6               3        south      afam   Bachelors_Degree
7               2         west      cauc HighSchool_Diploma
8               2        south      cauc HighSchool_Diploma
9               2        south      cauc HighSchool_Diploma
10              2    northeast      afam HighSchool_Diploma
11              2    northeast      afam HighSchool_Diploma
12              1      midwest      cauc     Masters_Degree
13              3        south      cauc                phd
14              7         west      cauc               none
15              8        south      cauc              other
16              8        south      cauc               none
17              2      midwest      cauc               none
18              2      midwest      cauc HighSchool_Diploma
19              1      midwest      cauc HighSchool_Diploma
20              2        south      cauc HighSchool_Diploma
```


#### Question#6: Display enough rows to see examples of all of steps 1-5 above.
```
#print(New_Df) this will show the data set up to the max threshold
head(New_Df, 20)
tail(New_Df, 20)

```


#### Question#6 Solution
```
> head(New_Df, 20)
   Healthy AGE Insurance_Limit Gender Qualified_Insurance Marital_Status Self_Employed
1      yes  31              no   male                 yes            yes           yes
2      yes  31              no female                 yes            yes            no
3      yes  54              no   male                 yes            yes            no
4      yes  27              no   male                 yes             no            no
5      yes  39              no   male                 yes            yes            no
6      yes  32              no female                  no             no            no
7       no  56             yes female                 yes            yes            no
8      yes  60              no female                 yes            yes            no
9      yes  62              no   male                 yes            yes            no
10     yes  52              no female                  no            yes            no
11     yes  50              no   male                 yes            yes            no
12     yes  44              no   male                 yes             no            no
13     yes  26              no female                  no            yes           yes
14     yes  38             yes   male                  no            yes            no
15     yes  48              no   male                 yes            yes            no
16     yes  48              no female                 yes            yes            no
17     yes  53              no   male                  no            yes           yes
18     yes  50              no female                  no            yes            no
19     yes  23              no female                  no             no            no
20     yes  43              no female                 yes             no            no

 Household_Size Geo_Location Ethnicity    Education_Level
1               4        south      cauc   Bachelors_Degree
2               4        south      cauc HighSchool_Diploma
3               5         west      cauc                ged
4               5         west      cauc HighSchool_Diploma
5               5         west      cauc               none
6               3        south      afam   Bachelors_Degree
7               2         west      cauc HighSchool_Diploma
8               2        south      cauc HighSchool_Diploma
9               2        south      cauc HighSchool_Diploma
10              2    northeast      afam HighSchool_Diploma
11              2    northeast      afam HighSchool_Diploma
12              1      midwest      cauc     Masters_Degree
13              3        south      cauc                phd
14              7         west      cauc               none
15              8        south      cauc              other
16              8        south      cauc               none
17              2      midwest      cauc               none
18              2      midwest      cauc HighSchool_Diploma
19              1      midwest      cauc HighSchool_Diploma
20              2        south      cauc HighSchool_Diploma



> tail(New_Df, 20)
     Healthy AGE Insurance_Limit Gender Qualified_Insurance Marital_Status Self_Employed
8783     yes  57             yes   male                 yes            yes            no
8784     yes  33              no   male                 yes            yes            no
8785     yes  32              no female                 yes            yes           yes
8786     yes  45              no   male                 yes            yes            no
8787     yes  42              no female                 yes            yes            no
8788     yes  19              no   male                 yes             no            no
8789     yes  47              no female                  no            yes           yes
8790     yes  22              no   male                  no             no            no
8791     yes  40              no female                 yes             no            no
8792      no  33              no   male                 yes            yes            no
8793     yes  50              no   male                 yes             no           yes
8794      no  36              no   male                 yes             no            no
8795     yes  34              no female                 yes             no            no
8796     yes  34              no   male                 yes            yes            no
8797     yes  33              no female                 yes            yes            no
8798     yes  46              no female                 yes            yes            no
8799     yes  50              no   male                 yes            yes            no
8800     yes  27              no   male                 yes            yes            no
8801     yes  27              no female                 yes            yes            no
8802     yes  35              no   male                 yes            yes            no

 Household_Size Geo_Location Ethnicity    Education_Level
8783              2    northeast      cauc               none
8784              2      midwest      cauc   Bachelors_Degree
8785              2      midwest      cauc     Masters_Degree
8786              5    northeast      cauc              other
8787              5    northeast      cauc              other
8788              5    northeast      cauc HighSchool_Diploma
8789              4        south      cauc   Bachelors_Degree
8790              4        south      cauc HighSchool_Diploma
8791              3      midwest      afam HighSchool_Diploma
8792              6        south      cauc HighSchool_Diploma
8793              1      midwest      cauc HighSchool_Diploma
8794              1    northeast      cauc HighSchool_Diploma
8795              2        south      cauc HighSchool_Diploma
8796              4      midwest      cauc HighSchool_Diploma
8797              4      midwest      cauc HighSchool_Diploma
8798              3    northeast      cauc HighSchool_Diploma
8799              3    northeast      cauc HighSchool_Diploma
8800              2        south      cauc   Bachelors_Degree
8801              2        south      cauc   Bachelors_Degree
8802              4    northeast      cauc                phd

```


#### Question#7: BONUS –place the original .csv in a github file and have R read from the link.  This will be a very useful skill as you progress in your data science education and career.
```
HealthInsurance_DataSet <- read.csv('https://raw.githubusercontent.com/jakegeo/RBridge-Course-Work/main/HealthInsurance.csv')
HealthInsurance_DataSet 

```


#### Question#7 Solution (Partial Solution shown for the first 20 entries of each attribute)
```
> HealthInsurance_DataSet <- read.csv('https://raw.githubusercontent.com/jakegeo/RBridge-Course-Work/main/HealthInsurance.csv')
> HealthInsurance_DataSet 
    X health age limit gender insurance married selfemp family    region ethnicity  education
1   1    yes  31    no   male       yes     yes     yes      4     south      cauc   bachelor
2   2    yes  31    no female       yes     yes      no      4     south      cauc highschool
3   3    yes  54    no   male       yes     yes      no      5      west      cauc        ged
4   4    yes  27    no   male       yes      no      no      5      west      cauc highschool
5   5    yes  39    no   male       yes     yes      no      5      west      cauc       none
6   6    yes  32    no female        no      no      no      3     south      afam   bachelor
7   7     no  56   yes female       yes     yes      no      2      west      cauc highschool
8   8    yes  60    no female       yes     yes      no      2     south      cauc highschool
9   9    yes  62    no   male       yes     yes      no      2     south      cauc highschool
10 10    yes  52    no female        no     yes      no      2 northeast      afam highschool
11 11    yes  50    no   male       yes     yes      no      2 northeast      afam highschool
12 12    yes  44    no   male       yes      no      no      1   midwest      cauc     master
13 13    yes  26    no female        no     yes     yes      3     south      cauc        phd
14 14    yes  38   yes   male        no     yes      no      7      west      cauc       none
15 15    yes  48    no   male       yes     yes      no      8     south      cauc      other
16 16    yes  48    no female       yes     yes      no      8     south      cauc       none
17 17    yes  53    no   male        no     yes     yes      2   midwest      cauc       none
18 18    yes  50    no female        no     yes      no      2   midwest      cauc highschool
19 19    yes  23    no female        no      no      no      1   midwest      cauc highschool
20 20    yes  43    no female       yes      no      no      2     south      cauc highschool

```


