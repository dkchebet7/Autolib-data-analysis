# Autolib-data-analysis
# DATA PREPARATION
     #Selecting data
 I selected or rather used the entire table of Autolib data as it was only one dataset and contained mostly useful information.
     #Clean data
To ascertain valid results, all the unwanted noises in our dataset has to be silenced. This was achieved in the following ways
Standardization: This involves removing all unnecessary spaces from our dataset column and replacing them with an underscore.
       Data.columns = Data.columns.str.strip().str.replace(' ','_')
       Data.head()
    #Validity; Here we dropped all the unnecessary columns from our data.
        Main_Data = Data.drop([Data.drop(['Cars','Address','Charging_Status','Displayed_comment','Geo_point','Scheduled_at','Slots','Station_type'], axis=1 ,inplace =True)])
   #Completeness: This was ensuring that all columns had no null values
         #Main_Data.isnull()
 
   #Construct data
From the cleaned data, we can create another csv data from it so as to prevent crushing due to the size of the dataset and to also prevent redundancy of work during analysis.
We therefore construct the new dataset,then load it into our notebook.
To achieve this, the following syntax is used.
         #Main_Data.to_csv(‘Data2.csv’)

# DATA ANALYSIS
Here, i used the cleaned dataset to answer the individual reserch questions 
