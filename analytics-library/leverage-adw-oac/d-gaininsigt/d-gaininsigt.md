# Asking direct questions on data 

![BI ASK](./images/biask0small.png)

## Introduction
When creating a Project out of a data set, you'll see a blank canvas.  
This time we are going to avoid _blank canvas syndrome_  using **BI Ask**, which is the search bar on the Home page to find the data and quickly visualize it.

**BI Ask** (**N**atural **L**anguage **Q**uery **P**rocessing) promotes direct interactions between the users and the BI System to explicitly understand what every user is interested in.  
Interprets semantic layer, user private data, expression library and catalog artifacts and generates on-the-fly queries – visualizations.


    Estimated Lab Time: 40 minutes

### Objectives

- **Use BI Ask to ask (or type) direct questions (Natural Language) on data - desktop/laptop**
- **Use BI Ask to ask direct questions (Natural Language) on data - mobil (Day by Day)**
- **Troubleshoot and Fine-Tune Searches**

### Prerequisites

* An Oracle Cloud Free Tier or Paid
* You have completed  
["Lab 1: Provisioning your Autonomous Database instance"]("../../provision-adw/provision-adw.md")  
["Lab 2: Provisioning your Oracle Analytics Cloud instance"]("../../provision-oac/provision-oac.md")  
["Lab 3: Connecting OAC to ADW and adjusting Data Set properties"]("../../a-connoactoadw/a-connoactoadw.md")

## **STEP 1**: Certify and Index your Data Set

1. ### Search for your Data Set

    In order to ask (English) questions on the data set, we need to **index** the Data Set to **enable searching**  
    > Note: English it's just an example 
    
    1.1 In the **Oracle Analytics Home** page, click the **Navigator** on top left, and then click **Data**  
    > Note: if you are still on the previous lab, you can quickly Go Back ![Go Back](../c-askdirectquestions/images/biaskgoback.png) to the **Home** page without saving the project  
    ![Data](../c-askdirectquestions/images/biaskconsoledata.png)

    1.2 Select you Data Set
    From **Data** page, then **Data Sets** section identify **DCA_SALES_DATA** Data Set.

    1.3 Click the **Actions menu** of the data set or right-click the Data Set, and click **Inspect**  
    ![Data Set](../c-askdirectquestions/images/dataset.png)
    ![Inspect](../c-askdirectquestions/images/datasetinspectsmall.png)

    1.4 **Certify** the Data Set  
    From **General** tab click **Certify** button  
    ![Certify](../c-askdirectquestions/images/datasetcertify.png)

    1.5 **Index** the Data Set  
    From **Search** tab click **Index Data Set for Searching**  
    ![Idex](../c-askdirectquestions/images/datasetindex.png)

    1.6 **Control access** (optional)  
    Access to the Data Sets can be controlled from **Access** tab  
    ![Control](../c-askdirectquestions/images/datasetcontrol.png)  
    > Note: is best practice to enforce control using **Roles** rather than individual **Users**

    Click **Save** and then **Close** button.

    1.7 Go to **Home** Page
    Click **Navigator** and then select **Home**  
    ![Home Page](../c-askdirectquestions/images/navigatorhome.png)

## **STEP 2**: Ask Questions about your data

1. ### BI Ask
    In the **Home** Page of OAC, a dialog bar appearing at the top can be leveraged to **ask** plain English language questions on the data.
    
    1.1 Click the **Search** bar and **Type** in the bar area "**show me value by sales week**".  
    As you enter the information, the application returns search results in a drop-down list. The system can be searched by column names or data elements or both. Best fit results are returned immediately

    1.2  Press **SHIFT + ENTER** to visualize data  
    ![Visualize Data](../c-askdirectquestions/images/biask.png)

    1.3 Check the results. Insights are rendered immediately from the best matching Data Set  
    ![Visualize Data](../c-askdirectquestions/images/biask1.png)

    1.4 Continue to type in the bar area "**for customers**" and press **SHIFT + ENTER**  
    ![Visualize Data](../c-askdirectquestions/images/biask2.png)
    We observe that we are losing customers over time

    1.4 Continue to type in the bar area "**for direct channel**" and press **SHIFT + ENTER**  
    ![Visualize Data](../c-askdirectquestions/images/biask3.png)

    1.5 Remove the last query.  
    Select  "**for direct channel**" and press the x (remove) sign ![Remove Data](../c-askdirectquestions/images/biask4a.png)

    1.6 Continue to type in the bar area "**by channel**" and press **SHIFT + ENTER**  
    ![Visualize Data](../c-askdirectquestions/images/biask5.png)

    1.7 You have 9 visuals to start with. You can always choose one (or more) and explore it.  
    > Note: optional you can select the first visual, hover over the top left of the visual and choose **Explore as Project** ![Visualize Data](../c-askdirectquestions/images/biaskexploreasproject0.png)  
    ![Visualize Data](../c-askdirectquestions/images/biaskexploreasprojectsmall.png)


2. ### Day by Day
    We should be able to get our questions answered when we are on the go as well. We should be able to move from desktop to mobile seemly, ask the same questions, get the results and more.

    **Oracle Day by Day** is an mobile analytic app that learns what you are interested in, when and where you are interested in it, and who you like to share and collaborate with. Start your day with a smart list of analytics that helps you make better decisions — day by day.

    **Oracle’s Day by Day** has been named a **winner** in the [Ventana Research 13th Annual Digital Innovation Awards](https://www.ventanaresearch.com/resources/awards/innovation#winners) in the category of **Analytics** for 2020.

    It's **supercharging BI Ask** with **context**. Understand who, what, when and where people are interested and eventually why.

    Key Features:  
    - Search based interface  
    - Natural Language Search  
    - Proactive delivery based on Time, Place and Threshold  
    - It will infuse analytics into a users daily activities, and not the other way around  
    - Collaboration with people and other apps

    **2.1 Prerequisites ** 
      2.1.1 Apps prerequisites: Install Day by Day  
      - Search for "**Oracle Day by Day**" app with Google Play or App Store  
      ![Google Play](../c-askdirectquestions/images/daybydayplaystoresmall.png)  
      - Install Day by Day is nothing different from installing any of your casual mobile apps.  
      - Don’t deny apps permissions right from the start; you can always go to your mobile app settings and work on permissions, if necessary.

     2.1.2 OAC prerequisites:  
     - Your **User** must have at least a **BI Content Author** and a **DV Consumer** Role.
         > Note: that's enough for our lab, but in a full enterprise environment you should also [Enable Data Model and Catalog Crawl](https://docs.oracle.com/en/cloud/paas/analytics-cloud/acabi/manage-how-content-is-indexed-and-searched.html#GUID-64DDEF84-75B8-4D0D-A625-17E9538435F0) for your User
     
     - In the **Oracle Analytics Home** page, click the **Navigator** on top left, and then click **Console**  
     ![Console](../c-askdirectquestions/images/biaskconsole.png)

     - From **Configuration** and Administration click **Users and Roles**
      > Note: a new browser page is opening
      
      ![Console](../c-askdirectquestions/images/biaskuserssmall.png)

     - From **Application Role Management** search for your **User** in the search box upper right, then click on **Manage Application Role** ![Console](../c-askdirectquestions/images/biaskuserrole2.png)  
     ![Console](../c-askdirectquestions/images/biaskuserrole.png)

     - From **Manage Roles** click **Search** button and see **Available Applications Roles**  
       > if you already have **BIService Administrator** role you are OK  
       
       > you double-click on **BI Content Author** and a **DV Consumer Role** to move it from the left side to the right side if necessary  
       Click **OK** button.  
       ![Console](../c-askdirectquestions/images/biaskuserrole3.png)

     - Close the new opened browser page, return to the **Console**, click on **Navigator** and select **Home Page**  
     ![Console](../c-askdirectquestions/images/biaskhomepage.png)


    **2.2 Connect to your OAC instance**  
    The prerequsites are met so it's time to connect your mobile to your OAC instance  
    - Enter your instance details: (https<nolink>://name-tenency.analytics.ocp.oraclecloud.com)  
    - Enter your OAC login User Name and Password; if you have enabled SSO in OAC, you have to set up [OAuth](https://docs.oracle.com/en/cloud/paas/analytics-cloud/biday/basics.html#GUID-4AE4B43-56F4-4DAC-8FF1-5FC4B5DE5BB)  
    ![Console](../c-askdirectquestions/images/daybydaylogin.png)

    **2.3 Ask your question**.  
    You can simply speak or type in plain English questions, which gets directed to your data set

     2.3.1 Go to **Search** tab.  
     Click on the microphone icon and speak “**show me value by week and customers by channel**”  
     > Alternatively, you can type the same question
     Questions are parsed and reports are returned which best matches the question, from the best matched data set.  
     
       Search results are listed in this order:  
       1. Data model (semantic layer)  
       2. Certified data sets  
       3. Personal data sets  
       4. Catalog items (projects, analyses, dashboards, and reports)

      ![Speak](../c-askdirectquestions/images/daybydaysearch3.png)

    **2.4 Add visuals to your feeb**.  
    Interesting visuals can be added to daily feeds. The daily feeds appear on the Home screen when the user logs in every time.  
    Choose two visuals, click on the 3 dots and select **Add to Your Feed**  
    ![Speak](../c-askdirectquestions/images/daybydayaddfeed.png)    

    **2.5 Comment**.  
    Choose a visual, click on the 3 dots and select **Comments**. Speak or type “**Please review ASAP**”  
    ![Comment](../c-askdirectquestions/images/daybydaycomment.png)
      > Note: see “**1 comment**” ![Comment](../c-askdirectquestions/images/daybydaycomment1small.png) at the bottom of the feed

## **STEP 3**: Troubleshoot and Fine-Tune Searches

This topic  briefly describes common problems that you might encounter, and suggestions to fine-tune your searches.

1. ### Connectivity  
If the app can’t connect to the server, then: 

   **1.1 Verify the URL format** of the server in the app.  
   The URL format must be https://<nolink>hostname:port for example, https<nolink>://oacserver.com:443  

   **1.2 Run the Users Service End Point test**.  
   Using a desktop browser, navigate to https://oacserver.com:443/bimajel. A page with a link for the Users Service End Point test must be displayed
   
   **1.3 Test the URL** for the server in a browser on a computer. After confirming that the URL works properly in that browser, enter the same URL in a browser on the mobile device.  
   
   **1.4 Certificate issues.**  
    Be aware of warnings for bad certificates in the address bar and when loading a page on the desktop or on the mobile device

2. ## BI ASK Troubleshooting, No Suggestions

   **2.1 Check ASK on the Home Page** - Verify it Returns Suggestions  
   Type in the ASK bar on the home page and verify that suggestions are returning. 

   **2.2 Verify that Indexes are Created**  
   Verify that the index has but run for at least one subject area. **Run index** again in case it is corrupt

   **2.3 Verify Security**  
   User must be at least a BI Content Author and a DV Consumer. Make sure you are searching for a term that exists

3. ## No Results or Missing Results  

   **3.1 Check ASK on the Home Page **- Verify it Returns Suggestions
   > Understand Matched vs Unmatched Terms.  
   Remember ASK on the desktop only supports matched terms, Day by Day supports either.  
   Unmatched terms may not always return what you expect.

   **3.2 Verify Security**  
   User must be at least a BI Content Author and a DV Consumer. Make sure you are searching for a term that exists

4. ## App Specific Issues  

   **4.1 Notification Issues**  
     4.1.1 Verify Notifications are Enabled  
     - Android – Settings | Apps | Day by Day | Show Notifications  
     - iOS - Settings | Day by Day | Notifications | Allow Notifications 

    4.1.2 Verify Do Not Disturb Options  
    - Android – Settings | Do Not Disturb  
    - iOS - Settings | Do Not Disturb

    4.1.3 Test with a Simple Bring Back  
    - Do a quick search and set any card as a bring back in 2 minutes  
    - Send the app to the background lock the device and wait 2 minutes

5. ## Location Issues  

   **5.1 Verify Location Services** are Enabled  
   - Android – Settings | Apps | Day by Day |Permissions  
    - iOS - Settings | Day by Day | Location

   **5.2 Check for Low Power Mode** or **WIFI Disabled**

   **5.3 Test with a Simple Bring Back by Location**

6. ## Other Issues  

   **6.1 Cannot Upload Profile Image**  
   - Verify Camera and Photo Access  
   - Check Image Size (larger then 1 MB)

7. ## Fine-Tune Searches

   **7.1 Avoid special characters** in your indexes, especially in terms from your subject areas

   **7.2 Don’t index any field** names whose value includes a large amount of text or confidential information

   **7.3 Try to flatten hierarchies** or avoid indexing hierarchies

   **7.4 Minimize the number of duplicate dimensions**

   **7.5 Create synonyms** to handle search queries
   > Please check [Configuring Synonyms for ASK Interface](http://oracledataviz.blogspot.com/2018/11/un-documented-beta-oac-1833-feature.html) blog

   **7.6 Expand acronyms** because they aren’t easily understood when searching
   > In a voice query, say “percent” or “percentage” rather than “p-c-t”.

   **7.7 Ensure** that your **security** settings improve and personalize what users see

   **7.8 Ensure** that the administrator has **Certified the Data Sets** that users need to find

You have just finished to learn how to ask direct questions to your data using **BI Ask** in both desktop and mobile flavour as well as basic troubleshooting and index tips.  
> Optional: you can check in the next [video](https://youtu.be/uEESc7yo6kA) how BI Ask engine works with OAC DV and Day by Day in a side by side comparison  
[](youtube:uEESc7yo6kA)

**This concludes this lab. Please proceed to the next lab in the Content menu.**

## Want to Learn More? 
- [Troubleshoot Indexing](https://docs.oracle.com/en/cloud/paas/analytics-cloud/acabi/troubleshoot-indexing.html)
- [Using Search and BI Ask](https://docs.oracle.com/en/cloud/paas/bi-cloud/bilug/using-search-and-bi-ask.html#GUID-97F546AE-6277-45AB-B5A7-C55E2328AC0E)
- [Natural Language Interview with Jacques Vigeant](https://www.youtube.com/watch?v=piE1ah51DnE&feature=youtu.be)
- [Oracle’s Day By Day: Transforming The Way People Consume Analytics](https://blogs.oracle.com/analytics/oracle%e2%80%99s-day-by-day:-transforming-the-way-people-consume-analytics?source=:em:nw:mt:RC_PDMK190606P00196:OACBLOGJUL20WK4&elq_mid=168112&sh=15062418261323181322082406290313253035&cmid=PDMK190606P00196C0058)
- [Using Oracle Analytics Day by Day](https://docs.oracle.com/en/cloud/paas/analytics-cloud/biday/basics.html#GUID-8D2A7AA1-37E0-4862-9FD9-DEE1179E5D69)

## **Acknowledgements**

- **Author** - Lucian Dinescu, Product Strategy, Analytics
- **Contributors** - 
- **Last Updated By/Date** - Lucian Dinescu, January 2021

## Need Help?
Please submit feedback or ask for help using our [LiveLabs Support Forum](https://community.oracle.com/tech/developers/categories/livelabsdiscussions). Please click the **Log In** button and login using your Oracle Account. Click the **Ask A Question** button to the left to start a *New Discussion* or *Ask a Question*.  Please include your workshop name and lab name.  You can also include screenshots and attach files.  Engage directly with the author of the workshop.  
Please contact us at  analyticsenablement_us_grp@oracle.com for any suggestions or challenges you might have with **Oracle Analytics** labs.

If you do not have an Oracle Account, click [here](https://profile.oracle.com/myprofile/account/create-account.jspx) to create one.





TO BE COPIED IN THE NEXT LAB!!!!!!!!
-----------------------------------------------
2. Now that you know a bit your way around in the **Project**, you can continue with the workshop.

    **Remember** that you just added the new dataset from the **SH&#95;SALES** table.

    All the number-type columns from this table are treated as **NUMBER** by default. You can check the information on the **Properties** section of each table column under the Data Type section.

    ![SH-SALES Properties](./images/lab300_25.png)

3. Select **AMOUNT&#95;SOLD** column from the TABLE panel and add **Aggregation** rule **SUM** from the COLUMNS detail panel from the bottom. By default **Aggregation** value, will be **SUM**, just confirm that it is the case, otherwise change it.

    ![SH-SALES Aggregation](./images/lab300_26.png)

4. We will **add Month** to your selection: **Hold the Control Button on your Keyboard** and expand **TIME_ID** and select **Month**, after right click of your mouse and select **Create Best Visualization**.

    ![SH-SALES Create Visualization](./images/lab300_27.png)

5. Verify that the **information** that is showing in the canvas is the following:

    **Line, Values (Y-Axis) &#45;&#45; AMOUNT&#95;SOLD, Category (X-Axis) &#45;&#45; TIME&#95;ID (Month)**.

    ![SH-SALES Verify information](./images/lab300_28.png)

6. Right click on the chart, select **Add Statistics** and **Trend Line**.

    ![SH-SALES - Add Statistics](./images/lab300_29.png)

7. In the **Properties** panel at the very bottom of the page in the **Trend** section change 95% to **Off**.

    ![SH-SALES - Properties](./images/lab300_30.png)
    ![SH-SALES - Trend](./images/lab300_31.png)

    Although we had some ups and downs in the **totals**, you see that in the overall the total amount sold has been trending up, meaning our **sales are in good shape**.

    We will compare this information (**AMOUNT&#95;SOLD by TIME&#95;ID (Month)**) to our active customer base over time. To find the number of active customers, we will "**count distinct**" on **CUST&#95;ID on a Monthly basis**.

9. Select **CUST_ID** column from the TABLE panel and add **Aggregation** rule **Count Distinct** from the **COLUMNS** Properties panel from the bottom.

    ![SH-SALES Aggregation](./images/lab300_32.png)

10. Be sure you drag **CUST&#95;ID** column to the Values (**Y-Axis**) section with your mouse in the canvas. Be sure it is added AMOUNT&#95;SOLD and not replace it. Right click on **CUST&#95;ID** and select **Y2 Axis** as part of the **CUST&#95;ID** details.

    ![SH-SALES Aggregation Drag](./images/lab300_33.png)

    ![SH-SALES canvas](./images/lab300_34.png)

    This **results** shows you that the number of customers is going down but the amount sold is going up, so we are **selling more to less customers**.

    We will create a **new Data Set** of data to enrich the **canvas**.

11. Click the **+** bottom in the left top corner of the Analytics Cloud Page and **Add Data Set**.

    ![Add New Data Set](./images/lab300_35.png)

12. Select **Create Data Set**.

    ![Create Data Set](./images/lab300_36.png)

13. Select **WORKSHOPADWOAC**.

    ![Create Data Set - WORKSHOPADWOAC](./images/lab300_37.png)

14. Click on the **SH** (Sales History) schema.

    ![Create Data Set - SH](./images/lab300_38.png)

15. Select **PRODUCTS** table from the *SH schema*.

    ![Create Data Set - Products](./images/lab300_39.png)

    This will display the columns available in the **PRODUCTS** table.

16. Select **Add All** to select all columns in the table.

    ![Create Data Set - Products - Add All](./images/lab300_40.png)

17. Then, to create the Data Set, select **PRODUCTS** at the top of the page or at the right side of the selection panel depend the version of OAC that you are using to **modify the Data Set** that we are creating right now.

    ![Create Data Set - Modify](./images/lab300_41.png)

    Use the following information to configure your **Data Set**:

    > **Data Access**: Live
    >
    > **Name**: SH&#95;PRODUCTS

18. Then **Add** to create the **Data Set**.

    ![SH-PRODUCTS](./images/lab300_42.png)

    The **Data Set** was successfully **saved**.

    ![SH-PRODUCTS Saved](./images/lab300_43.png)

    Now we have to join the new Data Set, **SH&#95;PRODUCT**, to the data set that we created a few steps before **SH&#95;SALES**.

    You will notice that we have been redirected to the **Prepare** section of the project.

    At the **bottom of the screen**, you can see three tabs, one per each dataset and another one called **Data Diagram**. **Click** on **Data Diagram**.

    ![Navigation - Prepare](./images/lab300_44.png)

    In this tab, you can view a representation of the **different datasets** included in the project and their **relationships**. Currently, there is no relationship defined, so you see both as isolated boxes.

    Hover over the imaginary line **between** them and click on the **0 number** that will appear:

    ![Connect Sources - O](./images/lab300_45.png)

19. A **pop-up window** appears allowing you to define a **new relation** between the datasets (join). Click on **Add Another Match**.

    ![Connect Sources - Add Match](./images/lab300_46.png)

20. Select **PROD_ID** under each Data Set, **SH&#95;PRODUCTS** and **SH&#95;SALES** in the **Select Data** Section.

    ![Connect Sources - SH-SALES & SH-PRODUCTS ](./images/lab300_47.png)

    > **NOTE**: You might see a balloon warning about using **PROD_ID** as a **Measure**. Do not worry about it. It is just a kind reminder that you are using a column that looks like a number only as a join column, but that is exactly what we want to do.

    ![Connect Sources - Measure](./images/lab300_48.png)

21. We will add the new dataset as a **Dimension** to this section. Click **Add Facts** and select **Extend a Dimension**.

    ![Connect Sources - Dimension](./images/lab300_49.png)

22. Select **OK**.

    ![Connect Sources - OK](./images/lab300_50.png)

    The **connection** between the two sources has been **created**.

    ![Connect Sources - Created](./images/lab300_51.png)

23. Now that the **preparation** of the data is done, you can navigate again to **Visualize** page in the right top corner of the **Analytics Cloud Home Page**.

    ![OAC Navigation](./images/lab300_52.png)

24. In the canvas go to **TIME_ID** section, **Show by** and select **Quarter** instead Month.

    ![OAC canvas Quarter](./images/lab300_53.png)

25. Apply the **Quarter** filter and the graph will **change dynamically**.

    ![OAC canvas Quarter Change Dynamically](./images/lab300_54.png)

    We will eliminate the **Linear Trend Line** that we have in the graph.

26. Click in the **graph** and in the **Properties section** of the bottom of the page, select the **Analytics** icon and click in the **Trend** section to remove the **Linear** section.

    ![OAC canvas Modify](./images/lab300_55.png)

27. We can see the **graph without the Trend Linear line**.

    ![OAC canvas Trend Linear](./images/lab300_56.png)

28. Select **PRODUCT_CATEGORY** from **SH&#95;PRODUCTS** and add it in **the Trellis Columns** section of the canvas.

    ![OAC canvas Trellis Columns](./images/lab300_57.png)

    ![OAC canvas Trellis Columns 2](./images/lab300_58.png)

    You can see now a **trend** on the **amount sold** and the number of distinct customers by product category. This allows you to compare the performance of each product. However, using just lines can be a bit messy. You will try now to make this graphic more appealing.

29. Select **AMOUNT&#95;SOLD** from the canvas and select **Bar** graph.

    ![OAC canvas - Bar](./images/lab300_59.png)

30. Select **Project Properties** from the Burger Menu in the right top corner.

    ![OAC canvas - Projec Properties](./images/lab300_60.png)
    ![OAC canvas - Projec Properties Actions](./images/lab300_61.png)

31. Select in the **Colour Series** and select another **colour** that you prefer.

    ![OAC canvas - Projec Properties Colour](./images/lab300_62.png)

32. Select **OK** after being applied the **colour changes**.

    ![OAC canvas - Projec Properties Select Colour](./images/lab300_63.png)

    ![OAC canvas - Projec Properties New Colour](./images/lab300_64.png)

33. We will save the **Project** in the **Save** section.

    ![OAC canvas - Save](./images/lab300_65.png)

    I saved the project with the name **ADW&#95;OAC&#95;SH&#95;SCHEMA**.

    ![OAC canvas - Save DW_OAC_SH&#95;SCHEMA](./images/lab300_66.png)

34. You can share your project by **email or social media**. Have a look at the **possibilities**.

    Select the Share icon and select **File or Print.**

    ![OAC canvas - File or Print](./images/lab300_67.png)

35. You can choose to **Save** your project in a wide variety of standard formats such as **PowerPoint (pptx), Acrobat (pdf), Image (png), Data (csv), Package (dva)**.  You can choose which parts of your project to include, such as **All Canvas, only the Active Canvas or the Active Visual**.

    ![OAC canvas - Save Options](./images/lab300_68.png)

    The file will be **downloaded** locally on your machine.

    ![OAC canvas - Download](./images/lab300_69.png)

36. When you select **Print**, you can choose which parts of your project to include in the **printed output, such as All Canvas, only the Active Canvas or the Active Visual**. Etc.

    ![OAC canvas - Print](./images/lab300_70.png)

Watch our short recap video that includes an outlook of other functionalities of **Oracle Autonomous Database (ADB)** and **Oracle Analytics Cloud (OAC)**:

[](youtube:/vlojHIcqKBc)

*Congratulations! Well done!*

You have just finished to ...

*You can proceed to the next lab…*

## Want to Learn More? 
- [Troubleshoot Indexing](https://docs.oracle.com/en/cloud/paas/analytics-cloud/acabi/troubleshoot-indexing.html)
- [Using Search and BI Ask](https://docs.oracle.com/en/cloud/paas/bi-cloud/bilug/using-search-and-bi-ask.html#GUID-97F546AE-6277-45AB-B5A7-C55E2328AC0E)
- [Natural Language Interview with Jacques Vigeant](https://www.youtube.com/watch?v=piE1ah51DnE&feature=youtu.be)
- [Oracle’s Day By Day: Transforming The Way People Consume Analytics](https://blogs.oracle.com/analytics/oracle%e2%80%99s-day-by-day:-transforming-the-way-people-consume-analytics?source=:em:nw:mt:RC_PDMK190606P00196:OACBLOGJUL20WK4&elq_mid=168112&sh=15062418261323181322082406290313253035&cmid=PDMK190606P00196C0058)
- 
## **Acknowledgements**

- **Author** - Lucian Dinescu, Product Strategy, Analytics
- **Contributors** - Priscila Iruela, Database Business Development | Juan Antonio Martin Pedro, Analytics Business Development Victor Martin, Melanie Ashworth-March, Andrea Zengin
- **Last Updated By/Date** - Lucian Dinescu, January 2021

## Need Help?
Please submit feedback or ask for help using our [LiveLabs Support Forum](https://community.oracle.com/tech/developers/categories/livelabsdiscussions). Please click the **Log In** button and login using your Oracle Account. Click the **Ask A Question** button to the left to start a *New Discussion* or *Ask a Question*.  Please include your workshop name and lab name.  You can also include screenshots and attach files.  Engage directly with the author of the workshop.

If you do not have an Oracle Account, click [here](https://profile.oracle.com/myprofile/account/create-account.jspx) to create one.