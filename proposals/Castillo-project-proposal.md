Michael Castillo
Project Proposal

Abstract:

Nuclear power plant outages can pose large financial setbacks for the nuclear industry. 
Depending on the severity of these outages, some power plants face termination from unprecedented economic setback. 
This research aims to minimize/mitigate power plant outages by analyzing documented operating reports of the United 
States nuclear power plant fleet from 1997 to 2016. Using methods in both engineering and data analysis, large metadata 
is processed to develop insight into implementing physical upgrades to reactors and addressing the source of common outages. 

Functionality:

What I intend for my software to accomplish is;
•	Classify data into subgroups by using available string type data
•	Build visual representation with information from sub groups
•	Identify common words from strings that gives information about data by implementing natural language processing techniques
•	Develop a decision tree algorithm that can to assist in data exploration
o	Build a model based on a target variable that I want to pick.
•	(Still not sure what target variable to pick)
•	(Still verifying if my data can even return results)

Individuals that will use my software are those that are exploring the following;
•	Investigating the applicability of their data. 
•	Using strings to identify important features of their data
•	Processing their data for future statistical analysis

Inputs and outputs:

Inputs: The software will require inputted Dataframe structure such as a CSV formatted file for processing.

Outputs: 
•	CSV files consisting of sub group information
•	Return text files with most common words in strings
•	Print visuals to text files
•	Print results from decision tree
Methodology:
Being new to package development, I intend to follow the methodology presented in the below link:
http://docs.python-guide.org/en/latest/writing/structure/

While also supplementing with information provided by the following;
https://packaging.python.org/tutorials/distributing-packages/
https://python-packaging.readthedocs.io/en/latest/

Current Status of proposed work:

As of this current state in my research, I have built a code that acts as a word counter to all the strings in a column of my data. 
Although the counter works, it does not accurately represent a true count. For example, a string existing in a column may be of the following

 “ THE TURBINE WAS SHUT DOWN BECAUSE OF A MALFUNCTIONING RELAY. THE TURBINE WAS THEN RETURNED ONLINE AFTER RELAY WAS FIXED.”

My current code counts all occurrences of specified words based on a list of keywords I give it. 
This is not what I need because I want to find a true count of what components of nuclear power plants have the most issues. 
Therefore, the string above will return two values for both TURBINE and RELAY

My new software, will only count nouns one time, and also return the respective index in which the nouns of interest occurred 
(So I can pull other data from different columns related to the timestamp). 

Packages:

I intend to use the following packages for python 2.7 in my code development;
•	Numpy
•	Pandas
•	Scikit






