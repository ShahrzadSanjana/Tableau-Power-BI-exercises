**Overview**

Scenario : 
A manager wants to see a report on the latest company sales figures. They've requested an executive summary of:

1) Which month and year had the most profit?
2) Where is the company seeing the most success (by country/region)?
3) Which product and segment should the company continue to invest in?

<br/>


**Objectives:** 
<br/>
1) Download sample data <br/>
2) Prepare the data with a few transformations <br/>
3) Build a report with a title, three visuals, and a slicer <br/>
4) Publish the report to the Power BI service to with colleagues <br/>
<br/>

**Getting the Data** 
<br/>

There were 2 ways to get the sample data for this project:

1) Download the sample workbook directly from https://go.microsoft.com/fwlink/?LinkID=521962 and connect to it using the Excel workbook connector in Power BI, or
2) Open up Power BI Desktop and choose "Try a sample dataset" from the blank canvas, and on the right of the dialog box, click "Load sample data"

![Image 1 resized](https://user-images.githubusercontent.com/78444311/212312415-4778fd68-f366-4fe6-8a3f-1e1f4d216c64.png)


<br/>

**Preparing your data**
<br/>

We will first transform the data in the financials table of the file before loading into the data model. 
<br/>

Transformations to do:

1) Change the data type of the Units Sold column from decimal to a whole number as it is impossible to have fractions of a product sold.

2) Format the Segments column to display text values in uppercase. Right click the column header > Transform > UPPERCASE

3) Rename the Month Name column to Month

4) Filter out the data for a discontinued product in the Product column. Select the drop-down button in the column header and filtered out the rows containing the “Montana” product from the data model.


Those were all the data transformations. We are ready to load this cleaned data in to a data model now, so I clicked “Close & Apply” in the Home tab.

<br/>

**Data Modelling**
