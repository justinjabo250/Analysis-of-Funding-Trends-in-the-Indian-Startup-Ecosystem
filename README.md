# Analysis-of-Funding-Trends-in-the-Indian-Startup-Ecosystem

![dataindian](https://user-images.githubusercontent.com/115732734/230741548-dee7968d-8722-4187-ac0a-82e6a9eccd79.gif)


# Project Description

The goal of this initiative is to provide information to important players who are considering entering the Indian startup ecosystem. In order to do this, we will examine important indicators of investment received by startups in India from 2018 to 2021. Management will make strategic business decisions using these information.

I created a hypothesis to test the dataset so that I might get a valid conclusion. In order to determine which industry is more likely to attract investment from investors, the data were analyzed in terms of technical and non-technology industries.

# Questions :

<ol type="1"style="font-size:20px;font-weight: bold;font-family: 'Times New Roman'"> 
    <li>what are the top five sectors where funding is maximum?</li>
    <li>what is the location with most starstup funded?</li>
    <li>what is the maximum amount of funding recieved by a startup?</li>
    <li>what is the most startups which has a potential or can attract more investor's to invest in?</li>
    <li>what is the total amount of funds each year?</li>
    <li>In which year did a startup recieve the highest amount of funding?</li>
    <li>Which stage receives more investment from investors for start-ups?</li>
    <li>Who makes the biggest investments among investors?</li>
    <li>Can the startup's age effect the amount of funding it receives from investors?</li>
</ol><br><br>

# Hypothesis :


I created the null and alternate hypotheses to concentrate on two groups: companies that are technology-biased and startups that are not technology-biased, in order to further evaluate and analyze the data. Hence, the following two hypotheses are presented:


**NULL:** It is unlikely that Indian startups in the technology industries will get funded.


**ALTERNATE:** Indian startups in the technology industries are likely to receive investment.


# Data preparation :


# Importing all Libraries :

<img width="925" alt="Screen Shot 2023-04-08 at 23 00 28" src="https://user-images.githubusercontent.com/115732734/230742466-0a1db365-2621-4c1d-ba40-d06ffba6304b.png">


# Data Loading :

<img width="916" alt="Screen Shot 2023-04-08 at 23 05 57" src="https://user-images.githubusercontent.com/115732734/230742544-d5581653-7de1-4b1f-9f88-2399d264b446.png">

# Exploratory Data Analysis: EDA :

Here,in this section, the datasets will be examined in-depth, presented, make hupotheses and thought about for cleaning, processing, and feature creation.

# DATA CLEANING :

In this section, the following properties of the data loaded will be analysed:

. Data Types
. Missing Data
. Categorical data values
. Continous data values
. Duplicated data
. Standard rule base check, that is, checks relating to industry standards, example email, dates, websites, currencies etc

<img width="1035" alt="Screen Shot 2023-04-08 at 23 09 43" src="https://user-images.githubusercontent.com/115732734/230742677-344d044d-eac0-439b-9a41-95d172897d16.png">

# Dataset overview :

Previewing Data sets and Providing Summary Information.

# Analysis Of The 2018 Data

# Column names and description: For the year 2018 :

# 2018 Dataset.

<img width="1029" alt="Screen Shot 2023-04-08 at 23 13 55" src="https://user-images.githubusercontent.com/115732734/230742795-d5693867-69ff-4060-a947-82cdab6190f1.png"><br>

<img width="1038" alt="Screen Shot 2023-04-08 at 23 15 34" src="https://user-images.githubusercontent.com/115732734/230742877-d8981cb2-27fe-47fd-be7b-8b1e27655643.png">

# To see the names of the columns in the dataset 

# Observation:

The following is observed about the columns in the data set with respect to the valiable columns and their order:

1. Company Name
2. Industry
3. Round/Series
4. Amount
5. Location
7. About Company


<img width="1030" alt="Screen Shot 2023-04-08 at 23 19 48" src="https://user-images.githubusercontent.com/115732734/230743002-0b355401-7b6d-4ccd-95a8-d1cacdec6a89.png">

# To know the total number of rows and columns repectively in the dataset

<img width="1024" alt="Screen Shot 2023-04-08 at 23 23 53" src="https://user-images.githubusercontent.com/115732734/230743109-6fd29e08-db0e-499b-baa8-6c84d272d327.png">


# To invetsigate the datatypes of the available fields or columns

# Observation:

It is observed that the "Amount" field which is supposed to be a continous data type is rather a string or an object, this has to be corrected

<img width="1031" alt="Screen Shot 2023-04-08 at 23 28 32" src="https://user-images.githubusercontent.com/115732734/230743237-c195dab2-e0aa-4d51-b39b-d32fd31ccfee.png">


# Dealing with Null Values

# Observation:

Initial check indicates there is no null value in the data set.

<img width="1024" alt="Screen Shot 2023-04-08 at 23 31 20" src="https://user-images.githubusercontent.com/115732734/230743333-c2b3d3f2-31b9-411b-8926-4abc146ca68a.png">


# Deep Dive Into the Data Set :

<img width="1040" alt="Screen Shot 2023-04-08 at 23 33 55" src="https://user-images.githubusercontent.com/115732734/230743435-dd341d9a-8dce-4978-bc63-4ba01e62d2c5.png">

# After carefully examining We note the following from the data shown above:


**The amount columns include cells with the symbol "-" as well as several currencies.**


**and the Industry columns is specified using more than one term.
**

**The Location is described using more than one physical address,**


**To clean these, we'll presume that the amounts with no indications are in dollars. As a result, we'll convert the numbers in INP to USD and swap out "-" for NaN.**


# Cleaning the 2018 Data Set :


# Renaming Columns to reflect consistency :

<img width="1042" alt="Screen Shot 2023-04-08 at 23 38 58" src="https://user-images.githubusercontent.com/115732734/230743602-d1b03ee4-59ef-4f46-ba05-3b368d2645f1.png">


### rename the column headings to be consistent with other data set

<img width="921" alt="Screen Shot 2023-04-08 at 23 41 43" src="https://user-images.githubusercontent.com/115732734/230743698-fb3e3e80-7f51-44df-84f1-59832181a769.png">


# Cleaning the Sector Column


### Cleaning the Sector column to get of multiple sectors represented as one. 

### This is done by first stipping and using slicing to select the first part.


<img width="1041" alt="Screen Shot 2023-04-08 at 23 44 30" src="https://user-images.githubusercontent.com/115732734/230743778-baedab7c-8727-4e9e-91b4-b14cfb14882f.png">


### Rename similar sectors with wrong or different spelling to make it consistent.

<img width="1037" alt="Screen Shot 2023-04-08 at 23 47 59" src="https://user-images.githubusercontent.com/115732734/230743939-e9706732-560e-4f32-9a58-c42144273a32.png">


### Using .unique() function finds the unique elements of an array and returns these unique elements as a sorted array.


<img width="934" alt="Screen Shot 2023-04-08 at 23 49 44" src="https://user-images.githubusercontent.com/115732734/230744054-11f823b4-9dad-417d-8d97-9f48883860ec.png">

# Cleaning the Stage Column

<img width="935" alt="Screen Shot 2023-04-08 at 23 54 41" src="https://user-images.githubusercontent.com/115732734/230744271-b876f46e-9bb9-4d8b-b98a-4538e6d0163d.png">

### Replacing similar stages with wrong or different spelling to make it consistent.

<img width="915" alt="Screen Shot 2023-04-08 at 23 55 31" src="https://user-images.githubusercontent.com/115732734/230744285-f419aac2-82bd-4f60-9797-c823beecf48a.png">


#### Using . loc() Function, . loc property of the DataFrame object allows the return of specified rows and/or columns from that DataFrame .

<img width="931" alt="Screen Shot 2023-04-09 at 00 02 08" src="https://user-images.githubusercontent.com/115732734/230744402-b02f48df-4b09-4540-a976-58599e3d7477.png">



### correcting the name of the sector from transportation to FinTech

<img width="936" alt="Screen Shot 2023-04-09 at 00 05 32" src="https://user-images.githubusercontent.com/115732734/230744493-cbb96b70-ce70-4379-a37e-db9736cc1c14.png">


### correcting the stage name to Unknown since there is no information

<img width="937" alt="Screen Shot 2023-04-09 at 00 05 59" src="https://user-images.githubusercontent.com/115732734/230744496-64c8a57f-33c6-4f9e-b61d-bb0208119e39.png">

### There is no further and better information concerning the stage column. This will be kept as it is.

<img width="931" alt="Screen Shot 2023-04-09 at 00 08 47" src="https://user-images.githubusercontent.com/115732734/230744573-6b5f0a6b-b755-4e51-9e53-ac83bba1463f.png">


# Cleaning the Amount($) Column


Since some of the currencies are in ₹ (rupees) and others in $ (dollars), the rupees are changed to dollars based on the current exchange rate.

Duty is to select all rows where 'Amount' column is in rupees.


##### Since some of the currencies are in ₹ (rupees) and others in $ (dollars), the rupees are changed to dollars


<img width="1027" alt="Screen Shot 2023-04-09 at 00 15 34" src="https://user-images.githubusercontent.com/115732734/230744760-018916c0-3003-47e9-a2d7-749a02647bff.png">


### Removing or stripping all special characters form the amount column.

<img width="933" alt="Screen Shot 2023-04-09 at 00 19 06" src="https://user-images.githubusercontent.com/115732734/230744950-a267e922-3e5c-4366-80e7-b0069668d7b9.png">


# Change the data type from a string to a float.

<img width="934" alt="Screen Shot 2023-04-09 at 00 19 32" src="https://user-images.githubusercontent.com/115732734/230744962-e39d66aa-21bf-43d7-a53b-864469409762.png">


# Convert the rows with rupees to dollars.

<img width="935" alt="Screen Shot 2023-04-09 at 00 21 03" src="https://user-images.githubusercontent.com/115732734/230744970-c0d6bc5c-c2a1-4e76-9351-c7c2e0c19486.png">


# Cleaning the HeadQuarter Column

### Strip the location data to only the city-area.


#### use ',' as the delimeter to separate them and select preferred choice with slicing.

<img width="941" alt="Screen Shot 2023-04-09 at 00 26 30" src="https://user-images.githubusercontent.com/115732734/230745171-9ba569ec-5f37-4729-8c27-1e63644fa4f8.png">


### Replacing wrongly spelt names and similar names entered differently.

<img width="937" alt="Screen Shot 2023-04-09 at 00 27 17" src="https://user-images.githubusercontent.com/115732734/230745175-ed1f5a91-593f-43ac-8f4e-c27e3699560d.png">

# Cleaned 2018 data.

<img width="942" alt="Screen Shot 2023-04-09 at 00 27 58" src="https://user-images.githubusercontent.com/115732734/230745181-5e2b6af1-07f7-4f9d-a0ce-b91cfe246186.png">












































































