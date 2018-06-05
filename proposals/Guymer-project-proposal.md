Solar Cell Calculations

Proposed Idea: A software package that calculates the maximum temperature storage of a flat plate solar collector. The software will take in user given design restrictions and information from the internet (ex: latitude and longitude values). 

Output: This software package will output two main items. The first item will be the values of the important variables used for solar cell evaluations (ex: declination angle, radiation values, etc.). The second item will be the maximum temperature storage of the collector and the time of day this value occurs.

Input: For item 1, users will input the location, date, and time. For item 2, users will input the area of the collector and the volume of the water storage. 

Potential Users: Students of CHE 551, solar systems designers, people curious about the viability of solar heating for their homes.

How the software will work: The software will need to grab data on a user specified location from the internet, apply that data along with other information to calculate a multitude of variables. These variables will then be applied to find the maximum temperature storage value of the collector.   

What I will do: I will implement web scraping to gather the necessary data and run the calculations.

Packages I will need: A webscraping package, Numpy or Scipy.

Sources: [1] Goswami, D. Yogi. Principles of Solar Engineering. Boca Raton: CRC Press, 2015. Print.
[2] Google



