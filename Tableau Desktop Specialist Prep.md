# Tableau Desktop Specialist Prep

## Connecting to & Preparing Data 

### Create and save data connections 

- Create a live connection to a data source 

  - A live connection is where Tableau connect to the data source directly.
  - For Tableua Desktop, a live connection is __default__.

  

- Explain the differences between using live connections versus extracts 

  - Live connections offer the convenience of real-time updates, with any changes in the data source reflected in Tableau. 
  - Live connections also rely on the database for all queries. 
  - And unlike extracts, databases are not always optimized for fast performance. 
  - With live connections, your data queries are only as fast as the database itself.

  

- Create an extract 

  - In Tableu Desktop, you can create an extract __by right-clicking__ on the dataset and selecting create extract.
  - You can also create extracts by selecting the extract radio button on the Data Source tab.
  - Managine the size of the extract
    - You get a lot of options than can make the extract smaller
      - only include a sample of the data
      - aggregate to visible dimensions
      - use extract fileters
  - Incremental Load
    - Incremental loads mean that only the new data is refreshed.
    - Reduce the time it takes to create the extract



- Save metadata properties in a . TDS 
  - Metadata is data about the data.
    - Data structure
  - TDS : Tableau Data Soucre
  - Save a data source 
    1. In Tableau Desktop, open the workbook that has the connection to the data you want to save as a file.
    2. At the top of the **Data** pane, right-click (Control-click on Mac) the name of the data source, and then select **Add to Saved Data Sources**.
    3. Enter a file name, select the file type (.tds or .tdsx), and then click **Save**.
  - Tableau File Types
    - .twb : Tableau workbook
    - .twbx : Tableau packaged workbook
    - .hyper and .tde : Tableau extract
    - .tds : Tableau data source
    - .tdsx : Tableau packaged data source



### Modify data connections 

- Add a join 

- Add a blend 

- Add a union 

### Manage data properties 

- Rename a data field 

- Assign an alias to a data value 

- Assign a geographic role to a data field 

- Change data type for a data field (number, date, string, Boolean, etc.) 

- Change default properties for a data field (number format, aggregation, color, date format, etc.) 

## Exploring & Analyzing Data 

###  Create basic charts 

- Create a bar chart
- Create a line chart 
- Create a scatterplot 
- Create a map using geographic data 
- Create a combined axis chart 
- Create a dual axis chart  
- Create a stacked bar 
- Create a chart to show specific values (crosstab, highlight table) 

### Organize data and apply filters 

- Create a visual group 
- Create a group using labels 
- Create a set 
- Organize dimensions into a hierarchy 
- Add a filter to the view 
- Add a context filter 
- Add a date filter 

### Apply analytics to a worksheet 

- Add a manual or a computed sort  
- Add a reference line or trend line 
- Use a table calculation  
- Use bins and histograms 
- Create a calculated field (e.g. string, date, simple arithmetic) 
- Add a parameter 

## Sharing Insights 

### Format view for presentation 

- Use color 
- Use bolding  
- Use shapes  
- Use viz animations  
- Change size of marks  
- Select fonts 

### Create and modify a dashboard 

- Create a dashboard layout  
- Add interactive or explanatory elements 
- Add dashboard actions  
- Modify existing dashboard layout for mobile devices 
- Create a story using dashboards or views 
- Share a twbx as a PDF - Share a twbx as an image 

## Understanding Tableau Concepts 

### Dimensions and measures 

- Explain what kind of information dimensions usually contain 
- Explain what kind of information measures usually contain 

### Discrete and continuous fields 

- Explain how discrete fields are displayed in Tableau 
- Explain how continuous fields are displayed in Tableau 
- Explain the difference between discrete date parts and continuous date values in Tableau 

### Aggregation 

- Explain why Tableau aggregates measures 
- Describe how an aggregated measure changes when dimensions are added to the view 



## Timeliness 

Completing a task effectively and efficiently has become a standard that organizations expect from employees. This exam is timed because we view time as a critical competency needed to be successful. 