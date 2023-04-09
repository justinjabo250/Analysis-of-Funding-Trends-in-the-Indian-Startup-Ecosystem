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

### To know the total number of rows and columns repectively in the dataset

<img width="1024" alt="Screen Shot 2023-04-08 at 23 23 53" src="https://user-images.githubusercontent.com/115732734/230743109-6fd29e08-db0e-499b-baa8-6c84d272d327.png">


### To invetsigate the datatypes of the available fields or columns

# Observation:

It is observed that the "Amount" field which is supposed to be a continous data type is rather a string or an object, this has to be corrected

<img width="1031" alt="Screen Shot 2023-04-08 at 23 28 32" src="https://user-images.githubusercontent.com/115732734/230743237-c195dab2-e0aa-4d51-b39b-d32fd31ccfee.png">


# Dealing with Null Values

# Observation:

Initial check indicates there is no null value in the data set.

<img width="1024" alt="Screen Shot 2023-04-08 at 23 31 20" src="https://user-images.githubusercontent.com/115732734/230743333-c2b3d3f2-31b9-411b-8926-4abc146ca68a.png">


# Deep Dive Into the Data Set :

<img width="1040" alt="Screen Shot 2023-04-08 at 23 33 55" src="https://user-images.githubusercontent.com/115732734/230743435-dd341d9a-8dce-4978-bc63-4ba01e62d2c5.png">

### After carefully examining We note the following from the data shown above:


**The amount columns include cells with the symbol "-" as well as several currencies.**


**and the Industry columns is specified using more than one term.
**

**The Location is described using more than one physical address,**


**To clean these, we'll presume that the amounts with no indications are in dollars. As a result, we'll convert the numbers in INP to USD and swap out "-" for NaN.**


# Cleaning the 2018 Data Set :


# Renaming Columns to reflect consistency :

<img width="1042" alt="Screen Shot 2023-04-08 at 23 38 58" src="https://user-images.githubusercontent.com/115732734/230743602-d1b03ee4-59ef-4f46-ba05-3b368d2645f1.png">


### Rename the column headings to be consistent with other data set

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





<br><br>

# Analysis Of The 2019 Data.



### Column names and description: For the year 2019 :



# 2019 Dataset.


<img width="945" alt="Screen Shot 2023-04-09 at 00 50 07" src="https://user-images.githubusercontent.com/115732734/230745773-b0fa2332-5e4b-4bfa-a5b2-4daea420ebed.png">


# Using .info() function


###### The info() method prints information about the DataFrame. The information contains the number of columns, column labels, column data types, memory usage, range index, and the number of cells in each column (non-null values). 

<img width="1037" alt="Screen Shot 2023-04-09 at 01 07 56 1" src="https://user-images.githubusercontent.com/115732734/230746279-f655b792-1fad-4e9c-8505-dead334b26d5.png">

# To see the names of the columns in the dataset

<img width="1029" alt="Screen Shot 2023-04-09 at 01 09 28" src="https://user-images.githubusercontent.com/115732734/230746281-38162988-2cce-45b9-ab74-2e6bfcd770d6.png">


# Using dfSummary()

##### A summary of the entire dataset. To create an organised and thorough summary of a dataframe, use dfsummary:

<img width="1037" alt="Screen Shot 2023-04-09 at 01 19 35 1" src="https://user-images.githubusercontent.com/115732734/230746679-fa1f809e-89df-4aac-bdde-ca14c10fb4fe.png">


# Using isnull() Method.

##### The isnull() method returns a DataFrame object where all the values are replaced with a Boolean value True for NULL values, and otherwise False.

<img width="1045" alt="Screen Shot 2023-04-09 at 01 20 32" src="https://user-images.githubusercontent.com/115732734/230746686-8e76a35c-7f46-4c55-a52f-23cfcd0305cb.png">


# Deep Dive Into the Data Set :


# Cleaning the Founded Column.


# convert the data type from float to a string.


##### convert the data type from float to a string.


<img width="938" alt="Screen Shot 2023-04-09 at 01 33 00" src="https://user-images.githubusercontent.com/115732734/230746848-8bf53dda-4434-4bf0-98ec-644cc7cf9697.png">

<br>

# Cleaning the HeadQuarter Column

<img width="938" alt="Screen Shot 2023-04-09 at 01 35 41" src="https://user-images.githubusercontent.com/115732734/230746915-c40b674d-7763-4ffe-ba04-dda36fd20fc4.png">


## Replacing wrongly spelt names and similar names entered differently.

<img width="937" alt="Screen Shot 2023-04-09 at 02 15 07" src="https://user-images.githubusercontent.com/115732734/230747866-3acd3a45-4be0-47d0-a8b5-c6d2bbc317cc.png">


# Cleaning the Sector Column.

<img width="1135" alt="Screen Shot 2023-04-09 at 01 38 41" src="https://user-images.githubusercontent.com/115732734/230747099-efe6b544-5ca6-4289-a222-afa66c86890d.png">


## Rename similar sectors with wrong or different spelling.

<img width="964" alt="Screen Shot 2023-04-09 at 01 39 31" src="https://user-images.githubusercontent.com/115732734/230747103-5fdef53d-6e46-4bd6-8682-315e3bb12941.png">


# Cleaning the Amount($) Column


<img width="944" alt="Screen Shot 2023-04-09 at 01 40 13" src="https://user-images.githubusercontent.com/115732734/230747108-34ddae66-60e5-41d7-888a-e376a9d0a1d4.png">

# Change the data type to a float.


<img width="945" alt="Screen Shot 2023-04-09 at 01 40 51" src="https://user-images.githubusercontent.com/115732734/230747125-66c32b11-2119-428d-a889-1e8bb148ad1d.png">


# Cleaning the Stage Column.

<img width="934" alt="Screen Shot 2023-04-09 at 01 53 54" src="https://user-images.githubusercontent.com/115732734/230747375-4d8e97e8-4358-4985-8bd9-d39caff63b5a.png">


# Replacing wrongly spelt and similar enteries.

<img width="934" alt="Screen Shot 2023-04-09 at 01 54 31" src="https://user-images.githubusercontent.com/115732734/230747380-55e66616-7f17-4de1-9aee-11acac692b85.png">


# Cleaned 2019 data.

<img width="1031" alt="Screen Shot 2023-04-09 at 01 56 06" src="https://user-images.githubusercontent.com/115732734/230747383-e93ce38a-4733-4c53-84af-a84235eebf59.png">

<br>
</br>

# Analysis Of The 2020 Data.


# Column names and description: For the year 2020 :



# 2020 Dataset.


<img width="1035" alt="Screen Shot 2023-04-09 at 02 00 38" src="https://user-images.githubusercontent.com/115732734/230747498-629fb147-64e1-4ae4-8faf-4c42061577d1.png">

<br>
<img width="938" alt="Screen Shot 2023-04-09 at 02 01 37" src="https://user-images.githubusercontent.com/115732734/230747504-f02da312-edaa-40e0-b2a3-99135114a3ac.png">



-----------


# Using .info() function


###### The info() method prints information about the DataFrame. The information contains the number of columns, column labels, column data types, memory usage, range index, and the number of cells in each column (non-null values). 

<img width="1044" alt="Screen Shot 2023-04-09 at 02 24 12" src="https://user-images.githubusercontent.com/115732734/230748153-1a33b560-e39f-4487-a5fa-e9e3d671ac9f.png">


# To see the names of the columns in the dataset.

<img width="935" alt="Screen Shot 2023-04-09 at 02 37 54" src="https://user-images.githubusercontent.com/115732734/230748401-cf735d79-b0b6-4d1f-ad67-d4a4e8f8df9b.png">


# Using dfSummary()

##### A summary of the entire dataset. To create an organised and thorough summary of a dataframe, use dfsummary:

<img width="1041" alt="Screen Shot 2023-04-09 at 02 25 03" src="https://user-images.githubusercontent.com/115732734/230748259-619f6daf-b35d-4773-aab7-935fc246ef05.png">


# Using isnull() Method.

##### The isnull() method returns a DataFrame object where all the values are replaced with a Boolean value True for NULL values, and otherwise False.


<img width="937" alt="Screen Shot 2023-04-09 at 02 26 08" src="https://user-images.githubusercontent.com/115732734/230748223-8e839b85-5e2c-48c4-9dbb-a82ce530b300.png">



# Deep Dive Into the Data Set :


<img width="936" alt="Screen Shot 2023-04-09 at 02 27 22" src="https://user-images.githubusercontent.com/115732734/230748241-0e4eb972-78c2-4ee0-95a7-c6fde092975b.png">


## Replacing all record with unknown dates with 2020

<img width="936" alt="Screen Shot 2023-04-09 at 02 28 08" src="https://user-images.githubusercontent.com/115732734/230748282-418d1dac-2f32-4666-a490-9a6f69f3851a.png">


# Cleaning the HeadQuarter Column.

<img width="1038" alt="Screen Shot 2023-04-09 at 02 41 38" src="https://user-images.githubusercontent.com/115732734/230748633-8566021b-7ed6-4cfe-ae72-f147ddc672a7.png">


# Strip and select only the City name.

<img width="937" alt="Screen Shot 2023-04-09 at 02 42 15" src="https://user-images.githubusercontent.com/115732734/230748635-2fd124a1-44c3-4464-9745-b5f44102fd99.png">


# Replacing wrongly spelt names and similar names.

<img width="939" alt="Screen Shot 2023-04-09 at 02 43 03" src="https://user-images.githubusercontent.com/115732734/230748639-82ef3b6a-4553-4ccf-bdeb-0dd870bdbf1d.png">


# Cleaning the Sector Column.

<img width="1027" alt="Screen Shot 2023-04-09 at 02 44 00" src="https://user-images.githubusercontent.com/115732734/230748641-2c46111d-b0ed-44af-bfb1-91f6d7bba1fe.png">



# Rename similar sectors with wrong or different spelling.

<img width="937" alt="Screen Shot 2023-04-09 at 03 00 08" src="https://user-images.githubusercontent.com/115732734/230748962-2b39aba4-b183-4a46-85bd-48c0dcb8b001.png">

# . Unique(). Methode

<img width="938" alt="Screen Shot 2023-04-09 at 02 53 04" src="https://user-images.githubusercontent.com/115732734/230748957-216bdd3d-ffa7-4a32-994e-82ea3d3e0d87.png">


# Cleaning the Amount($) Column.


### Changing the data type to a string.

<img width="936" alt="Screen Shot 2023-04-09 at 03 11 00" src="https://user-images.githubusercontent.com/115732734/230749390-581bb692-e32a-42b9-9432-d0c6e40ec0ee.png">



# Retrieveing records with 'Undiclsosed'

<img width="937" alt="Screen Shot 2023-04-09 at 03 11 37" src="https://user-images.githubusercontent.com/115732734/230749395-7e2109f4-4586-44bd-9014-179ebbdb179d.png">


# Correcting the name of the Amount($) from 'Undiclsosed' to 0

<img width="935" alt="Screen Shot 2023-04-09 at 03 12 39" src="https://user-images.githubusercontent.com/115732734/230749406-14e34e7b-c5f6-470d-b74d-9f2d0b38d4a7.png">


# Retrieveing records with Undislosed.

<img width="939" alt="Screen Shot 2023-04-09 at 03 13 43" src="https://user-images.githubusercontent.com/115732734/230749408-61727812-4a6b-4cd3-bb0c-6e5140ab11a8.png">



# Correcting the name of the Amount($) from Undislosed to 0

<img width="932" alt="Screen Shot 2023-04-09 at 03 25 57" src="https://user-images.githubusercontent.com/115732734/230749597-e6d3f671-ef28-49dd-8539-9de3a6757d65.png">

# Retrieveing records with Undisclosed.

<img width="939" alt="Screen Shot 2023-04-09 at 03 26 36" src="https://user-images.githubusercontent.com/115732734/230749599-bdffb892-3b18-472e-a03d-2f32f25971de.png">

# Replacing all Undisclosed.

<img width="934" alt="Screen Shot 2023-04-09 at 03 33 34" src="https://user-images.githubusercontent.com/115732734/230749836-00be8197-343e-4256-8a77-e08de39918b2.png">

# Replacing all 'nan' with 0

<img width="930" alt="Screen Shot 2023-04-09 at 03 34 20" src="https://user-images.githubusercontent.com/115732734/230749838-8c04eef9-2e16-4089-8de6-86e5fd868390.png">


# Removing all special characters.

<img width="939" alt="Screen Shot 2023-04-09 at 03 34 55" src="https://user-images.githubusercontent.com/115732734/230749841-cde8aba8-c25b-4f3d-a16b-7baef07dc948.png">

# Change the data type to a float.

<img width="935" alt="Screen Shot 2023-04-09 at 03 35 52" src="https://user-images.githubusercontent.com/115732734/230749843-8a7a9d47-e2e9-4836-91e3-367552f39835.png">


# Cleaning the Stage Column.

<img width="934" alt="Screen Shot 2023-04-09 at 03 41 21" src="https://user-images.githubusercontent.com/115732734/230750008-71717300-52be-4d0a-ab57-e46f6aa55d52.png">


# Replacing wrongly spelt and similar enteries.

<img width="936" alt="Screen Shot 2023-04-09 at 03 42 18" src="https://user-images.githubusercontent.com/115732734/230750013-c3bcbcaa-4c77-41f6-83d1-27f76a9c3551.png">


# Replacing all 'nan' with Unknown.

<img width="932" alt="Screen Shot 2023-04-09 at 03 43 00" src="https://user-images.githubusercontent.com/115732734/230750017-43a7cb17-3c63-4c8b-b315-07971d45eb61.png">


# Cleaning the Investor Column.


## All nan values are to be filled with unknown.

<img width="938" alt="Screen Shot 2023-04-09 at 03 48 17" src="https://user-images.githubusercontent.com/115732734/230750214-b9821afe-08a1-4b2e-92aa-b85ed49069a3.png">


# Checking for duplicate entries.

<img width="933" alt="Screen Shot 2023-04-09 at 03 49 07" src="https://user-images.githubusercontent.com/115732734/230750217-8f446fe4-b803-4e96-b519-5981a6b0779c.png">


# Remove the duplicate record.

<img width="938" alt="Screen Shot 2023-04-09 at 03 49 49" src="https://user-images.githubusercontent.com/115732734/230750221-353c7bb6-8f1a-4534-83df-62f683ba28e7.png">



# Cleaned 2020 data.

<img width="935" alt="Screen Shot 2023-04-09 at 03 50 36" src="https://user-images.githubusercontent.com/115732734/230750229-1db2d35f-1334-49cb-9804-622c0248128c.png">


------------





























































