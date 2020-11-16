# spatial-join-tutorial


There are usually difficulties in joining data to admin boundaries due to spelling, capitalisation, accents etc..

Afrimapr wants to improve that, particularly for users relatively new to these issues.

Here we start to develop a checklist identifying code steps that users can work through to aid the joining process.

The use-case is that you want to plot data on a map but the data only have names of regions or places. You also can get some spatial data that does have the coordinates of the regions or places. The data are in a spreadsheet type format and the spatial data are in some kind of GIS format like a shapefile.

STEPS

### STEPS

1. **Install and load the relevant libraries**

2. **Import the data frame** 

  - Read the data into R as a data.frame (dfdata).
  - Check that dfdata is a data.frame is a dataframe with class(dfdata).
  - Identify the column that contains the admin unit information. 

3. **Import the spatial data** 

  - Read in the spatial data to R as a sf object (sfshapes). 
  - Check that sfshapes is an sf object with class(sfshapes).
  - Plot sfshapes to check the locations. 
  - Identify the column that contains the admin unit information. 


4. **Joins: use anti_join to detect mismatches in admin units**
  - Use an `anti_join` to detect mismatches in the admin units.
  - Mismatches may occur due to different spellings or missing information.

5. **Joins: Renaming admin units**
  - Correct any mismatches due to differences in spellings.

6. **Joins: using left-join to join the datasets**
  - Use a `left_join` to join the data.frame to the spatial data.frame. 

7. **Plot the data on a map**



You can try out the tutorial by downloading the package:

# install.packages("devtools")
library(devtools)
devtools::install_github("afrijoin/join-admin")
