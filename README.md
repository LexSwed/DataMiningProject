# DataMiningProject
Data mining project: https://docs.google.com/presentation/d/1veA_WQcfRRx7hQnE8qklmsLYceWzQGrPHrieSEWqcaI/edit#slide=id.g2a549964dd_29_0

# 1. Business understanding

## 1.1 Background

RateChain is an online network of car rental suppliers and brokers all connected to each other through just one link. It allows the supplier to load and electronically distribute their rental product including, locations, rates, terms and conditions, fleet information, ancillary product and stop sales to the broker, bookings can also be sent, received and confirmed or denied using the same link.
Since companies provide prices for a car class and not for a specific car model, RateChain helps to keep track of changes in class rates. These classes are defined using ACRISS - industry standard car classification code. It defines a car as a set of four characters in the way that vehicles inside one class have similar characteristics. However, the rules of how to classify a car are not strict that leads to a problem that the same car has different codes in different rental companies. For example cars with different ACRISS code may be equal alternatives for customer, When ideally the cars should have same ACRISS code. As a result, 
It becames difficult to monitor the prices.

## 1.2 Business goals

RateChain always improves the service it provides, to make life of brokers, rental companies and customers better. One of the opportunities to improve the quality of service is to improve the accuracy of monitoring rental car offers. If we classify it more accurately, the sales will increase by some percentage and RateChain will have more satisfied customers as well and members of this company will also increase.

## 1.3 Business success criteria

The real customers of Ratechain should judge if our improvement is really good or not. Only from them we will be able to see the real feedback of our work. Besides we can measure the sales before/after our changes and get the real percentage. If  the sales is increased by at least 5 percent, then it means that the changes worked.

## 2. Assessing

## 2.1 Inventory of resources

We have got old data of reservations, market prices, and rate quotes, also the contact person from the company and as a software we will use R.

## 2.2 Requirements, assumptions, and constraints

Our requirement is to finish the project before the deadline and also fulfill the requirements of the company by answering the questions they want to have the answers to.
Our  legal and security obligation is not to share the data provided by the company to other person, outside the team.

## 2.3 Risks and contingencies

The delay of the project completion may cause different things that we must avoid, they can be:
team does not have work environment for enough time, so the place where we can work whole day must be found;
for big data some commands may need too long time to run in R. So we must take into account that fact and start doing the project earlier;
with a lack of domain knowledge we could ask questions to the contact person, who may answer with some delay.

## 2.4 Terminology

Car class - ACRISS code assigned to the car model;
Active pricing - changing prices more often than other;
ACRISS - utilise an industry standard vehicle matrix to define car models ensuring a like to like comparison of vehicles. This easy-to-use matrix consists of four categories. Each position in the four character vehicle code represents a definable characteristic of the vehicle. The expanded vehicle matrix makes it possible to have 400 vehicle types. (http://acriss.org/car-codes.asp - ACRISS)


## 2.5 Costs and benefits
 
If we imagine that it is real project then:
Salaries for people included in the project. 3000 EURO for each.
Price for renting the space for working with the project including the utilities. 300 EURO
Benefits:
RateChain has increased income by 100 000 EURO  
However, as this is the project for the university, the costs are:
56 cups of coffee;
one pen;
one copybook;
18 dinners in university cafeteria
The benefits are:
RateChain will get a new glance of existing problems, questions and solutions

## 3. Data mining goals
## 3.1 Goals
Classify car rental offers more accurately for price comparison by using collected data
Find right ACRISS code for a car model based on collected data
Which car models can be considered as alternatives to each other from pricing perspective?
How manual and automatic gearbox affects rental price by car class?
What is price difference between car classes?
How much price per day varies based on rental duration?
Which car rental companies are using active pricing (changing prices more often than others)?

## 3.2 Success criteria

Success will be when the chosen classification model have the highest accuracy with the number of at least 95 %.

# 2. Data understanding

## 1.Gathering data

The data exists and is gathered in different CSV files which are easy to use. 
All the data we need to reach the goals are already given from the company, no need to find out more from other sources.
We have four CSV files which contains the information about reservations, market prices and rate quotes.

The most useful columns are:

acriss_code -  ACRISS code provided by reseller
car_class_name – Car class name by ACRISS. Equal with first letter of ACRISS code,
model_name – vehicle vendor and model name (usually provided as an example)
total_price –  total rental price,
price_per_day – rental price per day

The data  is compatible with our data-mining platform.

## 2. Describing data
As we have described above we have 4 CSV files and all of them contain important fields like car models, prices for this models per day and total rental price, also the history of reservations, pick up and returning dates of cars and the companies who used the service. 
We have all the data fields we may need to finish the project properly.

## 3. Exploring data
There are easily seen some fields that are not meaningful. We can consider them as NA values and filter out. Here are the steps to do:
replace all non-sensical values by missing values;
use NA to denote missing values
count how many rows are affected by each change

## 4. Verifying data quality
We have chosen this project because of the data quality, They are organized in an understandable manner.
Though, there are some fields that does not make any sense to have. In the fuel_type and drive_type fields there are many values unspecified. 
Besides the car model names are not written accurately. For example you will find lots of car models with the value : “Ford or similar”.
So to summarize there are some quality problems but in overall we can identify an adequate solution from it.

# 3. Planning 

List of tasks:
1. Investigate the data to find out patterns that might help to improve car rental offers classifier.
understand how monitoring works
find which cars differs in their ACRISS code
divide car rentals to classes by price and compare with ACRISS code classes
develop a classifier using available data for each car, to classify it to a some price class
2. Find out whether ACRISS code for a car model vary by countries and find “correct” code for car models.
detect same car models with different ACRISS code
find countries in which this varying occurs
find “correct” class for each model
3. Find cars that can be considered as alternatives to each other from pricing perspective. Using available data, build a classifier from model specification to a price class.
4. Determine how manual and automatic gearbox affects rental price by car class.
split cars by rental price and class
find out the difference
5. Find the price difference between car classes.
6. Find out how much price per day varies based on rental duration.
7. Find companies that use active pricing, so change prices very actively, perhaps based on prices monitoring from RateChain company.

