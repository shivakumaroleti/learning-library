# Geo Maps and Custom Binning

## Introduction

In this lab, you will learn about plotting the data on a map and Binning.

_Estimated Lab Time_: 20 minutes

![Connect Data Sets](../geo-maps/images/geo-maps.png)

### Objectives

* Custom Binning
* Geo Maps

### Prerequisites

* An Oracle Cloud Free Tier or Paid
* You have completed  
    * Lab 1: Provisioning your Autonomous Database instance
    * Lab 2: Provisioning your Oracle Analytics Cloud instance
    * Lab 3: Connecting OAC to ADW and adjusting Data Set properties
    * Lab 5: Gaining Insights with Visual Data Dialog
    * Lab 6: Monitoring and Ad-hoc scaling up ADW activity for optimal OAC experience
    * Lab 7: Building simple Interactive Analysis
    * Lab 8: Mashing up additional Data Sets, Contextual Data Preparation

## **STEP 1**: Custom Binning

Lets analyze the issue of losing customers further with the new Data Set.

1.  Delete Donut Visualization.  
Select second visualization 
Go to **Menu** and select **Delete** Visualization

    ![Delete Visualization](../geo-maps/images/delete-viz.png)

2.  Expand **Customers** Data Set.  
Select **MARITAL_STATUS** and Drag and Drop it to **SUB_CATEGORY** 

    ![Add Marital Status](../geo-maps/images/add-maritalstatus.png)


3.  Create Data Set.  
Click **Create Data Set** button, Click 'Drop data file here or click to browse' area and Select the location where you've copied 'customers.xlsx' file.

    ![Add Data Set](../geo-maps/images/add-dataset2.png)

4.  Lets change the properties of the Data Set.  
Set **CUST_ID** as an **Attribute** so that we can join to our existing Data Set.  
Click on **CUST_ID** column, go to **General Property Pane** from bottom left, click on the default 'Match' properties from **Treat As** General Properties and change to **Attribute**.

    ![Treat As Attribute](../geo-maps/images/prepscript-custidasattribute.png)

5.  Set **AGE** column as an **Attribute**.  
Click on **AGE** column, go to **General Property Pane** from bottom left, click on the default 'Measure' properties from **Treat As** General Properties and change to **Attribute**.

    ![Treat As Attribute](../geo-maps/images/prepscript-ageasattribute.png)

6.  Add the new Data Set.  
Click **Add** button from top right.

    ![Add Data Set](../geo-maps/images/add-dataset3.png)

7.  Recommendations on columns are available for the new Data Set as well.  
Lets enhance the city column with population.  
Select **CITY** column and choose **Enhance CITY with Population** from recommendations.

    ![Enhance City with Population](../geo-maps/images/prepscript-enhancewithpopulation.png)

8.  Lets **group** **Income** into **3 bins**.  
_Below 70_ in one group, _70-130_ in another and the last group in _Above 130_.  
Select **INCOME_LEVEL** column, go to **Options** and Click **Group**.

    ![Group](../geo-maps/images/prepscript-group.png)

9.  First group **Below 70**.  
Type **Below 70** (instead of Group 1) and select A, B and C.

    ![Below 70](../geo-maps/images/prepscript-group1.png)

10.  Add first group. 
Click on '+' sign

     ![Add 1st Group](../geo-maps/images/add-group.png)

11.  Add second group.  
Type **From 70 to 130**  (instead of Group 2)  and select D, E and F

     ![From 70 to 130](../geo-maps/images/prepscript-group2.png)

12.  Add second group.  
Click on '+' sign

     ![Add 2nd Group](../geo-maps/images/add-group2.png)

13.  Add third group.  
Type **Above 130**  (instead of Group 3), select **Add All**.

     ![Above 130](../geo-maps/images/prepscript-group3.png)

14. Type **Income Group** to Name, Click **OK** and Click **Add Step**.

     ![Add Income Group](../geo-maps/images/prepscript-group4.png)

14. Apply Script to activate the changes.  
Click **Apply Script**.

     ![Apply Script](../geo-maps/images/apply-script.png)

## **STEP 2**: Join the Data Sets

When you add more than one data set to a project, the system tries to find matches for the data that’s added. It automatically matches external dimensions where they share a common name and have a compatible data type with attributes in the existing data set.  
Lets join the Data Sets using **CUST_ID** as the join condition between the data sets.

1.  Go to **Data Diagram** tab.  
In this tab, you can view a representation of the **different datasets** included in the project and their **relationships**.  
Click on **Data Diagram** tab

    ![Data Diagram](../geo-maps/images/datadiagram.png)

2.  **Connect** Data Sets.  
Currently, there is no relationship defined, so you see both as isolated boxes.  
Hover the mouse  over the imaginary line **between** the two Data Sets and click on the **0 number** that will appear.

    ![Connect Data Sets](../geo-maps/images/datadiagram-join.png)


3.  **Blend Data** Sets.  
A **pop-up window** appears allowing you to define a **new relation** between the datasets (join).  
Click on **Add Another Match** button.

    ![Blend Data Sets](../geo-maps/images/datadiagram-blend1.png)

4.  **Blend Data** Sets.  
Select **CUST_ID**column from both Data Sets.

    ![Blend Data Sets](../geo-maps/images/datadiagram-blend2.png)

5.  Lets extend the new Data Set as a dimension as the mashup data set doesn't contain any metrics.  
Click **Add Facts** and select **Extend a Dimension**.

    ![Extend a Dimension](../geo-maps/images/datadiagram-blend3.png)

6.  Click **OK** button.

    ![OK](../geo-maps/images/datadiagram-blend4.png)

7. Click **Visualize** tab

    ![Visualize](../geo-maps/images/visualize.png)

You have just finished learning about data mash-up and various options to connect Data Sets.

You may now [proceed to the next lab](#next)

## Want to Learn More?

* [Blend Data that You Added](https://docs.oracle.com/en/cloud/paas/analytics-cloud/acubi/blend-data-that-you-added.html)
* [About Mismatched Values in Blended Data](https://docs.oracle.com/en/cloud/paas/analytics-cloud/acubi/mismatched-values-blended-data.html)
* [Change Data Blending in a Project](https://docs.oracle.com/en/cloud/paas/analytics-cloud/acubi/change-data-blending-project.html)

## **Acknowledgements**

- **Author** - Lucian Dinescu, Product Strategy, Analytics
- **Contributors** -
- **Last Updated By/Date** - Lucian Dinescu, February 2021

## Need Help?

Please submit feedback or ask for help using our [LiveLabs Support Forum](https://community.oracle.com/tech/developers/categories/livelabsdiscussions). Please click the **Log In** button and login using your Oracle Account. Click the **Ask A Question** button to the left to start a *New Discussion* or *Ask a Question*.  Please include your workshop name and lab name.  You can also include screenshots and attach files.  Engage directly with the author of the workshop.  
Please contact us at  analyticsenablement_us_grp@oracle.com for any suggestions or challenges you might have with **Oracle Analytics** labs.

If you do not have an Oracle Account, click [here](https://profile.oracle.com/myprofile/account/create-account.jspx) to create one.