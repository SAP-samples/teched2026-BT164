# Exercise 3 - Scope the Blueprint: Select & Reduce Data - Part 1/2
<p align="justify">In this exercise, you will define the data scope of your digital blueprint by excluding irrelevant company codes, limiting historical data, and filtering transformation objects. These scoping activities help to reduce system size and complexity before the transformation model is created.</p>

This exercise consists of the following sub-exercises:
- [Exercise 3.1 - Select Company Codes](#exercise-31---select-company-codes)
- [Exercise 3.2 - Enable Time Slice](#exercise-32---enable-time-slice)
- [Exercise 3.3 - Select Scanned Tables](#exercise-34---select-scanned-tables)

<br>

## Exercise 3.1 - Select Company Codes
<p align="justify">In this sub-exercise, you will narrow the scope of your digital blueprint by excluding specific company codes to achieve a vertical reduction.</p>

### Steps:
Follow these steps to complete the exercise:<br>
1.  Within your blueprint, select **Transition Readiness**.<br><br>
    ![](/exercises/ex3/images/Screenshot-1-01.png)<br>

    > **💡 TIP**: If you closed the application, reopen [SAP Cloud ALM](https://calm-deep-dive-workshop.us10.alm.cloud.sap) and log in with the user **btc-0XX** (replace *XX* with your seat number, for example **btc-001**). Then navigate to **Transformation** > **Manage Digital Blueprint** and select your blueprint.

2.  From the list, choose **Select Company Codes**.<br><br>
    ![](/exercises/ex3/images/Screenshot-1-02.png)<br>
3.  The **Select Company Codes** application opens, with your blueprint already preselected.<br><br>
    Scroll down to the **Company Codes** table and select all entries except **Company 2000, Inc (2000)** [1]. Then choose **Mass Edit** [2].<br><br>
    ![](/exercises/ex3/images/Screenshot-1-03.png)<br>
4.  For **Scope**, select **Out of Scope**. In **Comment for all objects**, optionally enter a note, for example: **As agreed with the business, I remove these company codes**. Then choose **Save**.<br><br>
    ![](/exercises/ex3/images/Screenshot-1-04.png)<br><br>
    All company codes except **Company 2000, Inc (2000)** are now set to **Out of Scope**.<br>
5.  To review the impact on the data footprint, go to **Related Apps** &gt; **Digital Blueprint Overview**.<br><br>
    ![](/exercises/ex3/images/Screenshot-1-05.png)<br>
6.  The **Digital Blueprint Overview** app opens, preselected with your blueprint.<br><br>
    This view provides detailed charts and dashboards to visualize technical and business information. The **Transformation Objects Summary** chart, for example, shows the ratio between in-scope transformation objects and out-of-scope data. You can see that roughly 30% of the data is now excluded from scope.<br><br>
    ![](/exercises/ex3/images/Screenshot-1-06.png)<br>
7.  Use the **Back** button in the Launchpad to return to your blueprint.<br>
8.  The **All Company Codes in Scope** warning has disappeared, confirming that the scoping adjustment was successful.<br><br>
    ![](/exercises/ex3/images/Screenshot-1-07.png)<br>
9.  Choose **Solution Patterns**.<br><br>
    A solution pattern provides predefined content and transformation rules based on business needs. Because multiple company codes were excluded in the previous step, the **Org Slice** pattern - representing a vertical reduction – is now active.<br><br>
    ![](/exercises/ex3/images/Screenshot-1-08.png)<br>
10. **Congratulations!** You have successfully completed this sub-exercise.<br><br><br>

## Exercise 3.2 - Enable Time Slice
<p align="justify">After excluding selected company codes through the <b>Org Slice</b> pattern, you will now activate the <b>Time Slice</b> solution pattern to apply a horizontal reduction. This limits the migrated data to a specific fiscal period, further reducing system size while preserving the essential business context.</p>

### Steps:
Follow these steps to complete the exercise:<br>
1.  You are already in the **Solution Patterns** tab of your blueprint. From the list, select **Time Slice**.<br><br>
    ![](/exercises/ex3/images/Screenshot-2-01.png)<br><br>
2.  The **Solution Pattern** application opens, showing available configuration options. Choose **Data Distribution** to review the current data footprint by fiscal year.<br><br>
    ![](/exercises/ex3/images/Screenshot-2-02.png)<br><br>
3.  This view provides an overview of how data is distributed across time periods and helps you decide from which fiscal year onward the data should be migrated.<br><br>
    The chart shows the **Total Data Count** across all fiscal years [1] (transactional data) and visualizes the distribution trend. For the hands-on, the **last six fiscal years** are highlighted [2], as the company decided to include only this timeframe in the migration scope.<br><br>
    ![](/exercises/ex3/images/Screenshot-2-03.png)<br><br>
4.  Scroll up and choose **Edit** to activate the pattern.<br><br>
    ![](/exercises/ex3/images/Screenshot-2-04.png)<br><br>
5.  In the Status dropdown, select **Active**.<br><br>
    ![](/exercises/ex3/images/Screenshot-2-05.png)<br><br>
6.  Under **General**, set **Fiscal Year** to **2021** and choose **Apply**.<br><br>
    ![](/exercises/ex3/images/Screenshot-2-06.png)<br><br>
7.  The **Time Slice** is now active. Confirm with **Save** again.<br><br>
    ![](/exercises/ex3/images/Screenshot-2-07.png)<br><br>
8.  To review the impact on the data footprint, go to **Related Apps** > **Digital Blueprint Overview**.<br><br>
    ![](/exercises/ex3/images/Screenshot-2-08.png)<br><br>
9.  The overview shows that, in combination with the **Org Slice**, a significant amount of the overall data (typically between **30%** and **50%**) has been excluded from the migration scope.<br><br>
    ![](/exercises/ex3/images/Screenshot-2-09.png)<br><br>
10.  Use the **Back** button in the Launchpad to return to the blueprint.<br><br>
11.  **Congratulations!** You have successfully completed this sub-exercise.<br><br><br>

## Exercise 3.3 - Select Scanned Tables
<p align="justify">After finalizing the transformation object scope, you will now complete the scoping by confirming the scanned tables. These tables were automatically identified by the system scan and typically include customer-specific (Z / Y) or third-party tables.</p>

### Steps:
Follow these steps to complete the exercise:<br>
1.  Within your blueprint, open the **Transition Readiness** tab [1] and choose **Select Scanned Tables** [2].<br><br>
    ![](/exercises/ex3/images/Screenshot-4-01.png)<br>

2.  Scroll down and select the tables **ZMSKA** or **ZMSSA** from the list [1]. Then choose **Mass Edit** [2].<br><br>
    ![](/exercises/ex3/images/Screenshot-4-02.png)<br>

3.  These tables are **legacy custom tables** whose functionality has been replaced in **SAP S/4HANA**. Since they are no longer required, you will remove them from scope.<br><br>
    For **Scope**, select **Out of Scope** and, in **Comment for all objects**, optionally enter a note, for example: **Exclude ZMSKA and ZMSSA from the scope, as their functionality is replaced in the target system**. Finally, choose **Save**.<br><br>
    ![](/exercises/ex3/images/Screenshot-4-03.png)<br>

4.  Next, select **all scoping-relevant tables** from the list [1] and choose again **Mass Edit** [2].<br><br>
    ![](/exercises/ex3/images/Screenshot-4-04.png)<br>

5.  Change the **Status** to **Confirmed** and choose **Save**.<br><br>
    ![](/exercises/ex3/images/Screenshot-4-05.png)<br>

6.  The **Status** of all scoping-relevant tables changes from **Open** to **Confirmed**, indicating that all relevant objects have been reviewed and validated.<br><br>
    ![](/exercises/ex3/images/Screenshot-4-06.png)<br>

7.  Use the **Back** button in the Launchpad to return to the blueprint.<br><br>
8.  The **Set status for scanned tables** warning has disappeared from the list.<br><br>
    ![](/exercises/ex3/images/Screenshot-4-07.png)<br>

9.  **Congratulations!** You have successfully completed this sub-exercise.<br><br><br> 


## Summary
<p align="justify">You have now successfully completed the the first scoping step on your <b>Digital Blueprint</b>. By defining the organizational scope through company code selection, applying a time-based reduction with the Time Slice pattern and refining scanned tables, you have reduced the overall data footprint while keeping all relevant business information intact. In the next two exercises we will now look into the Value Mappings for the Chart of Accounts solution pattern.</p>

Continue to - [Exercise 4 - Chart of Accounts Mapping: Manage Value Mappings](../ex4/README.md)
