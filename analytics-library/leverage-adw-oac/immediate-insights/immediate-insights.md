# Immediate Basic Insights on Data

## Introduction

When creating a Project out of a Data Set, you'll see a blank canvas.  
We are going to avoid the _blank canvas syndrome_  using **Explain**. Explain uses machine learning (**ML**) to find useful insights about your data. 

_Estimated Lab Time:_ 25 minutes

![Explain](./images/explain0.png)

### Objectives

- Use Explain to get immediate basic insights on data

### Prerequisites  

* An Oracle Cloud Free Tier or Paid
* You have completed  
  Lab 1: Provisioning your Autonomous Database instance  
  Lab 2: Provisioning your Oracle Analytics Cloud instance  
  Lab 3: Connecting OAC to ADW and adjusting Data Set properties

## **STEP 1**: Create a Project

1. ### Create your first Project

    After you have applied the [starter file script](files/starter-file.sql) and run the SQL code with ["Lab 2: Provisioning your Oracle Analytics Cloud instance"]("../../provision-oac/provision-oac.md"), you can quickly **create** your **Project**.  
    Go to top right and click **Create Project** button.
    ![Create Project](../immediate-insights/images/createproject.png)

    An empty **Canvas** is presented in **Visualization** tab  
    ![Create Project](../immediate-insights/images/blankcanvas.png)    

    Before drowning into details, let us give you a quick **explanation** of the different parts of this screen. This will help you to easily follow the next steps.

    An **Oracle Analytics Project** consist of **three main parts** (you can see them at the top center part of the screen):
    ![OAC Navigation](./images/lab300_23b.png)  
     - **Prepare**: Here is where you configure your data. You get a preview of each dataset on the project. You enrich it by adding columns, hiding or renaming the available ones. You can also define joins between datasets here  
     - **Visualize**: Here is where you explore and Analyze the data. You can create several canvases to hold the different visualizations you define  
     - **Narrate**: Here is where you create a more presentation-oriented view of the analysis you created. This tab allows you to choose which insights to show and add comments and descriptions. It helps to understand your analysis journey and focus on showing the results

    During this workshop, you will use the **Prepare** and **Visualize** tabs mainly.

    You have already seen the **Prepare** screen on previous steps.  
    The **Visualize** screen is this one:  
    ![OAC - Canvas explanation](./images/lab300_24a.png)

    Main areas to note here are:  
    - **Elements Pane**: Contains all fields from your datasets to be used in the project  
    - **Properties Pane**: Allows you to define the properties and parameters of the selected object. If it is a column it will be highlighted in blue (in the screen PROD_ID in the Explorer menu is selected), if it is a graphic from the canvas it will have a thin blue borderline around it  
    - **Visualization Grammar Pane**: Contains definition of the selected Visualization, which fields to use and where (Axis, Filters, Trellis Groups...)
      > After you’ve selected the Data Sets for your project, you can begin to add data elements such as _measures_ and _attributes_ to visualizations
    - **Canvas**: Your play area. You can place your visuals here. You can also create more Canvases and copy/move visuals around

    Some of the **options** are **context based**, so we’ll get a better idea once we start working on it

2. Now that you know a bit your way around in the **Project**, you can continue with the lab.

    > **Remember** that you have just added the new dataset from the **DCA_SALES_DATA** table.
  
    Let’s start by letting the system to generate insights.  
    This is the **Explain** feature.  
    
    It works for both for **Attributes** and **Measure** columns, and helps to analyze important and non-obvious patterns in data.
    The insights that Explain delivers are based on the column type or aggregation that you chose and will vary according to the aggregation rule set for the chosen metric. Explain generates only the insights that makes sense for the column type that you chose.  
      - **Attributes**  
       - **_Basic Fact insights_** (distribution across categories)  
       - **_Key Drivers_** list columns that influence attribute values and their distribution  
       - **_Segment_** tab visualizes segments where value for the attribute can be identified with certain confidence based on other columns in the dataset  
       - **_Anomalies_** tab performs combinatorial analysis between selected attribute and other attribute columns and shows groups that exhibit unexpected behavior
    
      - **Measures**  
       - **_Basic Facts_**  
       - **_Anomalies_** insights based on the aggregation rule

    2.1 In Data Pane Select **# VALUE**, Right-Click and select **Explain VALUE**  
    ![Explain Value](./images/explainvalue.png)  
    Explain displays its findings to you as text descriptions and visualizations. You can select key visualizations and add them to your project's canvas.

    2.2 A new page is opened. Explain on metric provides basic facts and anomalies based on aggregation rule  
    ![Explain Value](./images/explainvalue2.png)  

    2.3 Interesting visuals can be selected to be added to the canvas.  
      2.3.1 Scroll down, hover the mouse over **SALES_DATE**; **Category** and click on top right of the insight its checkmark (_Select for Canvas_) ![Explain Value](./images/explainvalueselectforcanvas3.png)  
      ![Explain Value](./images/explainvaluebasicfacts.png) 

      2.3.2 Anomalies tab exhibits groups in the data that show unexpected results. Select first two visualizations and click on top right of the insight (_Select for Canvas_)  
      ![Explain Value](./images/explainvalueanomalies.png) 

      2.3.2 Go on top right of the page and click **Add Selected** ![Explain Value](./images/explainvalueaddselected.png) 

      2.4 Returning to the canvas you notice the 4 selected insights as visualizations.  
      > Note that the canvas name has changed to **Explain VALUE** and under _My Calculations_ you get 2 new measures and 2 new attributes.  
      ![Explain Value](./images/explainvaluecanvas.png) 

   2.5 Let's now **select** an **attribute** column which generates basic factual insights, key drivers, segments and anomalies.
  
   In Data Pane Select **SUB_CATEGORY**, Right-Click and select **Explain SUB_CATEGORY**  
     2.5.1 Check visuals and then close the page (Click **Close** ![Close](./images/explainsubcategoryclose2.png)) 
    ![Explain Sub-Category2](./images/explainsubcategory2.png)

You have just finished to explore **Explain** **ML** feature, which enable insights that you can immediately start with, instead of a blank canvas.

You may now [proceed to the next lab](#next)

## Want to Learn More? 
- Free [Udemy: Modern Data Visualization with Oracle Analytics Cloud](https://www.udemy.com/augmented-analytics/), Section 4, Topic 28. Augumented Analysis using Explain Feature
- [Analyze Data with Explain](https://docs.oracle.com/en/middleware/bi/analytics-desktop/bidvd/analyze-data-explain.html#GUID-D1C86E85-5380-4566-B1CB-DC14E0D3919E)

## **Acknowledgements**

- **Author** - Lucian Dinescu, Product Strategy, Analytics
- **Contributors** - Priscila Iruela, Database Business Development | Juan Antonio Martin Pedro, Analytics Business Development Victor Martin, Melanie Ashworth-March, Andrea Zengin
- **Last Updated By/Date** - Lucian Dinescu, January 2021

## Need Help?
Please submit feedback or ask for help using our [LiveLabs Support Forum](https://community.oracle.com/tech/developers/categories/livelabsdiscussions). Please click the **Log In** button and login using your Oracle Account. Click the **Ask A Question** button to the left to start a *New Discussion* or *Ask a Question*.  Please include your workshop name and lab name.  You can also include screenshots and attach files.  Engage directly with the author of the workshop.  
Please contact us at  analyticsenablement_us_grp@oracle.com for any suggestions or challenges you might have with **Oracle Analytics** labs.

If you do not have an Oracle Account, click [here](https://profile.oracle.com/myprofile/account/create-account.jspx) to create one.