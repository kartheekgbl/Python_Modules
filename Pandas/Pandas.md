# Pandas

## What is data science

data science or data analytics is a process of analyzing lardge set of data points to get answers on questions related to that data set

## What is pandas

pandas is a python module that makes data science easy and effective

## Concepts in Pandas

1. Installation of pandas
2. Importing pandas
3. How to download dataset
4. Creating data frame
5. Indexing & Slicing
6. Understanding LOC & ILOC
7. Sorting Dataframe
8. Handling missing Data
9. Data filtring and Conitional Changes
10. export dataftrame

## 1. Introduction

- Pandas is a software library written for the Python lrogamming language for data manipulation and analysis
- Tha pandas library mainly works with the tablar data
- Pandas is capable of offering an in-memory 2nd table object called Dataframe
- Main used two datastuctures Series, Dataframe and Panel
- simply, series is similar to a single column of data while dataframe is similar to sheet with rows and columns

### Datastuctures in pandas

1. Series -- 1 Dimentinal
2. Dataframe -- 2 Dimentional
3. Panel -- 3 Dimentional

- A data set is a collection of data

### Load data from excel

we pass the sheet_name also

    d=pd.read_excel("C:\\Users\\surya\\OneDrive\\Desktop\\pandas\\for_pandas.xlsx",sheet_name="kartheek")
    df1=pd.DataFrame(d)
    print(df1)

- have to install openpyxls in pip
- read_excel("file_location")

### Load data from CSV file

- read_csv("file_location")

### Create a dataframe using Dictionary

    di={"Name":["abc","def","ghi"],"Roll_no":[1,2,3],"price"=[20,30,40]}
    df2=pd.DataFrame(di)
    print(df2)

### Create a dataframe using list of tuples

     l=[("abc",10,10),("def",20,30),("fgh",30,40)]
     df3=pd.DataFrame(l)
     print(df3)

## Total Code to create

    import pandas as pd
    #Data get from an excel
    d=pd.read_excel("C:\\Users\\surya\\OneDrive\\Desktop\\pandas\\for_pandas.xlsx")
    df1=pd.DataFrame(d)

    d=pd.read_csv("C:\\Users\\surya\\OneDrive\\Desktop\\pandas\\for_pandas.csv")
    df2=pd.DataFrame(d)

    #data get from a dictionary
    di={"Name":["abc","def","ghi"],"Roll_no":[1,2,3],"price":[20,30,40]}
    df3=pd.DataFrame(di)

    l=[("abc",10,10),("def",20,30),("fgh",30,40)]
    df4=pd.DataFrame(l)

    print(df1)
    print(df2)
    print(df3)
    print(df4)

# 5. Indexing Slicing

- ### data_frme.head(no.of rows)

  To dislay top to bottom no.of recordswith out number it gives the top 5

- ### data_frme.tail(no.of rows)

  To dislay top to bottom no.of records
  with out number it gives the Bottom 5

- ### data_frme.describe()

  defaulty it gives the different type of operations (sum, mean, max...)

- ### data_frme.shape()

  it gives the nof rows and column in the taken data

- ### data_frme[start:stop:step]

  it gives the data from start to stop with difference in step

- ### data_frme['column_name']

  it gives total column by column name

- ### data_frame [[col1,col2]]
  it gives the columns by names
- ### data_frme[[col1,col2]][start:stop:step]

  it gives the data after fallow both columns and slicing conditions satisfied

- ### data_frame.iterrows()

it Gives the individual records

# 6. Understanding LOC & ILOC

- In LOC stop index included and access the columns with names
- In ILOC stop index excluded and access the columns with numbers

## LOC

- ### dat_frame.loc[ row_no ]

  it gives the direct row as record

- ### dat_frame.loc[ row_no,[col_name] ]

  it gives the row details based on column name

- ### dat_frame.loc[ start : stop]

  It gives the strt to stop (it gives stop include)

- ### dat_frame.loc[ start:stop,"col_name" ]

  It gives the strt to stop (it gives stop include) based column name

- ### dat_frame.loc[start:stop, [ "col1, col2...." ]]

  It gives the strt to stop (it gives stop include) based multiple column name  
   we have to pass as a list in the case we want multi columns names and

- ### dat_frame.loc[start:stop,"col_1":col_n"]
  we can give idex for the column names also

## ILOC

- ### dataframe.iloc[ row-no, col-no ]

  we get cell values by using this

- ### dataframe.iloc[ row-strt : row-stop, col-start, col-stop ]

  we get rows and columns

- ### dataframe.iloc[ strat:stop, "column-no" ]

  we get range of rows and column by numbers

- ### dataframe.iloc[ row1,row2.... ]

  we get the no.of random numbers

- ### dataframe.iloc[ :, [col1,col2,... ] ]

  we get all rows and specific columns

- ### dataframe.iloc[ strt:stop,[ col1,col2,.. ]]

  we getrange of rows and specific columns

# 7. Sorting the DATAFRAME

## We have some imbuilt methods to sort data

- ### data_frame.sort_values("col_name")
- ### data_frame.sort_values("col_name",ascending=False)
- ### data_frame.sort_values([ "col1","col2" ])
- ### data_frame.sort_values( ["col1", "col2"],ascending=[ 0,1 ])

# Manipulating DATAFRAME

## 1. Adding Column

- data_frame['new_col_name']=defaulu_value
  to add column with default value
- data_frame['new_col_name']=Expression/condition
  to add column with

## 2. Removing Column

- Data_frame.drop(column="coumn_name")

  to delete tempararly

- Data_frame.drop(column="coumn_name",inplace=True)

  To delete perminently

## know Duplicates

- Data_frame.duplicated() -boolean result (True/Flase)

## 3.Removing Duplicates

- Data_frame.drop.duplicates()

  To delete tempararly

- Data_frame.drop_duplicates(inplace =True)

  To delete perminently

# 8. Handling Missing Data

## Removing Missing Data

- ### Data_frame.dropna()

  To delete complete record tempararly

- ### Data_frame.dropna(inplace=True)

  To delete complete record perminently

## Fill With Default Values

- ### Data_frame.fillna(default_value)

fill with a default value

Below method is also used for specific column fill

    df["social"].fillna(80)

# 9. Data Filtering & Conditional Changes

- Data_frame.loc[simple_codition]

        syntax
        df.loc[df["maths"]>60]

- Data_frame.loc[compound_condition]

        syntax
        df.loc[( df["maths"]>60) & (df["maths"]<85) ]

- Data_frame.loc[simple_codition.str.contains(str)]

         syntax
         df.loc[df["name"].str.contains("n")]

- Data_frame.loc[simple_codition.str.strtswith(str)]

         syntax
         df.loc[df["name"].str.startswith("s")]

- Data_frame.loc[simple_codition.str.endswith(str)]
  syntax
  df.loc[df["name"].str.endsswith("s")]

## Conditional change

Based on condition change the data of anpther column

    syntax
    df.loc[(d["percentage"]>60) & (df["percentage"]<70),"Grade"]="First Class"

# 10. Export DATAFRAME

- ### Data_frame.to_excel(Path)

  with index values

- Data_frame.to_excel(Path,index=False)

  with out indux values

- ### Data_frame.to_csv(Path)

  with index values

- ### Data_frame.to_csv(Path,index=False)

  with out indux values
