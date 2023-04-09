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




# Analysis Of The 2021 Data


# Column names and description: For the year 2021 :

<img width="938" alt="Screen Shot 2023-04-09 at 12 21 01" src="https://user-images.githubusercontent.com/115732734/230767434-1b92d237-15b2-48de-b0a8-c933a511839c.png">


# 2021 Dataset.

<img width="1040" alt="Screen Shot 2023-04-09 at 12 20 13" src="https://user-images.githubusercontent.com/115732734/230767443-09a60260-9ff3-4716-a370-ec456a2b67f7.png">



# Using .info() function


###### The info() method prints information about the DataFrame. The information contains the number of columns, column labels, column data types, memory usage, range index, and the number of cells in each column (non-null values). 

<img width="939" alt="Screen Shot 2023-04-09 at 12 28 02" src="https://user-images.githubusercontent.com/115732734/230767807-64c41cba-3463-41b6-8abe-1ebd6d7492e0.png">


# To see the names of the columns in the dataset.

<img width="936" alt="Screen Shot 2023-04-09 at 12 28 59" src="https://user-images.githubusercontent.com/115732734/230767818-28ef40e8-c549-47fe-a780-b591094a51d7.png">


# Using dfSummary()

##### A summary of the entire dataset. To create an organised and thorough summary of a dataframe, use dfsummary:

<img width="934" alt="Screen Shot 2023-04-09 at 12 29 55" src="https://user-images.githubusercontent.com/115732734/230767836-a630faa4-da4d-4e7a-9c7f-6bdb7e1c5d9c.png">


# Using isnull() Method.

##### The isnull() method returns a DataFrame object where all the values are replaced with a Boolean value True for NULL values, and otherwise False.


<img width="937" alt="Screen Shot 2023-04-09 at 02 26 08" src="https://user-images.githubusercontent.com/115732734/230748223-8e839b85-5e2c-48c4-9dbb-a82ce530b300.png">


# Deep Dive Into the Data Set :

## Cleaning the Founded Column:

<img width="934" alt="Screen Shot 2023-04-09 at 12 32 36" src="https://user-images.githubusercontent.com/115732734/230767855-f35308c3-5d18-4ccc-bbee-b715164b62a4.png">


# Convert the data type from float to a string.

<img width="936" alt="Screen Shot 2023-04-09 at 12 42 34" src="https://user-images.githubusercontent.com/115732734/230768344-0bf4ab4c-180f-4b99-9e85-604a188902ee.png">


# Changing the data type to numeric.

<img width="935" alt="Screen Shot 2023-04-09 at 12 43 21" src="https://user-images.githubusercontent.com/115732734/230768352-efe937b1-3bba-418a-92bd-48a731c2508c.png">


# Replacing nan with 2021

<img width="934" alt="Screen Shot 2023-04-09 at 12 44 11" src="https://user-images.githubusercontent.com/115732734/230768358-dd2819d1-d083-4aa9-aac0-3831795f6631.png">


# Cleaning the HeadQuarter Column

<img width="937" alt="Screen Shot 2023-04-09 at 12 45 04" src="https://user-images.githubusercontent.com/115732734/230768361-b15583d2-f29f-4e48-ae12-276b64b0cfdb.png">

## checking for the record with Information Technology & Services.

It is realized that the values at the Sector column and the HeadQuarter column has been interchanged. This is corrected in the cell below.


<img width="933" alt="Screen Shot 2023-04-09 at 12 46 05" src="https://user-images.githubusercontent.com/115732734/230768373-acc4d623-3f6c-464f-944d-4b6b08e520c8.png">


## Correcting the wrong placement of the HeadQuarter and Sector values

<img width="936" alt="Screen Shot 2023-04-09 at 12 55 28" src="https://user-images.githubusercontent.com/115732734/230769060-ea1fae27-3c44-40e6-aca1-e149fee3f568.png">


# Checking for the record with Online Media\t#REF!

<img width="938" alt="Screen Shot 2023-04-09 at 12 56 18" src="https://user-images.githubusercontent.com/115732734/230769071-ecde706e-8661-449d-828e-b6d8be0bbd86.png">


## Correcting the wrong placement of the HeadQuarter and Sector values:

<img width="937" alt="Screen Shot 2023-04-09 at 12 58 43" src="https://user-images.githubusercontent.com/115732734/230769083-f9667616-bfcb-4532-af51-2ffa4f4cd594.png">



# Checking for the record with Gurugram\t#REF

<img width="934" alt="Screen Shot 2023-04-09 at 13 00 04" src="https://user-images.githubusercontent.com/115732734/230769092-432e1f98-49f5-473f-bf07-bd4458177d45.png">



## Correcting the wrong placement of the HeadQuarter and Sector values

<img width="936" alt="Screen Shot 2023-04-09 at 13 00 53" src="https://user-images.githubusercontent.com/115732734/230769098-005ad45d-0e36-4b48-9423-3e5459bc99dd.png">



# Checking for the record with Food & Beverages

<img width="935" alt="Screen Shot 2023-04-09 at 13 01 52" src="https://user-images.githubusercontent.com/115732734/230769106-90164be4-9f9c-4b42-b922-e51fa40d1291.png">



# dropping the duplicate:

<img width="936" alt="Screen Shot 2023-04-09 at 13 02 30" src="https://user-images.githubusercontent.com/115732734/230769109-6c3f4024-fe48-4d08-94f4-d266d6f5fda1.png">




# Checking for the record with Computer Games

This investigation also revealed a duplicated entry. The second entry with index 111 will be dropped and then the correction will be done.

It also revealed that the amount and stage column has been interchanged.

<img width="934" alt="Screen Shot 2023-04-09 at 13 24 13" src="https://user-images.githubusercontent.com/115732734/230770180-3af33a0c-eb7a-4743-b085-d6930d84a851.png">



# Dropping the duplicate

<img width="938" alt="Screen Shot 2023-04-09 at 13 25 24" src="https://user-images.githubusercontent.com/115732734/230770190-0ec663bd-45b9-44f9-97f8-fd95a126570e.png">


# Checking for the record with Pharmaceuticals\t#REF!

<img width="937" alt="Screen Shot 2023-04-09 at 13 26 08" src="https://user-images.githubusercontent.com/115732734/230770201-2d8e7228-64ed-47cb-8e25-b6582d8a416c.png">


# Dropping the duplicate

<img width="933" alt="Screen Shot 2023-04-09 at 13 27 03" src="https://user-images.githubusercontent.com/115732734/230770216-ea3e193b-3182-4a01-bdeb-73fe2cccc78b.png">


# Replacing HeadQuarter with cleaned City name

<img width="936" alt="Screen Shot 2023-04-09 at 13 28 08" src="https://user-images.githubusercontent.com/115732734/230770226-49d67683-31cd-4d19-9612-a20554022cc0.png">




# Cleaning the Sector Column

<img width="938" alt="Screen Shot 2023-04-09 at 13 40 04" src="https://user-images.githubusercontent.com/115732734/230770734-f0853db9-c0b8-4999-94ee-b7a74f70dfcc.png">


## Rename similar sectors with wrong or different spelling

<img width="937" alt="Screen Shot 2023-04-09 at 13 41 06" src="https://user-images.githubusercontent.com/115732734/230770743-1bf4edc3-d960-434c-86cc-7bb788e8c83b.png">


# Using .unique()

<img width="937" alt="Screen Shot 2023-04-09 at 13 41 53" src="https://user-images.githubusercontent.com/115732734/230770748-154a7df4-44cc-40f8-9e75-d3bc500b7d06.png">


# Replacing nan with unknown

<img width="940" alt="Screen Shot 2023-04-09 at 13 42 46" src="https://user-images.githubusercontent.com/115732734/230770759-b33f0602-f0f0-46cd-9757-c24e35c1bb4e.png">



# Cleaning the Stage Column

<img width="935" alt="Screen Shot 2023-04-09 at 13 52 09" src="https://user-images.githubusercontent.com/115732734/230771477-566b4b52-b28b-45dc-a06b-229665e89fb5.png">


# Rename similar Stage with wrong or different spelling

<img width="938" alt="Screen Shot 2023-04-09 at 13 53 18" src="https://user-images.githubusercontent.com/115732734/230771488-13a84478-6185-44d6-bdd8-5c105225130d.png">


# Using .unique()

<img width="935" alt="Screen Shot 2023-04-09 at 13 54 14" src="https://user-images.githubusercontent.com/115732734/230771497-f89a6e09-ebcc-45e8-a42a-6acc6e6c7c2e.png">



## checking for the record with $300000 at the Stage column

<img width="937" alt="Screen Shot 2023-04-09 at 13 55 07" src="https://user-images.githubusercontent.com/115732734/230771503-6b843ce6-6f62-49c3-ad26-aac07717703c.png">



## correcting the wrong placement of the HeadQuarter and Sector values

<img width="933" alt="Screen Shot 2023-04-09 at 13 56 06" src="https://user-images.githubusercontent.com/115732734/230771513-928bda6a-0819-41d4-8669-b370d313b703.png">


## checking for the record with $6000000 at the Stage column

<img width="937" alt="Screen Shot 2023-04-09 at 13 56 57" src="https://user-images.githubusercontent.com/115732734/230771524-f557c0b0-6816-452e-9ed0-78b3c459161e.png">


## correcting the wrong placement of the HeadQuarter and Sector values

<img width="934" alt="Screen Shot 2023-04-09 at 13 58 00" src="https://user-images.githubusercontent.com/115732734/230771852-e8caac2e-684f-4eb4-a602-019cbb61027f.png">


## checking for the record with $1000000 at the Stage column

<img width="935" alt="Screen Shot 2023-04-09 at 13 58 44" src="https://user-images.githubusercontent.com/115732734/230771790-defbe07a-e6e3-4e81-ab6f-6fbd5d498345.png">


## Correcting the wrong placement of the HeadQuarter and Sector values

<img width="937" alt="Screen Shot 2023-04-09 at 14 15 02" src="https://user-images.githubusercontent.com/115732734/230772159-f40fa859-0d48-4dd8-bf2e-928b203fe961.png">


# Using .unique()

<img width="936" alt="Screen Shot 2023-04-09 at 14 15 51" src="https://user-images.githubusercontent.com/115732734/230772166-3bff25cd-8f46-4430-9a89-9226d124f98b.png">


# Replacing nan with unknown

<img width="936" alt="Screen Shot 2023-04-09 at 14 16 34" src="https://user-images.githubusercontent.com/115732734/230772168-323e39a6-1ba3-4172-9295-0760125ec5f7.png">




# Cleaning the Amount($) Column

<img width="934" alt="Screen Shot 2023-04-09 at 14 26 18" src="https://user-images.githubusercontent.com/115732734/230773461-b75ee2a3-a0d6-4baf-a42a-4f767c440b52.png">



# Using .unique()

Values such as Undisclosed, Series C, Seed,$Undisclosed, $undisclosed, Pre-series A all wrongly entered into the Amount($) column. This will have to be investigated and corrected.

<img width="935" alt="Screen Shot 2023-04-09 at 14 26 56" src="https://user-images.githubusercontent.com/115732734/230773466-e87570f9-2f66-42ba-9794-bdb8aeeb9dc4.png">


# Checking for undisclosed in the amount column:

The invetsigation output above revealed that none of the records had the amount wrongly entered in a different column. It is obvious that the amount was not disclosed. Theey are replace with 0.


<img width="936" alt="Screen Shot 2023-04-09 at 14 29 14" src="https://user-images.githubusercontent.com/115732734/230773474-32eb1dc8-b56a-4a89-bef0-2aae269b3bda.png">



# Replacing the Undisclosed with nan

<img width="935" alt="Screen Shot 2023-04-09 at 14 31 14" src="https://user-images.githubusercontent.com/115732734/230773490-952c43f1-980c-478f-932c-2ffcd997f0e1.png">


# Checking for $Undisclosed in the amount column:

<img width="935" alt="Screen Shot 2023-04-09 at 14 32 50" src="https://user-images.githubusercontent.com/115732734/230773500-bed0175c-fd23-448b-9a5e-de52cb444c3e.png">


# Replacing the $undisclosed with 0

<img width="935" alt="Screen Shot 2023-04-09 at 14 34 04" src="https://user-images.githubusercontent.com/115732734/230773512-d1843dbc-8f1c-461d-b024-873cc068988a.png">


# Checking for Series C in the amount column

<img width="937" alt="Screen Shot 2023-04-09 at 14 35 25" src="https://user-images.githubusercontent.com/115732734/230773523-0fe3aba4-2e5b-4e14-ace8-e88596e39f87.png">


### correcting the wrong placement of the HeadQuarter and Sector values

<img width="937" alt="Screen Shot 2023-04-09 at 14 37 03" src="https://user-images.githubusercontent.com/115732734/230773536-aa975914-704c-4e85-8177-ecb23256f175.png">



# checking for Seed in the amount column

The output of the investigation shows that two records were involved with this error. The stage, investor and Amount columns were interchanged. This is corrected in the code below.

<img width="938" alt="Screen Shot 2023-04-09 at 15 05 14" src="https://user-images.githubusercontent.com/115732734/230774343-73b68d6d-aafd-4ca0-8de0-450670b8be38.png">



### correcting the wrong placement of the HeadQuarter and Sector values

<img width="935" alt="Screen Shot 2023-04-09 at 15 05 47" src="https://user-images.githubusercontent.com/115732734/230774355-a40bfc8c-f135-4730-8466-236474beefad.png">



# Checking for Pre-series A in the amount column

The invetsor, Amount, and stage columns has been interchanged. The Sector column will be renamed to be consistent with others.

This is correcetd in the code below.


<img width="937" alt="Screen Shot 2023-04-09 at 14 42 53" src="https://user-images.githubusercontent.com/115732734/230773874-76a7ae4b-9621-451f-9008-0245ef93b7fe.png">



### First change the data type to a string to work on the special characters


<img width="933" alt="Screen Shot 2023-04-09 at 14 45 00" src="https://user-images.githubusercontent.com/115732734/230773887-ca84cf12-6425-4ca7-88f9-fedb2a4e49af.png">



# Removing all special characters in the colum

<img width="936" alt="Screen Shot 2023-04-09 at 14 45 29" src="https://user-images.githubusercontent.com/115732734/230773893-1846f947-29d7-4ec4-b896-53152ff1eb31.png">



# change the data type to a float

<img width="933" alt="Screen Shot 2023-04-09 at 14 46 20" src="https://user-images.githubusercontent.com/115732734/230773904-2b8b223f-add8-4b95-9695-6f7d3a5b89c6.png">


# Replacing nan with median

<img width="933" alt="Screen Shot 2023-04-09 at 14 46 54" src="https://user-images.githubusercontent.com/115732734/230773914-e78bff84-a005-403a-beea-9271f1a700c2.png">

<br>


# Cleaning the Founders Column

<img width="933" alt="Screen Shot 2023-04-09 at 15 10 11" src="https://user-images.githubusercontent.com/115732734/230775012-a4183592-a14d-4503-9f0b-d35f9b918b76.png">



# All nan values are to be filled with unknown on the


<img width="933" alt="Screen Shot 2023-04-09 at 15 10 50" src="https://user-images.githubusercontent.com/115732734/230775017-d7e6272d-037d-4d6e-8558-b171374bcb3c.png">



<br>

# Cleaning the Investor Column


## All nan values are to be filled with unknown on the

<img width="938" alt="Screen Shot 2023-04-09 at 15 13 06" src="https://user-images.githubusercontent.com/115732734/230775022-528392e1-b4ce-4028-bb99-519270533ee7.png">



# Checking for duplicate entries

<img width="936" alt="Screen Shot 2023-04-09 at 15 13 48" src="https://user-images.githubusercontent.com/115732734/230775029-2f98bdba-fc1f-4a07-b772-a0d3ab59fef6.png">



# Remove the duplicate record


<img width="935" alt="Screen Shot 2023-04-09 at 15 14 25" src="https://user-images.githubusercontent.com/115732734/230775039-f062ea16-54a5-420d-833f-e647034e7e02.png">



# Checking for null values

<img width="936" alt="Screen Shot 2023-04-09 at 15 15 02" src="https://user-images.githubusercontent.com/115732734/230775048-2016c968-0ebb-49f3-8148-0209808af06c.png">


# Cleaned 2021 data.

<img width="937" alt="Screen Shot 2023-04-09 at 16 47 58" src="https://user-images.githubusercontent.com/115732734/230779731-654ed445-c2d9-4776-bee6-6a107d02e9da.png">

<br>



## Combining the Various Data Sets 2018, 2019, 2020, 2021 into one

### Creating a variable to hold the different dataframes

### Concatenating the varibale holding the various dataframes

<img width="935" alt="Screen Shot 2023-04-09 at 16 51 37" src="https://user-images.githubusercontent.com/115732734/230780633-1729e388-f011-4b83-8c0d-6d46e4ca0196.png">

<br>

<img width="937" alt="Screen Shot 2023-04-09 at 16 56 12" src="https://user-images.githubusercontent.com/115732734/230780652-919011ca-719a-4704-9db6-27e283d341d9.png">

# Using .shape()

<img width="936" alt="Screen Shot 2023-04-09 at 16 57 01" src="https://user-images.githubusercontent.com/115732734/230780678-e535a6d0-47f6-43c9-b459-c571c8d609da.png">

<br>

## Saving the combined data set as a new file and reloading it for analysis

saving the new dataframe after concatenation in order to have it work on it without having to change the other datasets

<img width="934" alt="Screen Shot 2023-04-09 at 16 59 42" src="https://user-images.githubusercontent.com/115732734/230780705-80753e19-a453-49c2-a33e-f5707040422a.png">

<br>

<img width="937" alt="Screen Shot 2023-04-09 at 17 00 26" src="https://user-images.githubusercontent.com/115732734/230780731-acd1077a-9a3f-44fb-bdd5-5e06028bccbd.png">



<br>


# Exploratory Data Analysis (EDA)


# dropping unwanted column


<img width="933" alt="Screen Shot 2023-04-09 at 17 21 05" src="https://user-images.githubusercontent.com/115732734/230781501-5ebb5ad5-af21-4c1e-9367-6661514a0cf7.png">

<br>

<img width="935" alt="Screen Shot 2023-04-09 at 17 21 56" src="https://user-images.githubusercontent.com/115732734/230781511-3e1b1e6d-15ba-4dcf-ad87-9215a9630c3f.png">


# Using dfSummary

This summary output revelas one duplicated entry after merging the four data sets as one. The duplicate has to be dropped. Since the initial 2018 data set did not have the Founders and Investor columns, it has been filled with nan. The cleaned records are identified with Unknown.


<img width="936" alt="Screen Shot 2023-04-09 at 17 25 10" src="https://user-images.githubusercontent.com/115732734/230781702-cfd6a759-d957-4092-a7d9-400ba10164c4.png">


# Confirming checks for duplicate entries

<img width="935" alt="Screen Shot 2023-04-09 at 17 34 13" src="https://user-images.githubusercontent.com/115732734/230782168-02959144-adfa-4598-bf30-9c31c47a584f.png">



# Visually Inspecting Missing Data

The heatmap indicate a clustered missing values for the founders and Investors column. This is as a result of the 2018 data set not having values for this field before the data set merge.


<img width="937" alt="Screen Shot 2023-04-09 at 17 33 29" src="https://user-images.githubusercontent.com/115732734/230782172-598e056a-c778-4649-94fc-8989bc2f6c95.png">



# Univariate Analysis


## Analysis on The `Amount($)` Column

<img width="937" alt="Screen Shot 2023-04-09 at 17 38 13" src="https://user-images.githubusercontent.com/115732734/230782918-bdf06ed5-78c3-416e-a0b9-c6330d83cd8e.png">


# Calculate basic statistical measures


<img width="936" alt="Screen Shot 2023-04-09 at 17 46 13" src="https://user-images.githubusercontent.com/115732734/230782927-c1357dc6-eca9-4c8e-a30e-e970bcd6d2bd.png">


The above metrics are visually inspected with a box plot below.

<img width="938" alt="Screen Shot 2023-04-09 at 17 48 45" src="https://user-images.githubusercontent.com/115732734/230782938-303f133b-4bb5-452e-860f-59b0f4f03a39.png">


# calculate z-scores

<img width="937" alt="Screen Shot 2023-04-09 at 18 00 06" src="https://user-images.githubusercontent.com/115732734/230783449-d806821a-0bb3-4840-b922-6d3da835ae0c.png">

<br>


<img width="936" alt="Screen Shot 2023-04-09 at 17 59 06" src="https://user-images.githubusercontent.com/115732734/230783470-04f0f368-d042-4895-a058-60e597a3e8b1.png">


# find the indices of the outliers

<img width="935" alt="Screen Shot 2023-04-09 at 18 03 44" src="https://user-images.githubusercontent.com/115732734/230783870-6f88da76-f7d5-4e1a-9598-2fc13a2c154d.png">

<br>

<img width="935" alt="Screen Shot 2023-04-09 at 18 05 39" src="https://user-images.githubusercontent.com/115732734/230783909-f11e9661-a4d5-436c-b56f-5cd6973fc5b2.png">



# Remove the outliers

<img width="935" alt="Screen Shot 2023-04-09 at 18 06 35" src="https://user-images.githubusercontent.com/115732734/230783945-cd8c6fb7-258f-4a1f-99a3-71ce3f4d7f7e.png">

There seem to be more outliers which has the potential of distorting the mean. The median will however be less affected.

<img width="938" alt="Screen Shot 2023-04-09 at 18 07 54" src="https://user-images.githubusercontent.com/115732734/230783980-ed8e4194-c491-44cd-b8aa-c82b26fe7a04.png">



# Analysis of the `Stage` Column

<img width="938" alt="Screen Shot 2023-04-09 at 18 21 07" src="https://user-images.githubusercontent.com/115732734/230784717-02b0e3dd-f7db-4fb5-b74f-aaf4e974fe75.png">

The high count of unnknowns is as a result of the 2018 data set. The info above is in percentage terms. This is graphically represented in the graph below.

<img width="935" alt="Screen Shot 2023-04-09 at 18 21 58" src="https://user-images.githubusercontent.com/115732734/230784726-adf89813-176b-4570-86cd-ee194c6eadff.png">



# Analysis of the Sector Column

The FinTech sector has the highest percentage of 9.2%, followed by Healthcare 6.8% etc. This is also represented graphically below.

<img width="937" alt="Screen Shot 2023-04-09 at 18 22 39" src="https://user-images.githubusercontent.com/115732734/230784735-5ed78549-b049-4ea5-ad96-087f12e21236.png">


Since there are about 90 different sectors, it will not be ideal to represent them all on a graph as it will not be visually appeaing, there compromising on undesrtanding. Futher analysis will sort either the top 120 or the least 10 for analysis

<img width="933" alt="Screen Shot 2023-04-09 at 18 23 18 1" src="https://user-images.githubusercontent.com/115732734/230784837-99139344-d0b8-444a-9dc7-91bd6cbcc7a7.png">


# Analysis of the Founded Column


<img width="938" alt="Screen Shot 2023-04-09 at 18 24 05" src="https://user-images.githubusercontent.com/115732734/230784746-9affd44a-9e9d-4deb-b937-d62a25fcca73.png">



















































