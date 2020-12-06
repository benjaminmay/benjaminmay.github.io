---
layout: post
title: Hospital Lab



---



### Most Hospital Beds Per Person

New York County


### Obtaining and Cleaning the Dataset

In order to get and clean the data set I wrote two different codes, one for getting, one for cleaning.

###### Getting Data

I created a method called Query. It took in an id, and queried the server for the data of that id. It would then print the data. I created this method so that I can create a loop that would call upon this method with the id incrementing by one each time. THis would allow me to get the data of all of the ID's. I would then pipe this file to a csv file called output. 

######  Cleaning Data

I created a method called HAB Changer. It took in a variable called HAB and Beds. It would then return the new HAB value of '2000HAB' , and the modified Bed Value.  To get the modified bed value, I divided 2000 by the old HAB value, and multiplied that by the Bed value. I created this function so that I could create a loop that would go throught each row of the output csv file, and change the values accordingly. Unfortantely, I do not know how to write into a csv file from a python code directly. So, what I formatted the values of each row (with the modified HAB and Beds value at this point) so that they would be printed in a style that could be piped into a csv file named outputFinal. 


### My process

In order to complete this lab, I worked in order of what needed to be done. I had to get the data, clean the data, and then analyze the data. WIth getting the data, I went imediately with the method described above. It was not very difficult, and worked almsot imediately. The one struggle was figuring out the line data = response.text. Figuring out that the word text followed it took a while, I tried a bunch of different stuff before then, including .json. I went almost immediately with the methods described above for cleaning the data. The one thing that I initially struggled with was printing the rows so that it could be piped into a csv file. I tried originaly to just print each (modified) row as a list, but it would not pipe cleanly. Since it was a csv file I wanted to convert it to, I figured I had to just seperate the values by commas. So I made a string for each row where the values were seperated by commas, and printed that, and that worked. 

I immediately figured out how to analyze the data  by thinking back to our first lab, it was very similar in nature. However, this time I went with an aproach where the county (species in the other one) was not hardcoded. I used a current max, current system. What I mean by that is that the previous highest beds per person was recorded in one variable, lets call it MAX for example. In another variable, lets call it Current, the beds per person of the row it is currently on would be added to it. If the county of the current row changes, then the MAX takes the value of the Current if the Current is higher than the MAX, and the Current is reset. Thus, the variable MAX will have the most hospital beds per person. These variables will be lists that can both record the beds per person as well as the county, so that we can know both. Thank You for reading this. 
