HEART ATTACK VISUALIZATION

Tools used : Power BI(DAX , POWER QUERY) , MICROSOFT EXCEL(SLICER , PIVOT TABLES) , PYTHON(PANDAS)

Python :  -Imported the data with pandas library , used the describe function to look at the details of the data , look at the mean of the heart rate , the oldest individual in the dataset who was 103 years old.
          -Used the isnull().sum() function to check for missing values and used the fillna() function to replace them.

          
EXCEL     - Created 5 pivot tables to check for the likelihood of heart attack.Focued more on Troponin ( highly specific protein biomarker for heart muscle injury) and CK-MBA cardiac enzyme released during heart muscle damage)
          -Looked at the averages of CK-MB by gender and using a slicer specific on being either positive or negative , I found that for individuals who tested positive for heart attack are female dominated(23.75) with a higher CK-MB averagecompared to males(23.05)
           and those who tested negative were male dominated with a higher average (2.65) compared to female's (2.4).So this indicates that the individuals who are likely to be positve produce this enzyme rapidly.
           -You can look at the visualizations by opening the excel file(xlsx).
           
      
Power BI - Transformed the data using Power Query Editor , I had already used the CK-MB  and the Troponin columns so I decided to delete them and get other visualizations , I the conbverted the type from text to whole numbers.
         - I then used DAX to create a new meaure called Total blood pressure where I added Systolic Blood Pressure (the pressure in arteries when the heart contracts) and Diastolic Blood Pressure (the pressure in arteries between heartbeats) , where I added the sum
           of tese as it was a measure not a calculated column
           -You can view the visualizations by opening the Power bi report in the respository


           
