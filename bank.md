# International Students in Canada: 2015-2023

<img src="images/is_study.jpg?raw=true"/>

In the past 8 years, immigration laws and the education system have drastically changed in order to welcome a higher number of international students. However, the government of Canada has recently annouced that new regulations and rules will be implemented in the future for students visas in order to alleviate the current housing crisis.

We will explore and discover the different international student's trends from 2015 to 2023 using MySQL, as well as visualizing our findings using Tableau in order to understand the impact in the Canadian education and housing market.

The following dataset has been provided by Immigration, Refugees and Citizenship Canada

## International Students - Nationalities Segmentation

This section of the study will focus on the table called international_students_Canada, which provides us with information about the different countries international students have come between 2015 and 2023.

### Viewing Data
In order to explore and organize our data, we need to take a look and understand it. This way we can find inconsistencies or errors we can clean in the process.

<img src="images/001_view_data.png?raw=true"/>

### Deleting hearders from data
After taking a closer look at the data, I couldn't find any issues or mistakes. However, I did have issues importing the table into MySQL Workbench, specifically the headers becoming part of the data. This can be fixed using the following query:

<img src="images/002_delete_headers.png?raw=true"/>

### Number of Countries that contributed with international students between 2015 and 2023

While reviewing the data, I could easily see that there weree many countries that had 0 international students coming to Canada. I wouldn't consider this an error, so filtering the non-contributor countries out of our study will definitely help us with future calculations. The following query and subquery helps us identify and count how many countries actually contribute with international students in Canada.

<img src="images/003_number_countries.png?raw=true"/>

<img src="images/003_number_countries_ss.png?raw=true"/>

### Total number of international students between 2015 and 2023
I thought it would be interesting to now the exact number of international students Canada has received in the past 8 years. This number will help us with other type of analysis later on.

<img src="images/004_number_is.png?raw=true"/>

<img src="images/004_number_is_ss.png?raw=true"/>

### Top 5 Nationalities: 2015 - 2023
With this query, we identify the 5 countries that contributed with the most international students. Just to clarify, the sum of the values doesn't reflect the total number of international students Canada has received between 2015-2023.

<img src="images/005_top5_nat.png?raw=true"/>

<img src="images/is_top5_nat_2015_2023_hq.png?raw=true"/>

### Bottom 5 Nationalities: 2015-2023

Just as the query above, exploring the 5 countries that contributed with less students in the past 8 years is an interesting finding that could help us understand future trends and policies in the education system.

<img src="images/006_bottom5_nat.png?raw=true"/>

<img src="images/is_bottom_nat_hq.png?raw=true"/>

## International Students Per Year
In the following section, we will explore the numbers and Top 5 nationalities for each year, starting from 2015 and ending at 2023.

### Top 5 Nationalities in 2015

<img src="images/007_top2015.png?raw=true"/>

<img src="images/is_top5_nat_2015_hq.png?raw=true"/>

### Top 5 Nationalities in 2016

<img src="images/008_top2016.png?raw=true"/>

<img src="images/is_top5_nat_2016_hq.png?raw=true"/>

### Top 5 Nationalities in 2017

<img src="images/009_top2017.png?raw=true"/>

<img src="images/is_top5_nat_2017_hq.png?raw=true"/>

### Top 5 Nationalities in 2018

<img src="images/010_top2018.png?raw=true"/>

<img src="images/is_top5_nat_2018_hq.png?raw=true"/>

### Top 5 Nationalities in 2019

<img src="images/011_top_2019.png?raw=true"/>

<img src="images/is_top5_nat_2019_hq.png?raw=true"/>

### Top 5 Nationalities in 2020

<img src="images/012_top_2020.png?raw=true"/>

<img src="images/is_top5_nat_2020_hq.png?raw=true"/>

### Top 5 Nationalities in 2021

<img src="images/013_top_2021.png?raw=true"/>

<img src="images/is_top5_nat_2021_hq.png?raw=true"/>

### Top 5 Nationalities in 2022

<img src="images/014_top_2022.png?raw=true"/>

<img src="images/is_top5_nat_2022_hq.png?raw=true"/>

### Top 5 Nationalities in 2023

<img src="images/015_top_2023.png?raw=true"/>

<img src="images/is_top5_nat_2023_hq.png?raw=true"/>

### Total number of International Students per year
The following query and graph shows us the total number of international students Canada has hosted each year, from 2015 to 2023.

<img src="images/016_total_per_year.png?raw=true"/>

<img src="images/is_peryear_hq.png?raw=true"/>

### Average number of International students between 2015 and 2023

<img src="images/017_avg_per_year.png?raw=true"/>

<img src="images/017-5_avg_per_year.png?raw=true"/>

### Creating Pivot Table

Creating a pivot table with the column names inverted will help us calculate the growth of international students each year in the next section, where we find the growth and porcentage numbers.

<img src="images/018_pivot_table.png?raw=true"/>

<img src="images/018-5_pivot_table.png?raw=true"/>

### Growth Percentage of international students per year compared to 2015

By using a Windows Function like LAG, we can get the right numbers from the previous year and calculate the student's growth. We can as well use the same calculation and turn it into a porcentage, which will be useful for visualization purposes.

<img src="images/019_growth.png?raw=true"/>

<img src="images/019_growth_table.png?raw=true"/>

<img src="images/is_growth_hq.png?raw=true"/>

## International Students - Province Segmentation
This section of the study will be focused on the table called international_students_Province_Canada, which provides us with information about the different Canadian provinces international students have come to between 2015 and 2023. We also have data about gender per provinces.

### View Data from second table
In order to explore and organize our data, we need to take a look and understand it. This way we can find inconsistencies or errors we can clean in the process.

<img src="images/20_viewtable.png?raw=true"/>

### Delete headers from data
After taking a closer look at the data, I couldn't find any issues or mistakes. However, I did have issues importing the table into MySQL Workbench, specifically the headers becoming part of the data. This can be fixed using the following query:

<img src="images/21_delete_headers.png?raw=true"/>

### Province Distribution: 2015-2023

<img src="images/22_province_distribution.png?raw=true"/>

<img src="images/22-5_province_distribution_ss.png?raw=true"/>

<img src="images/is_map_hq.png?raw=true"/>

### Top 5 Provinces: 2015-2023

<img src="images/23_top5_provinces.png?raw=true"/>

<img src="images/23-5_top5_provinces_ss.png?raw=true"/>

### Bottom 5 provinces: 2015-2023

<img src="images/24_bottom5_provinces.png?raw=true"/>

<img src="images/24-5_bottom5_provinces.png?raw=true"/>

### Gender segmentation: 2015-2023

<img src="images/25_gendersegmentation_002.png?raw=true"/>

<img src="images/is_province.png?raw=true"/>

## Findings
Between 2015 and 2023, Canada received a total of 3,502,910 international students.

The number of international students went from 227,340 in 2015 to 594,670 in 2023, showing an increase of 161%.

The average number of students per year was 389,212.22.

The Top 5 International Students Nationalities between 2015 and 2023 are:

India: 1,131,605
People’s Republic of China: 644,030
Republic of Korea: 132,470
France: 127,870
Nigeria: 101,105

International Students from India were the group that grew the most, going from 32,465 in 2015 to 220,035 in 2023.
This shows an increase of 577.76%.

The Top 5 Provinces that hosted the most international students between 2015 and 2023 are:

Ontario: 1,677,535
British Columbia: 738,330
Quebec: 440,060
Alberta: 186,540
Manitoba: 102,455
