# Tableau Desktop Specialist Prep

## Connecting to & Preparing Data 

### Create and save data connections 

- Create a live connection to a data source 

  - A live connection is where Tableau connect to the data source directly.
  - For Tableua Desktop, a live connection is __default__.

    __QUIZ__

    How can the users refresh an extract immediately in Tableau desktop? (Multiple Possible Answers)
    a) Select a Data Source on Data Menu -> Extract 

    b) Select a Data Source on Data Menu -> Extract -> Refresh 

    c) Sign in to Tableau Server -> Click Tasks at the top of the page -> Under Extract Refreshes select the workbook or data source -> On the Actions menu click Run now. 

    ~~d) Select a Data Source on Data Menu -> Extension -> Refresh~~

    

    __Explanation__

    In Tableau in several way user can immediately refresh an extract either by going to extract and then select refresh or by manually selecting data source or workbook under extract refreshes and click on run now under Actions menu.



- Explain the differences between using __live connections__ versus __extracts__ 

  - Live connections offer the convenience of real-time updates, with any changes in the data source reflected in Tableau. 
  - Live connections also rely on the database for all queries. 
  - And unlike extracts, databases are not always optimized for fast performance. 
  - With live connections, your data queries are only as fast as the database itself.

    __QUIZ__

    What Is The Difference Between Live And Extract Connections. (Multiple Possible Answers)
    a) Live allows real-time data while extracts are kind of batch which needs to be refreshed from time to time to get the updated data.
    b) Live Connection takes more time to load data than Extract Connection.
    ~~c) Live Connection does not slow down operational queries which results in fetching data quickly.
    d) Both the connection takes same time to work with and they do not have any functional difference.~~ 

    __Explanation__ 

    In the case of live connection whatever changes will be done at the Datasource end that will be directly available to the tableau desktop.
    While in case of extracting any changes made in the data source won't reflect in the report immediately. It will be reflected when the extract will be refreshed. Also, we need to apply an aggregation that takes too long when using a live connection which results in delaying working with the dataset. Live connection might slow down operational queries too much, so having Tableau only query at scheduled extract refresh times is preferable.





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
    
    __QUIZ__
    
    Why the direct connection to the extract is not recommended – (Multiple Possible Answers)
    a) The table names will be different 
    
    b) The extract cannot be refreshed 
    
    c) The data model and relationships will be lost. 
    
    ~~d) The extract cannot be removed once it is connected directly.~~
    
    __Explanation__
    
    We can remove an extract at any time by selecting the extract data source on the Data menu and then selecting Extract > Remove.
    Tables stored in the extract use special naming to guarantee name uniqueness, and it may not be human-readable. We cannot refresh the extract. When connecting directly to an extract, Tableau treats that file as the true source, as opposed to a clone of underlying data. So, it's not possible to relate it back to your source data. The data model and relationships will be lost. The data model and relationships between the tables is stored in the .tds file and not in the .hyper file, so this information is lost when connecting directly to the .hyper file.



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
  - Inner 
  - Left
  - Right
  - Full Outer
- Add a blend 
  - Combine data with different levels of granularity without duplication.
  - With a blend, a primary data source is linked to a secondary data source. The data in the secondary data source will not duplicate even if linking criteria is satisfied multiple times.
  - Data blending keeps the data sources __separate__ and simply displays their information together.
  - Each data source is __queried independently__ and the results are __aggregated to the appropriate level__ then visualized together.
- Add a union 
  
  - Relationships combine data at different levels of detail without introducing duplication.
  
  - Relationships __don't duplicate data__ and they __don't query data__ unless columns from that table are used in the viz.
  
  - Joins produce a new row each time the join criteria is met, which can duplicate data.
  
    
    
    __QUIZ__
    
    How many data sources can we blend in Tableau? 
    
    a) Two  
    
    __Explanation__
    
    The two sources involved in data blending are referred as primary and secondary data sources. A left join is created between the primary data source and the secondary data source with all the data rows from primary and matching data rows from secondary data source.
    
    __QUIZ__
    
    In a Relationship we need to define the following Join type  
    
    d) It is not required to define a join type in a relationship
    
    __Explanation__
    
    It is not required to define a join type in a relationship Explanation: In a relationship in Tableau it does not require to select any join type.
    
    
    
    __QUIZ__
    
    Which option leads to adjusting the granularity of data in Tableau? 
    
    __a) Aggregate__
    
    b) Group by 
    
    c) Grouped Fields 
    
    d) Extract
    __Explanation__
    
    To adjust the granularity of the data, we use the Aggregate option to create a step to aggregate or group data.
    
    __QUIZ__
    
    Advantages to using relationships to combine tables: (Multiple Possible Answers) 
    
    ~~a) Makes it easier to change the key fields used to combine the tables~~
    
    b) Make it easier to analyse data across multiple tables at different levels of granularity 
    
    ~~c) Makes it easier to combine rows from one table with rows from another~~
    
    d) Tables are only queried when fields from the tables are added to the viz.
    
    __Explanation__
    
    Changing the key fields is a similar process with relationships and joins. Relationships do not combine rows from one table with rows from another. They do have the other benefits listed: duplication is avoided when tables are combined with different levels of granularity and tables are only queries when required in the worksheet.













### Manage data properties 

- Rename a data field 

  __QUIZ__

  Select the correct pathway to edit the data source  

  a) Data Menu -> Select a Data source -> Edit Data Source 

  ~~b) Data Menu -> Select a Data source -> Extract Data~~ 

  ~~c) Data Menu -> Select a Data source -> View Data~~ 

  ~~d) Data Menu -> Select a Data source -> Edit Data Source Filters~~

  __Explanation__ 

  On the Data menu, select a data source, and then select Edit Data Source. And, then on the data source page, make the changes to the data source.

- Assign an alias to a data value 

  __QUIZ__

  Aliases cannot be created for the following – (Multiple Possible Answers) 

  ~~a) Discrete dimension~~ 

  b) Continuous dimension
  c) Measures 

  d) Dates
  __Explanation__

  In Tableau aliases can be created for the members of __discrete dimensions only__. They cannot be created for continuous dimensions, dates, or measures.
  

- Assign a geographic role to a data field 

  __QUIZ__

  While assigning geographic role to a field, Tableau adds two fields to the Measures area of the Data pane: 

  a) Latitude and Longitude.
  __Explanation__

  In Tableau while assigning geographic role to a field, Tableau adds two fields to the Measures area of the Data pane: __Latitude (generated) and Longitude (generated)__. While Meridian an imaginary line from the North Pole to the South Pole.

- Change data type for a data field (number, date, string, Boolean, etc.) 

  __QUIZ__

  Choose the correct path to change the data type for a field in the view 

  a) Right click the field in the Data pane -> Change Data Type -> Data Types -> Choose the appropriate data type 

  __b) Right click the field in the Data pane -> Change Data Type -> Choose the appropriate data type__

  c) Right click the field in the Data pane -> Data Types -> Choose the appropriate data type 

  d) Right click the field in the Data pane -> Choose the appropriate data type
  __Explanation__

  To change a field's data type in a view, right-click (control-click on a Mac) the field in the Data pane, choose Change Data Type, and then select the appropriate data type from the drop-down list.

  

- Default : Sum

- Change default properties for a data field (number format, aggregation, color, date format, etc.) 

  __QUIZ__

  Choose the correct path to add a default comment for a field

  __a) Right click a field in the Data pane-> Default Properties-> Comment __

  b) Right click a field in the Data pane-> Aggregation -> Default Properties-> Comment 

  c) Right click a field in the Data pane -> Comment 

  d) Right click a field in the Data pane-> Describe-> Comment

  __Explanation__

  Right-click (control-click on a Mac) a field in the Data pane and select Default Properties > Comment. Write a comment in the subsequent dialog box. Comments support rich text formatting that will be represented in the tooltip.

 [For QUIZ ONLY](https://learningtableau.com/quiz/specialist-quiz-connecting-to-preparing-data/)




## Exploring & Analyzing Data 

###  Create basic charts 

- Create a bar chart
  - Add values and dimension
  - Add a second dimension to view creates a stacked bar
  - Side by side bar 
  - Order of columns changes charts. 
- Create a line chart 
  - Discrete fields create header.
  - Continuous field create axes.
- Create a scatterplot 
  - Scatter plots allow you to visualize the relationship between two or more measures
- Create a map using geographic data 
  - Edit loaction for data
  - When the same city exists in multiple states, you need to include the state in the view.
- Create a combined axis chart 
- Create a dual axis chart  
  - A dual line chart shows two diffrent measures changing a date range.
- Create a stacked bar 
- Create a chart to show specific values (crosstab, highlight table) 
  - Cross tab is tax table.
  - A hightlight table is a crosstab with a color gradient for the measure.

### Organize data and apply filters 

- Create a visual group 
- Create a group using labels 
- Create a set 
  - Set comes before filter.
  - When we set a context filter, the filter happens before the set.
- Organize dimensions into a hierarchy 
  - Simply drag for a hierarchy
- Add a filter to the view 
- Add a context filter 
- Add a date filter 

### Apply analytics to a worksheet 

- Add a manual or a computed sort  
- Add a reference line or trend line 
  - For trend line, R-squared tells you how well the line fits the data. 
  - A value  of 1 would indicate a perfect fit.
  - The smaller the p-value, the more confident we are that the relationship we see between the x and y  values is not just due to chance
- Use a table calculation  
- Use bins and histograms 
- Create a calculated field (e.g. string, date, simple arithmetic) 
  - split function allows us to split a string into parts
- Add a parameter 
  - Parameters values can be used in calculations. 
- [For more](https://learningtableau.com/quiz/specialist-quiz-exploring-analyzing-data/)



## Sharing Insights 

### Format view for presentation 

- Use color 
- Use bolding  
- Use shapes  
- Use viz animations  
- Change size of marks  
  - Most important measure should be on the x and y axis, less import can be visualized with color or size
- Select fonts 
- Viz Animations
  - Provide gradual transitions when change is made to visulization
  - Transition can be sequential where one element at a time changes or simultaneous where all elemnts change together
  - Animation options can be set at the workbook

### Create and modify a dashboard 

- Create a dashboard layout  
- Add interactive or explanatory elements 
- Add dashboard actions  
- Modify existing dashboard layout for mobile devices 
- Create a story using dashboards or views 
  - Story points direct the viewer to the specific insights you want them to focus on.
- Share a twbx as a PDF - Share a twbx as an image 

[For More Quiz](https://learningtableau.com/quiz/specialist-quiz-sharing-insights/ )







## Understanding Tableau Concepts 

### Dimensions and measures 

- Explain what kind of information dimensions usually contain 
  - Dimensions at granularity to the view.
- Explain what kind of information measures usually contain 
  - Measures are aggregated when added to the view.

### Discrete and continuous fields 

- Explain how discrete fields are displayed in Tableau 

  - Pill color is blue
  - Header
  - Discrete dimensions are more common than continuos dimensions.

- Explain how continuous fields are displayed in Tableau 

  - Pill color is green
  - Axis
  - Continuous measures are more common than discreted measures.

- Explain the difference between discrete date parts and continuous date values in Tableau 

  

### Aggregation 

- Explain why Tableau aggregates measures 
- Describe how an aggregated measure changes when dimensions are added to the view 
  - Dimensions increas the granularity (also called level of detail) of the view.



[For More Quiz](https://learningtableau.com/quiz/specialist-quiz-understanding-tableau-concepts/)











## Timeliness 

Completing a task effectively and efficiently has become a standard that organizations expect from employees. This exam is timed because we view time as a critical competency needed to be successful. 