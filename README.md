# spatial-join-tutorial


There are usually difficulties in joining data to admin boundaries due to spelling, capitalisation, accents etc..

Afrimapr wants to improve that, particularly for users relatively new to these issues.

Here we start to develop a checklist identifying code steps that users can work through to aid the joining process.

The use-case is that you want to plot data on a map but the data only have names of regions or places. You also can get some spatial data that does have the coordinates of the regions or places. The data are in a spreadsheet type format and the spatial data are in some kind of GIS format like a shapefile.

STEPS

1. **Import the data** read the data into R as a dataframe (dfdata)
2. **Import the spatial data** read in the spatial data to R as an sf object (sfshapes)
3. **Check the class** check that dfdata is a data.frame and sfshapes is an sf object with class(dfdata) and class(sfshapes) 
4. **Identify columns for joining** view both objects and identify the columns that contain the information (e.g. place names) you wish to join the data on.
5. **Check the names in each column** use distinct to check the names in the two columns.

7. **Detect the matches and non-matches** use str_c to create a search and str_subset to detect matches and non-matches.
8. **Rename placenames so they match** use recode to rename the place names so that they match and appear how you wish them to appear on the map.
9. **Rename placenames so they appear how you want** think about how you want the names to appear on the map, make a note of any changes to the names you would like to make. 

10. **Join the datasets** try initial join dplyr::left_join(), check that the datasets match up by checking the dimensions of the new dataframe.

11. **Plot the data on a map**
