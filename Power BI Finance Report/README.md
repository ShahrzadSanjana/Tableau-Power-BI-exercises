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


Those were all the data transformations. We are ready to load this cleaned data in to a data model now, so click “Close & Apply” in the Home tab.

<br/>

**Data Modelling**

Using DAX for new columns and measures


We will use a measure to calculate the SUM of the Units Sold column:


Total Units Sold = SUM(financials[Units Sold])


And I “commit” the measure to the data model. This measure will be useful in …


Then I create a New Table in the Data View to be populated by a calculated column. I will write a DAX formula/expression to return a calculated column of all dates between January 1, 2013 and December 31, 2014 using the CALENDAR function. The new table will be called Calendar:

Calendar = CALENDAR(“01/01/2013”, “31/12/2014”)	

In the Model View, we will set up a relationship between this new table and the original Financials table imported from the Excel file that will allow them to interact with each other. Drag the Date field/column from the Financials table on to the Date column in the Calendar table.

We are now ready to build our visuals.

<br/>

**Data Visualization** 

There will be 5 visuals in all.

<br/>

*Visual #1: Title*

Create a Text Box for the report title and add a transparent background to it.

<br/>

*Visual #2: Profit by Date*

See which Month & Year had the highest profit using a Line Chart.

We will use the Profit field from the Financials table and the Date column from Calendar (without the Quarter and Day.

In the Visualizations on the right in the Field section, select the drop-down list next to “Dates”, and select “Date Hierarchy”.

<br/>

*Visual #3: Profit by Country/Region*

Use Map visualization to see which Country/Region earned the greatest share of profit. Drag Country field to a blank area of the canvas to create a map visualization, and drag the profit field from the Financials table to the map.

Power BI creates a map visual complete with bubbles representing the profit of each Country/Region.

Region-wise, North America (Canada, U.S., and Mexico) produces more profit than Europe. Country-wise, France produces more profit during the time period - $3.3 million, followed by Canada with $3.2 million. 

<br/>

*Visual #4: Sales by Product & Segment*

We’ll create a Bar Chart to determine which Segment and Products generated more sales. From the chart, it is clear the company should continue investing in its 'Paseo' product as it generates the higest sales acros all Segments. For this product, the Government segment returns the most sales.

<br/>

*Visual #5: Year Slicer*

Slicers are valuable for filtering and adjusting the visuals on your page to display specific information. There are two ways we can create slicers for performance by Month & Year. The first is with the Date field from the original Financials table. You can go to Slicer settings in the visualizations pane and click the drop-down to choose a different type of Slicer.

The second way to create a Slicer is through using the DAX table. Select the Date field from the Calendar table and drag to the canvas. In the Visualizations pane, select the drop-down button next to “Date”, remove Quarter and Day from the Date Hierarchy so you’re only left with Year and Month in the Slicer. 

<br/>

**Formatting the report:**

We'll change the colour scheme of the reports to Executive, and edit the titles for each visualization, change their font sizes and toggle on background shadows. Then add separate background shapes for the Title visual and for the Line chart and Map visuals. 
