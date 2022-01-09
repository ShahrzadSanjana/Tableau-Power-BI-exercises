**Overview**

I wanted to demonstrate and practice my dashboarding skills and ability to present visualizations on metrics that I think will matter most to a business in a clean, thoughtful, and easily digestible manner.

But rather than stopping at only building a dashboard, I wanted to put myself in the shoes of an Analyst at Netflix and provide a few recommendations/actions, based on my review of the Tableau dashboard, to a fictitious senior executive to consider in spurring business performance – thereby allowing me to also demonstrate business acumen and nous by leveraging my economics/business background.

To this end, I downloaded this dataset of Netflix Titles in .CSV format from Kaggle, and cleaned it using the Data Cleaning techniques described below, and then created my visualizations and dashboard with KPI’s. 


**Data cleaning steps:**

The .CSV file from Kaggle needed to be cleaned before I could import it into my visualization program, so these are the data cleaning steps that I took to address its quality. 

1)	My data set contains Director’s names and Titles with accented letters and words in foreign languages as well. I noticed that Excel had trouble displaying these characters in their true forms, and instead displayed odd characters in their place. For example, the Mexican documentary, titled ‘Zoé: Panoramas’ was displayed as ‘ZoÃ©: Panoramas’ in the file. 

    Since I have never faced such encoding issues to do with accented letters and foreign languages in my data, I looked up another way to clean my data on the internet. The   solution was to first save the file in .txt type (using ‘Save as’). Then I opened a new Excel workbook and went to the Data tab to select ‘Get External Data from Text file’. For ‘File Origin’ drop-down, I learned I am supposed to change the default to ‘65001: Unicode (UTF-8)’, in order to debug the encoding issues with my data set. I learnt this trick through excelforum.com. 
