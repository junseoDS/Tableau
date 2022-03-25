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
  
    __QUIZ__
  
    What types of trend lines are available in Tableau? 
  
    __a) Drag the measure to the columns shelf and the dimension to the row shelf__ 
  
    b) Drag the measure to the rows shelf and the dimension to the column shelf 
  
    c) Drag the measure to both the row shelf and the columns shelf 
  
    d) Drag the dimension to both the rows shelf and the column shelf
  
    __Explanation__
  
    In Tableau, bar chart represents data in rectangular bars with the length of the bar proportional to the value of the variable. Tableau automatically produces a Vertical bar chart when you drag a __dimension to the Column shelf and measure to the Row shelf__. Hence, to flip a vertical bar chart to horizontal bar chart it is needed to draw Measure to Columns and Dimension to Rows.
  
- Create a line chart 
  - Discrete fields create header.
  - Continuous field create axes.
  
- Create a scatterplot 

  - Scatter plots allow you to visualize the relationship between two or more measures

    __QUIZ__

    What types of trend lines are available in Tableau? [Select All that Apply] 

    ~~a) logistic~~

    b) Linear 

    c) Logarithmic 

    ~~d) Multinomial~~ 

    e) Polynomial

    __Explanation__

    While creating Scatter Plot in Tableau, to add a trend line we need to go to the Analytics Pane and then select the trend line and drag it to view the available trend line models and drop it. The available trend line models that are used in Tableau are – __Linear, Logarithmic, Exponential and Polynomial__. However multinomial is not a type of trend line.

- Create a map using geographic data 
  - Edit loaction for data

  - When the same city exists in multiple states, you need to include the state in the view.

    __QUIZ__

    What steps should be taken to create a geographical hierarchy? 

    a) In the Analytics pane right-click the geographic field -> Create Hierarchy 

    b) In the Analytics pane right-click the create Hierarchy -> Select Hierarchy -> Ok 

    __c) In the Data pane right-click the geographic field-> Hierarchy -> Create Hierarchy__ 

    d) In the Data pane right-click the geographic field-> Transform -> select Hierarchy -> Create Hierarchy

    __Explanation__ 

    We can create geographic hierarchies. To create a geographic hierarchy:
    In the Data pane, right-click the geographic field, Country, and then select Hierarchy > Create Hierarchy. In the Create Hierarchy dialog box that opens, give the hierarchy a name, such as Mapping Items, and then click OK.

- Create a combined axis chart 

  __QUIZ__
  What is the difference between a dual axis chart and a combined axis chart? 

  a) Dual axis and combined axis are different terms but have the same meaning. 

  __b) Dual axis chart creates two independent axes while a combined axis chart merges two or more measures into a single axis. __

  c) Combined axis chart creates two independent axes while a dual axis chart merges two or more measures into a single axis.
  d) Dual axis chart becomes a combined axis chart once two or more measures are combined into a single axis.

  __Explanation__

  A combined axis merges two or more measures into a single axis so we can plot as many measures as we like in the same chart. The biggest advantage of this is that we have the option of adding an additional dual axis to this chart later if we need another mark type to reflect another measure. 

  On the other hand, a dual axis chart creates two independent axes (which we can synchronise) that we can plot two separate measures on in the same chart.

- Create a dual axis chart  
  
  - A dual line chart shows two diffrent measures changing a date range.
  
    __QUIZ__
  
    What steps will create a dual axis chart? [Select All that Apply] 
  
    __a) Drag one dimension to Column and drag two measures to Row -> In the Rows right click any of the measure -> Select Dual axes -> Go to marks type of any of the measure and choose the chart type as Bar__ 
  
    b) Drag two dimensions to Column and drag one measures to Row -> Go to marks type of any of the measure and choose the chart type as Bar 
  
    __c) Drag one dimension to Column and drag one measures to Row -> drag another measure to the chart itself and as the rectangle shape appears drop it -> Go to marks type of any of the measure and choose the chart type as Bar__
  
    d) Drag one dimension to Column and drag one measure to Row -> Go to marks type of any of the measure and choose the chart type as Bar
  
    __Explanation__
  
    There are several ways to create a dual axis chart in Tableau. 
  
    One of them are – Drag one dimension to Column and drag two measures to Row -> In the Rows right click any of the measure -> Select Dual axes -> Go to marks type of any of the measure and choose the chart type as Bar 
  
    Another way to create a dual axis chart is – Drag one dimension to Column and drag one measures to Row -> drag another measure to the chart itself and as the rectangle shape appears drop it -> Go to marks type of any of the measure and choose the chart type as Bar
  
- Create a stacked bar 

  __QUIZ__

  How to create a stacked bar chart while using a separate bar for each measure? – [Select All that Apply] __a) Drag a dimension to Color -> Drag Measure Names to Columns and drag Measure Values to Rows -> On the Columns shelf right-click Measure Names -> select Filter -> select the check boxes for the measures to display -> Ok__

  b) Drag a dimension to Color -> Drag Measure Names to Rows and also drag Measure Values to Rows -> On the Columns shelf right-click Measure Names -> select Filter -> select the check boxes for
  the measures to display -> Ok 

  c) Drag a dimension to Color -> Drag Measure Names to Columns and drag Measure Values to Rows -> On the Columns shelf right-click Measure Names -> Ok

  d) Drag a Measure Values to Color -> Drag Measure Names to Columns and drag Dimension to Rows -> On the Columns shelf right-click Measure Names -> select Filter -> select the check boxes for the measures to display -> Ok

  __Explanation__

  To create a stacked bar chart while using a separate bar for each measure we need to follow the steps - Drag a dimension to Color -> Drag Measure Names to Columns and drag Measure Values to Rows -> On the Columns shelf right-click Measure Names -> select Filter -> select the check boxes for the measures to display -> Ok

- Create a chart to show specific values (crosstab, highlight table) 
  - Cross tab is tax table.

  - A hightlight table is a crosstab with a color gradient for the measure.

    __QUIZ__

    Which of the following applies for Density map in Tableau – [Select All that Apply] 

    a) To create a density map, the data source should contain Latitude and Longitude coordinates or location names
    ~~b) Tableau cannot recognize location names and create a density map using the point locations assigned to Tableau geocoding locations~~

    c) Density maps are most effective when the location data is very precise, such as location coordinates in a limited space

    d) Density marks work best where the specific locations change continuously and smoothly across space, rather than values constrained to discrete locations like borough or neighbourhood.

    __Explanation__

    In Tableau to create a density map, the data source should contain Latitude and Longitude coordinates or location names .Tableau can recognize location names and create a density map using the point locations assigned to Tableau geocoding locations, but density maps are most effective when the location data is very precise, such as location coordinates in a limited space. Density marks work best where the specific locations change continuously and smoothly across space, rather than values constrained to discrete locations like borough or neighbourhood.

    __QUIZ__

    How to create Highlight Table or Heat Map in Tableau – 

    __a) Drag one or more dimensions on the Columns shelf and one or more dimensions on the Rows shelf -> place a measure of interest on the Colour shelf -> Select Square as the mark type __

    b) Drag one or more dimensions on the Columns shelf -> Select Square as the mark type -> place a measure of interest on the Colour shelf.

    c) Drag one or more dimensions on the Rows shelf-> Select Square as the mark type -> place a measure of interest on the Colour shelf. 

    d) Drag one dimension on the Columns shelf and one measure on the Rows shelf -> place a measure of interest on the Colour shelf.
    Correct answer: a. Explanation: In Tableau, we create a highlight table by placing one or more dimensions on the Columns shelf and one or more dimensions on the Rows shelf. We then select Square as the mark type and place a measure of interest on the Colour shelf.





### Organize data and apply filters 

- Create a visual group 

  __QUIZ__

  How to create a group from a field in the Data pane? – 

  __a) In the Data pane right-click a field -> select Create -> In the Create Group dialog box select the members that needs to be grouped -> Group -> Ok.__

  __b) In the Data pane right-click a field -> select Group. __

  c) In the Data pane right-click a field -> Group

  d) In the Analytics pane right-click a field -> select Group -> Ok.

  __Explanation__

  In Tableau to create a group from a field in the Data pane - in the Data pane, right-click a field and select Create > Group and then in the Create Group dialog box, select several members that you want to group, and then click Group.

- Create a group using labels 

- Create a set 
  - Set comes before filter.

  - When we set a context filter, the filter happens before the set.

    __QUIZ__

    Which of the following are the types of sets in Tableau? – [Select All that Apply] 

    ~~a) Singleton set~~

    b) Dynamic set 

    c) Fixed set

    ~~d) Equal set~~

    __Explanation__

    There are two types of sets: __dynamic sets and fixed sets__. The members of a dynamic set change when the underlying data changes. Dynamic sets can only be based on a single dimension. Singleton and Equal sets are used in mathematical calculations not in Tableau.

- Organize dimensions into a hierarchy 
  
  - Simply drag for a hierarchy
  
    __QUIZ__
  
    How to create a Hierarchy in Tableau? – 
  
    __a) In Data pane drag a field and drop on top of another field -> enter a name of the hierarchy -> ok__
    b) Right click on a field -> Create Hierarchy -> Choose the fields -> ok
    c) Right click on a field -> Create Hierarchy -> ok
    d) Right click on a field -> Choose the fields -> Create Hierarchy -> ok
  
    __Explanation__
  
    To create a hierarchy: In the Data pane, drag a field and drop it directly on top of another field and then, enter a name for the hierarchy and click OK.
  
- Add a filter to the view 

  __QUIZ__

  Filter dialog box offers the following tabs for filtering – [Select all that Apply] 

  ~~a) Report~~
  b) Wildcard
  c) Condition
  d) Top

  __Explanation__

  When we drag a discrete dimension to the Filters shelf, the Filter dialog box offers four tabs for filtering: General, Wildcard, Condition, and Top. Whereas report is a level of filter in Power BI.

  

- Add a context filter 

- Add a date filter 

  __QUIZ__

  How to create Relative Date Filters– 

  a) Drag a date field to the filter shelf -> Ok
  b) Drag a date field to the filter shelf -> Select a time unit -> Ok
  __c) Drag a date field to the filter shelf -> Select a time unit -> Define the date period -> Ok__
  d) Drag a date field to the filter shelf -> Define the date period -> Ok

  __Explanation__

  In Tableau to create Relative Date Filters we need to drag a date field to the filter shelf -> Select a time unit -> Define the date period -> Ok.

### Apply analytics to a worksheet 

- Add a manual or a computed sort  

  __QUIZ__

  Which of the following are applicable for nested sort in Tableau? – [Select all that Apply] 

  a) Nested sort considers each pane independently and sorts the rows per pane
  b) Nested sorts look correct within the context of the pane, but don’t convey the aggregated information about how the values compare overall
  ~~c) Sorting from an axis does not give a nested sort by default~~
  d) While creating a nested sort, the sort is inherited when we drill down through the dimensions

  __Explanation__

  In Tableau a nested sort considers each pane independently and sorts the rows per pane. Nested sorts look correct within the context of the pane, but don’t convey the aggregated information about how the values compare overall. Also, sorting from an axis gives a nested sort by default. When creating a nested sort, the sort is inherited when you drill down through the dimensions. For example, a nested sort on Hue will apply to Colour.

- Add a reference line or trend line 
  - For trend line, R-squared tells you how well the line fits the data. 
  - A value  of 1 would indicate a perfect fit.
  - The smaller the p-value, the more confident we are that the relationship we see between the x and y  values is not just due to chance
  
- Use a table calculation  

  __QUIZ__

  Which of the following quick table calculations are available in Tableau? – [Select all that Apply] 

  ~~a) Z-score~~
  b) Percent of total
  c) Rank
  d) Percentile

  __Explanation__

  The following quick table calculations are available in Tableau for you to use:
  __Running total, Difference, Percent difference, Percent of total, Rank, Percentile, Moving average, YTD total, Compound growth rate, Year of year growth, YTD growth__.
  Z-score option is not available in the quick table calculation of Tableau (however manually it can be performed).

- Use bins and histograms 

  __QUIZ__

  How do you create a Binned Dimension in Tableau? – 

  __a) In the Data pane right-click a measure -> select Create > Bins -> Create Bins dialog box accept the proposed New field name or specify a different name for the new field -> Mention the size of bins -> Ok.__

  b) In the Data pane right-click a measure -> Create Bins dialog box accept the proposed new field name or specify a different name for the new field -> Mention the size of bins -> Ok.

  c) In the Data pane right-click a measure -> select Create bins > Ok.

  d) Select Create > Bins -> Create Bins dialog box accept the proposed New field name or specify a different name for the new field -> Mention the size of bins -> Ok.

  __Explanation__

  To create a Binned Dimension in Tableau - In the Data pane right-click a measure -> select Create > Bins -> Create Bins dialog box accept the proposed New field name or specify a different name for the new field -> Mention the size of bins -> Ok.

- Create a calculated field (e.g. string, date, simple arithmetic) 

  - split function allows us to split a string into parts

    __QUIZ__

    The main types of calculations you can use to create calculated fields in Tableau: – 

    a) Basic calculations
    b) Level of Detail (LOD) expressions
    ~~c) Statistic Calculations~~
    d) Table calculations

    __Explanation__

    There are three main types of calculations you can use to create calculated fields in Tableau - Basic calculations, Level of Detail (LOD) expressions, Table calculations. There is no such option of Statistic Calculations in Tableau for calculated field.

- Add a parameter 

  - When the parameter value or list of values can’t refresh

    Below are a few scenarios in which a default parameter value or a refreshable list of parameter values (domain) will not update as expected:

    - The default field returns a value whose data is incompatible with the parameter’s data type.
    - The default field doesn’t return a single value (for the parameter’s current value).
    - The default field returns null.
    - The default field is in a data source that’s not yet connected.
    - The default field is no longer found in the workbook’s namespace (i.e. it’s been deleted).
    - The user cancels the query to the data source while Tableau is attempting to connect.

  - Parameters values can be used in calculations. 

    __QUIZ__

    Which of the following can prevent a refresh for a refreshable list of parameter values? [select all that apply] 

    a) The default field returns null.
    ~~b) The default field does not return a single value.~~
    c) The default field is in a data source that’s not yet connected.
    d) The user cancels the query to the data source while Tableau is attempting to connect.

    __Explanation__

    As explained here, https://help.tableau.com/current/pro/desktop/en-us/parameters_create.htm#when-the-parameter-value-or-list-of-values-can%E2%80%99t-refresh will cause the list to fail to refresh. A single value is required when setting the parameters default value, but not when dynamically setting a list of possible values for the parameter.
    
    __QUIZ__
    
    How to show subtotals in a visualization in Tableau – 
    
    __a) Click the Analytics pane -> In the Analytics pane under Summarize drag Totals into the Add Totals dialog -> drop it over Subtotals__
    
    b) Click the Analytics pane -> Click the Subtotals
    
    c) Click the Data pane -> In the Data pane under Summarize drag Totals into the Add Totals dialog -> drop it over Subtotals
    
    d) Click the Data pane -> Click the Subtotals
    
    __Explanation__
    
    To show subtotals in a visualization: Click the Analytics pane and in the Analytics pane, under Summarize, drag Totals into the Add Totals dialog, and drop it over Subtotals

- [For QUIZ ONLY](https://learningtableau.com/quiz/specialist-quiz-exploring-analyzing-data/)



## Sharing Insights 

### Format view for presentation 

- Use color 

  __QUIZ__

  How do you change the color of a chart from Marks card in Tableau? – [Select all that Apply] 

  __a) For an existing chart select the All in Marks card -> Select Color -> Edit Colors -> From the Select Color Palette select any of the desired option -> From the select Data item choose desired color for each of the measure -> Apply -> Ok__

  b) For an existing chart select the All in Marks card -> From the Select Color Palette select any of the desired option -> From the select Data item choose desired color for each of the measure -> Apply -> Ok 

  __c) For an existing chart select the All in Marks card -> Select Color -> Edit Colors -> From the Select Color Palette select any of the desired option -> Apply -> Ok__ 

  d) For an existing chart select the All in Marks card -> Select Color -> Choose the desired color -> Apply -> Ok

  __Explanation__

  There are two ways to change color from Marks card –
  For an existing chart select the All in Marks card -> Select Color -> Edit Colors -> From the Select Color Palette select any of the desired option -> From the select Data item choose desired color for each of the measure -> Apply -> Ok

  Or
  For an existing chart select the All in Marks card -> Select Color -> Edit Colors -> From the Select Color Palette select any of the desired option -> Apply -> Ok (when we are keeping the color palette as automatic)

  __QUIZ__

  Choose which of the following are true for using fonts in Tableau for visualization? – [Select all that Apply] 

  __a) If the workbook is created in Tableau Desktop then we can use any font installed on the computer in the workbook.__
  b) If the workbook is created using Web Authoring we can use any font installed on the computer in the workbook

  __c) If the workbook is published to Tableau Server any custom font must be installed on all server nodes. If the font is not installed on Tableau Server, the uninstall font will be replaced with a substitute font upon publishing. __

  d) If the workbook is published to Tableau Online we can use any font installed on the computer in the workbook.

  __Explanation__

  If the workbook is created using Web Authoring we can use only fonts installed on the Tableau Server or Tableau Online are functional when formatting your text. If the workbook is published to Tableau Online we can use only fonts supported by Tableau Online will appear.

  __QUIZ__

  How can we change the shape of the marks for a chart in Tableau? – 

  a) Choose any two measures and drag them to columns and rows -> select any measure and drag it to the color of Marks card -> select any measure and drag it to the shape of the Marks card
  b) Choose any one measures and drag it to columns and choose any dimension and drag it to rows -> select any dimension and drag it to the color of Marks card -> select any dimension/measure and drag it to the shape of the Marks card 

  c) Choose any two dimensions and drag them to columns and rows -> select any dimension and drag it to the color of Marks card -> select any dimension/measure and drag it to the shape of the Marks card 

  __d) Choose any two measures and drag them to columns and rows -> select any dimension and drag it to the color of Marks card -> select any dimension/measure and drag it to the shape of the Marks card__

  __Explanation__

  The correct way to change the shape of the marks for a chart in Tableau –
  Choose any two measures and drag them to columns and rows -> select any dimension and drag it to the color of Marks card -> select any dimension/measure and drag it to the shape of the Marks card

  

- Use bolding  

- Use shapes  

- Use viz animations  

- Change size of marks  
  
  - Most important measure should be on the x and y axis, less import can be visualized with color or size
  
  __QUIZ__
  
  How can we change the size of marks in Tableau? – 
  
  __a) After creating any chart go to Marks card -> Select the size -> Move the slider to the right or left to increase or decrease the size of the chart__
  
  b) After creating any chart go to Format -> Select the Marks card -> Choose the size of the chart
  
  c) After creating any chart go to Analysis -> Select the Marks card -> Choose the size of the chart 
  
  d) After creating any chart go to Story -> Select the Marks card -> Choose the size of the chart
  
  __Explanation__
  
  To change the size of marks in Tableau - After creating any chart go to Marks card -> Select the size -> Move the slider to the right or left to increase or decrease the size of the chart
  
- Select fonts 

- Viz Animations
  - Provide gradual transitions when change is made to visulization
  
  - Transition can be sequential where one element at a time changes or simultaneous where all elemnts change together
  
  - Animation options can be set at the workbook
  
    __QUIZ__
  
    How can we enable the option of Animation in Tableau? – 
  
    a) Go to Analysis -> Choose Animations -> Select On from Animations Tab
  
    __b) Go to Format -> Choose Animations -> Select On from Animations Tab__
  
    c) Go to Dashboard -> Choose Animations -> Select On from Animations Tab 
  
    d) Go to Worksheet -> Choose Animations -> Select On from Animations Tab
  
    __Explanation__: The correct way to enable the option of Animation in Tableau – Go to Format -> Choose Animations -> Select On from Animations Tab

### Create and modify a dashboard 

- Create a dashboard layout  

  __QUIZ__

  How can we create a dashboard in Tableau? [Select all that Apply] 

  __a) Go to dashboard and select New Dashboard -> Drag the desired worksheets to the dashboard to work for -> Adjust the dashboard length and width -> Ok__

  b) Go to Analysis and select New Dashboard -> Drag the desired worksheets to the dashboard to work for -> Adjust the dashboard length and width -> Ok

  c) Go to Worksheets and select New Dashboard -> Drag the desired worksheets to the dashboard to work for -> Adjust the dashboard length and width -> Ok 

  __d) Select the New Dashboard option -> Drag the desired worksheets to the dashboard to work for -> Adjust the dashboard length and width -> Ok__

  __Explanation__

  To create a dashboard in Tableau – there are two ways we can do it –
  Go to dashboard and select New Dashboard -> Drag the desired worksheets to the dashboard to work for -> Adjust the dashboard length and width -> Ok
  Or
  Select the New Dashboard option from the below tabs directly -> Drag the desired worksheets to the dashboard to work for -> Adjust the dashboard length and width -> Ok

  

- Add interactive or explanatory elements 

  __QUIZ__

  How do you create a viz in tooltip in Tableau?

  __a) Create a visualization in the source worksheet in Tableau -> Create a visualization in a target worksheet view to serve as the Viz in Tooltip and rename it to identify -> In the source worksheet, click Tooltip in the Marks card -> Select insert and select the target worksheet__

  b) Create a visualization in the source worksheet in Tableau -> Create a visualization in a target worksheet view to serve as the Viz in Tooltip and rename it to identify -> In the target worksheet, click Tooltip in the Marks card -> Select insert and select the target worksheet

  c) Create a visualization in the source worksheet in Tableau -> Create a visualization in a target worksheet view to serve as the Viz in Tooltip and rename it to identify -> In the source worksheet, click Tooltip in the Analytics tab -> Select insert and select the target worksheet

  d) Create a visualization in the source worksheet in Tableau -> Create a visualization in a target worksheet view to serve as the Viz in Tooltip and rename it to identify -> In the source worksheet, click Tooltip in the Worksheets tab -> Select insert and select the target worksheet

  __Explanation__

  To create a viz in tooltip in Tableau –
  Create a visualization in the source worksheet in Tableau and create a visualization in a target worksheet view to serve as the Viz in Tooltip and rename it to identify. In the source worksheet, click Tooltip in the Marks card and select insert and select the target worksheet.

  __QUIZ__

  Which of the following are true for URL actions in Tableau? [Select all that apply] 

  a) A URL action is a hyperlink that points to a web page, file, or other web-based resource outside of Tableau

  b) We can use URL actions to create an email

  c) We can use URL actions to link to additional information about the data

  ~~d) To customize links based on our data, we cannot automatically enter field values as parameters in URLs.~~

  __Explanation__

  For URL actions in Tableau to customize links based on your data, you can automatically enter field values as parameters in URLs.
  Also, URL action is a hyperlink that points to a web page, file, or other web-based resource outside of Tableau. We can use URL actions to create an email or link to additional information about our data.

- Add dashboard actions  

  __QUIZ__

  How can we manually add separate device layout in Tableau? – 

  __a) Open a dashboard -> On the Dashboard tab on the left, click Device Preview -> Take a moment to click through the Device types and Models and explore the different screen sizes ->Also there is a button to turn the dashboard into landscape or portrait mode__

  b) Open a dashboard -> On the Analytics tab on the left, click Device Preview -> Take a moment to click through the Device types and Models and explore the different screen sizes ->Also there is a button to turn the dashboard into landscape or portrait mode

  c) Open a Worksheet -> On the Dashboard tab on the left, click Device Preview -> Take a moment to click through the Device types and Models and explore the different screen sizes ->Also there is a button to turn the dashboard into landscape or portrait mode

  d) Open a dashboard -> On the Dashboard click on Format tab and select Device Preview -> Take a moment to click through the Device types and Models and explore the different screen sizes ->Also there is a button to turn the dashboard into landscape or portrait mode

  Explanation: To manually add separate device layouts we need to open a dashboard. On the Dashboard tab on the left, click Device Preview. Then take a moment to click through the Device types and Models and explore the different screen sizes. Also there is a button to turn the dashboard into landscape or portrait mode

- Modify existing dashboard layout for mobile devices 

- Create a story using dashboards or views 
  
  - Story points direct the viewer to the specific insights you want them to focus on.
  
    __QUIZ__
  
    How can we create a story in Tableau? – 
  
    a) Go to Analysis -> Click on New Story -> Select Ok
  
    b) Go to File -> Click on New Story -> Select Ok
  
    __c) Click the New Story tab -> In the lower-left corner of the screen, choose a size for the story -> Double click on any sheet or dashboard to put inside the story -> By default the story name gets its title from the -> Click Add a caption to summarize the story point.__
  
    d) Go to Data -> Click on New Story -> Select Ok
    Explanation: To create a story in Tableau we need to follow the below steps -
  
    Step 1: Click the New Story tab -> In the lower-left corner of the screen, choose a size for the story
  
    Step 2: Double click on any sheet or dashboard to put inside the story -> By default the story name gets its title from the -> Click Add a caption to summarize the story point.
    Question
  
- Share a twbx as a PDF - Share a twbx as an image 

  __QUIZ__

  How can we publish a workbook for Tableau? – 

  __a) Open the desired workbook for publish. Go to File. Click on Save to Tableau Public As. Sign in to the server. Name the workbook for publish. Ok__

  b) Open the desired workbook for publish. Go to Data. Click on Save to Tableau Public As. Name the workbook for publish. Ok

  c) Open the desired workbook for publish. Go to Analytics. Click on Save to Tableau Public As. Name the workbook for publish. Ok

  d) Open the desired workbook for publish. Go to Format. Click on Save to Tableau Public As. Name the workbook for publish. Ok

  __Explanation__

  To publish a workbook of Tableau to the server we need to follow the below steps –
  Step 1: Open the desired workbook for publish -> Go to File
  Step 2: Click on Save to Tableau Public As -> Sign in to the server

  Step 3: Name the workbook for publish -> Ok

  

  __QUIZ__

  How can we export a view as an image file in Tableau? – 

  a) Select Data > Export> Image -> Click Save -> In the Save Image dialog box, specify a file location, name, and format. Then click Save

  __b) Select Worksheet > Export> Image -> In the Export Image dialog box, select the elements we want to include in the image. If the view contains a legend, under Image Options, select the legend layout -> Click Save -> In the Save Image dialog box, specify a file location, name, and format. Then click Save__

  c) Select Format > Export> Image -> Click Save -> In the Save Image dialog box, specify a file location, name, and format. Then click Save

  d) Select Worksheet -> Click Save as -> In the Save Image dialog box, specify a file location, name, and format. Then click Save

  __Explanation__

  To export a view as an image file in Tableau we need to follow the below steps –
  Select Worksheet then select Export and then select Image. In the Export Image dialog box, select the elements we want to include in the image. If the view contains a legend, under Image Options, select the legend layout. Then click Save and in the Save Image dialog box, specify a file location, name, and format. Then click Save.

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

  
  
  __QUIZ__
  
  In Tableau, a discrete field is shown in which color? – 
  
  a) Red
  __b) Blue__
  c) Green
  d) Yellow
  __Explanation__
  
  In Tableau, Blue measures and dimensions are discrete. Discrete values are treated as finite. Generally, discrete fields add headers to the view.
  Whereas. Green measures and dimensions are continuous. Continuous field values are treated as an infinite range. Generally, continuous fields add axes to the view.
  
  __QUIZ__
  
  Which of the following is true for Measures in Tableau? – [Select all that Apply] 
  
  __a) Measures contain numeric, quantitative values__
  b) Measures contain qualitative values (such as names, dates, or geographical data)
  c) Measures can be used to categorize, segment, and reveal the details in the data
  __d) Measures can be aggregated__
  
  __Explanation__
  
  In Tableau, Measures contain numeric, quantitative values that we can measure. Measures can be aggregated. When we drag a measure into the view, Tableau applies an aggregation to that measure (by default).

### Aggregation 

- Explain why Tableau aggregates measures 

  __QUIZ__

  Which of the following are the differences between dimensions and measures? – [Select all that Apply]

  __a) Measures contain quantitative values whereas Dimensions contain names, dates or Geographical data__

  b) Measures contain continuous values with green pills whereas dimensions contain discrete values with blue pills.

  c) Dimensions contain numeric, quantitative values whereas Measures can be used to categorize, segment, and reveal the details in the data

  d) Dimensions are aggregated when added to the view, while measures increase the level of detail in the view.

  __e) Dimensions increase the level of detail in the view while measures are aggregated when added to the view.__

  __Explanation__

  In Tableau, Measures contain numeric, quantitative values whereas Dimensions can be used to categorize, segment, and reveal the details in the data and also Dimensions contain Names, Dates or Geographical data. Also in Tableau even if Measures are generally aggregated however even Dimensions can be aggregated.

  __QUIZ__

  Which of the following is true about the display of a discrete field when dragged to Color in Marks Card? 

  a) When dragged to the color of marks card, Tableau displays a palette with colors based on the order of the field values.

  b) When dragged to the color of Marks Card, Tableau displays a quantitative legend with a continuous range of colors.

  __c) When dragged to the color of Marks Card, Tableau displays both the categorical palette and a legend with a color for each value of the field.__

  d) When dragged to the color of Marks Card, Tableau displays a stepped color gradient.

  __Explanation__

  In Tableau, when we drop a discrete field on Color in the Marks card, Tableau displays a categorical palette and assigns a color to each value of the field.

  __QUIZ__

  What are the differences between discrete date and continuous date values? [Select all that Apply] 

  a) Discrete date part color is Blue whereas the Continuous date part color is Green

  b) Discrete date creates labels whereas the Continuous date creates axes

  c) Discrete date aggregates data at the selected unit whereas the Continuous date uses individual date values

  ~~d) Continuous date part color is Blue whereas the Discrete date part color is Green~~

  __Explanation__

  In Tableau, Discrete date part color is Blue whereas the Continuous date part color is Green , Discrete date aggregates data at the selected unit whereas the Continuous date uses individual date values.

  

- Describe how an aggregated measure changes when dimensions are added to the view 

  - Dimensions increas the granularity (also called level of detail) of the view.

    __QUIZ__

    How can we disaggregate data in Tableau?

    a) For any visualization Go to File -> Uncheck the Aggregate Measures

    b) For any visualization Go to Data -> Uncheck the Aggregate Measures

    c) For any visualization Go to Worksheet -> Uncheck the Aggregate Measures

    __d) For any visualization Go to Analysis -> Uncheck the Aggregate Measures__
    __Explanation__

    In Tableau, to disaggregate the data we need to go to Analysis and uncheck the Aggregate Measures for any visualization.

  __QUIZ__

  How can we change the aggregation of a measure in Tableau? 

  a) For any visualization right click on the measure -> Go to Aggregate -> Select any of the desired aggregate for that measure

  b) For any visualization right click on the measure -> Go to Analysis -> Select any of the desired aggregate for that measure

  __c) For any visualization right click on the measure -> Go to Measure -> Select any of the desired aggregate for that measure__

  d) For any visualization right click on the measure -> Go to Format -> Select any of the desired aggregate for that measure
  __Explanation__

  In Tableau, to change the aggregation of a measure we need to visualization right click on the measure and then go to Measure. Select any of the desired aggregate for that measure.

  



[For More Quiz](https://learningtableau.com/quiz/specialist-quiz-understanding-tableau-concepts/)











## Timeliness 

Completing a task effectively and efficiently has become a standard that organizations expect from employees. This exam is timed because we view time as a critical competency needed to be successful. 