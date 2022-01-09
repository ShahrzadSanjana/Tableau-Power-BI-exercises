**Overview**

I wanted to demonstrate and practice my dashboarding skills and ability to present visualizations on metrics that I think will matter most to a business in a clean, thoughtful, and easily digestible manner.

But rather than stopping at only building a dashboard, I wanted to put myself in the shoes of an Analyst at Netflix and provide a few recommendations/actions, based on my review of the Tableau dashboard, to a fictitious senior executive to consider in spurring business performance – thereby allowing me to also demonstrate business acumen and nous by leveraging my economics/business background.

To this end, I downloaded this dataset of Netflix Titles in .CSV format from Kaggle, and cleaned it using the Data Cleaning techniques described below, and then created my visualizations and dashboard with KPI’s. 



**Data cleaning steps:**

The .CSV file from Kaggle needed to be cleaned before I could import it into my visualization program, so these are the data cleaning steps that I took to address its quality. 

1)	My data set contains Director’s names and Titles with accented letters and words in foreign languages as well. I noticed that Excel had trouble displaying these characters in their true forms, and instead displayed odd characters in their place. For example, the documentary, titled ‘Zoé: Panoramas’ was displayed as ‘ZoÃ©: Panoramas’ in the file. 

    Since I have never faced such encoding issues with accented letters and foreign languages in my data, I looked up another way to clean the file without having to search for the right Title or Director's names on Google and copying that into the .CSV file. The solution was to first save the file in .txt type (using ‘Save as’). Then I opened a new Excel workbook and went to the Data tab to select ‘Get External Data from Text file’. For the ‘File Origin’ drop-down menu, I learned I am supposed to change the default to ‘65001: Unicode (UTF-8)’, in order to debug the encoding issues with my data set. I learnt this trick through excelforum.com. 
    
    This ‘cleaning technique’ eliminated any time I had to take to replace the broken characters with the right letters or foreign language for multiple affected rows and columns.

2)	Next, I used the ‘Filter’ function in Excel, and applied it to each column to get a get an 'at-a-glance' view of the different values through the menu drop-down in the column headers. For example, I found that there were show duration times in the Rating column, and copied and pasted those values to the Duration column. The 'Filter' tool saved me time in having to go through each row for thousands of rows to find incorrectly entered data.

3)	Thirdly, I used the ‘Text to Columns’ feature in the Data tab to reformat the dates in my data set into a single, uniform format. In the downloaded version of the file, the Date_added column had multiple date formats, such  as ‘21-02-2012’ and ‘September 16, 2018’. The ‘Text to Columns’ feature allowed me to change the date format to the MDY convention we use in N. America. I then went to the ‘Number’ section on the Home tab to display dates in the long format: ‘month dd, year’, and all this ensured there was uniformity in appearance. 

4)	I had a few duplicate entries in my data, so I used the Conditional Formatting option to highlight duplicate Titles with red-colour text. I then used the ‘Filter’ feature to ‘Filter by text colour’ and return only these titles (instead of having to sift through thousands of rows to find the highlighted Titles in red-coloured text), and deleted the duplicate entries. 

![screenshot](https://user-images.githubusercontent.com/78444311/148698223-5f17f735-820b-4ebe-95bf-cf289e6db28d.jpg)


    In the above screenshot, all the duplicate Titles in the database are in red-colour text. This allowed me to quickly delete the rows that were really duplicates – for example, I deleted one of the “Love in a Puff” rows, but I kept both “Fullmetal Alchemist” titles as one was a movie and the other a TV show released by different Director’s and Cast (I confirmed this was the case on imdb.com). 
