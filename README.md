# GetJob.com-Webscraper

Project team
Shashank Chikara |  schikara@andrew.cmu.edu
Jennifer B Liu | jbistafa@andrew.cmu.edu
Jing Cao  | jingc2@andrew.cmu.edu
Dhruv Dixit  | dhruvdix@andrew.cmu.edu
Yingqian Wang | yingqian@andrew.cmu.edu

# Project Description
This project is a web scraper to give you job opportunities based on the type of job desired and the location. Relevant statistics for the job and location are also provided, along with reviews from current/past employees.


# Requirements
In order to run the project, python version 3.9x+ will need to be installed. If you don’t have it installed, please visit: https://www.python.org/downloads/.

Many libraries are also needed in order to run the program. A list of the libraries required and their installation commands are provided below:

Pip (install first): sudo apt install python3-pip
Numpy: pip3 install numpy
Re: should be included with python download
Pandas: pip install pandas
Requests: pip install requests
BeautifulSoup: pip install beautifulsoup4
Csv: should be included with python download
Plotext: pip install plotext
Pyfiglet: pip install pyfiglet
Texttable: pip install texttable

In addition, some datasets need to be added / saved to the same folder as the application. The list of datasets are (also included with the package):
HomeValueRaw.csv
LandAreaRaw.xlsx
CrimeRateRaw.xls


# How to Run
After setting up the entire environment, download the zip file provided. It is called “dfp_final”. Export this file into your IDE of choice and run the file titled “Main_module.py”. Then, you will get into the following main CLI interface. 

Navigating the UI:

<img width="605" alt="Screen Shot 2023-02-16 at 10 39 05 PM" src="https://user-images.githubusercontent.com/110956369/219543663-35d09afa-7ccf-4247-adb6-0ffca3d49908.png">

Here the user is asked to enter the information of following two questions 
Enter your desired job title: 
Enter a location to search:
The answer to the first question is about what type of  job you want, like data engineer or engineer or something else. The answer to the second question is about the location you like, Pittsburgh, Boston and so on. 
After typing in information, the program will start to work and CLI based user interface will also give the user a far richer experience by showing the progress of processes running in the background with a progress bar.
 (Like Data scrapping, data cleaning and other calculations)

Once the data is scrapped and crunched, the user is presented with a table containing the job postings and other information including job title, company, location, salary and time of posted, as shown below:

<img width="622" alt="Screen Shot 2023-02-16 at 10 41 12 PM" src="https://user-images.githubusercontent.com/110956369/219543738-06ba78d4-21cc-4a77-991d-f266850fad07.png">

Here you are presented with a menu where you can see options like
Enter the job id to get more details
Enter ‘m’ to search for another job title / location (Takes you to the main menu)
Enter ‘l’ to calculate the livability score of the location
Enter ‘b’ to go back to the search results
Enter ‘q’ to quit

You can select different options to get into the next step.

If a user enters the job id  (generally between 0-24), the user can get the detailed information about the jobs as shown below. More information like company rating, headcount, avg. salary at the company and many location information will be presented. To make the results more straightforward and better help users to make decisions we also include some charts here. We make a comparison of the crime rate, Avg.Home Value and income between the location user selected and the avg. of US. Also days of job posting are also presented with charts. The programme also collects the reviews of the company which is presented following the charts.  

<img width="429" alt="Screen Shot 2023-02-16 at 10 42 17 PM" src="https://user-images.githubusercontent.com/110956369/219543862-e26ca37f-946e-4806-819d-26ffd4eaa3a7.png">

<img width="425" alt="Screen Shot 2023-02-16 at 10 42 45 PM" src="https://user-images.githubusercontent.com/110956369/219543914-d363227a-5344-4292-8d36-30f8d839515d.png">

Also the users can get more information about livability with the livability score. First the user will be asked to provide the Job ID in the following information.
Enter the Job ID to calculate the livability score:

Then users also need to tell the programme the ranking for each city criteria, from 1 to 4 without repetition with 1 the most important ranking and 4 the least important ranking. After typing “y” to confirm the rankings, the programme can calculate and give the livability score. If you change the ranking of the city criteria, you will find the livability also changed according to the rankings.  

The livability score is calculated as the sum of criteria weights multiplied by normalized city variable. More specifically, the formula is:
Livability score =  
weight_density * (city_density - density_min) / (density_max -density_min) + weight_median_income * (median_income - median_income_min) / (median_income_max - median_income_min) 
+ weight_home_value * (home_value - home_value_min) / (home_value_max - home_value_min)
+ weight_crime_rate * (1-(crime_rate - crime_rate_min) / (crime_rate_max - crime_rate_min))

The weight for each for each criteria is defined by the user, according to the scale:
Rank 1st most important criteria = 40%
Rank 2nd most important criteria = 30%
Rank 3rd most important criteria = 20%
Rank 4th most important criteria = 10%

The livability score will range from 0 (zero) to 100 (one hundred). The final score will help users decide between different locations, which one would be more appropriate to him/her.

<img width="461" alt="Screen Shot 2023-02-16 at 10 43 14 PM" src="https://user-images.githubusercontent.com/110956369/219543993-f190b128-b49c-49f8-8c26-9dbe920cdff4.png">

If you want to go back to get detailed information about another company, then you can type in “b” in the choice blank to go back to the search results. Then you can check the information about other companies you like using the same procedures we go over above.

<img width="519" alt="Screen Shot 2023-02-16 at 10 43 55 PM" src="https://user-images.githubusercontent.com/110956369/219544054-db42d535-1649-44a0-ab32-aede58ec82ee.png">

Then if you want to quit and exit, you just need to type “q” in the  choice blank.


# Video-Demonstration
To see this application being ran, watch this video!:
https://www.youtube.com/watch?v=ClTejAYxjH4


Enjoy!

