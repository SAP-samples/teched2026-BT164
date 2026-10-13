# Exercise 6 - Build the Model: Create Transformation Model & Version
<p align="justify">In this exercise, you will create the transformation model and its version, the technical foundation that defines how your scoped data will be processed during execution in the upcoming cycle. The transformation model translates the scope defined in the digital blueprint into technical definitions and rules that fully describe the transformation initiative.</p><br>

<p align="justify">As one step of the transformation model creation you will also assign the CoA Value Mapping Version that was created in the previous exercise.</p><br>


## Steps:
Follow these steps to complete the exercise:<br>
1.  From the launch page of the Transformation Applications within Cloud ALM scroll down to the section **Selective Data Transition: Model Your Transformation** and select the tile **Manage Transformation Models**. <br>

    ![](/exercises/ex6/images/Screenshot-01b.png)<br><br>

**ℹ️ Hint**: A quick click on the SAP Logo on the top left hand side of your Cloud ALM window will bring you back to the Cloud ALM staring page. <br><br>

2.  The **Manage Transformation Models** application opens. Select **Create** to create a new transformation model. <br>
    ![](/exercises/ex6/images/Screenshot-01c.png)<br><br>

3.  Enter **TRF_MDL_BT164_XX** (replace *XX* with your seat number, for example **TRF_MDL_BT164_01**) as **Title**. In the second input field labeled "Digital Blueprint" select the digital blueprint you created in exercise 3 (e.g. **BLUEPRINT_BT164_XX**). Lastly, in the field labeled "Mapping Variant" enter the Chart of Accounts Model Mapping Variant (e.g. **CoA_MVV_BT164_XX**) you created in the previous exerecise. <br><br>
    ![](/exercises/ex6/images/Screenshot-02b.png)<br>

4.  Leave the toggle **Client Mapping** untouched.
5.  Finally, choose **Create**.<br><br>


6.  It will take a few moments until the **Transformation Model** is successfully created.<br>

    > **ℹ️ NOTE**:  The **Transformation Model Readiness** scan is running in the background and does not require any action at this stage.

    In this view, you can see that the transformation model combines all **transformation objects**, **relations**, **filters**, and **rules** into one consistent technical definition for your transformation initiative.<br><br>
    In addition to the scoped objects defined in your **Digital Blueprint**, extra elements are automatically added to ensure consistency — including semantically related or logically grouped objects, baseline components required for technical stability, and custom objects identified through the **System Scan**.<br><br>
    ![](/exercises/ex6/images/Screenshot-03.png)<br>

7.  Choose **Transformation Objects** [1] and search for **FI Document** [2]. Then scroll down and click the **Name** of the **FI Document** [3] transformation object to navigate into it.<br><br>
    ![](/exercises/ex6/images/Screenshot-04.png)<br>

8.  The details of the **FI Document** appear. Choose **Filters**.<br><br>
    You can see that the transformation filters applied to this object are displayed - there are filters for **Org** and **Time Slice** on several tables and fields.<br><br>
    ![](/exercises/ex6/images/Screenshot-05.png)<br>

9.  Use the **Back** button to return to the transformation model overview.<br><br>
    Choose **Transformation Filters** tab [1] and then open the **Company Code Filter** [2] with the ID EccCompanyCodeFilter.<br><br>
    ![](/exercises/ex6/images/Screenshot-06.png)<br>

10.  The filter details open, showing that the value is set to company code **2000** — as scoped in your blueprint.<br><br>
    ![](/exercises/ex6/images/Screenshot-07.png)<br>

11.  Next, open the **Fiscal Year Greater Than or Equal To Filter** with the ID EccFiscalYearGreaterEquals.<br><br>
    The filter value is set to **2021**, following the Time Slice definition.<br><br>
    ![](/exercises/ex6/images/Screenshot-08.png)<br>

12. Use the **Back** button to return to the transformation model overview.<br>
13. Check that the **Source System Scan** is successful. If it is still **In Progress**, use the **Refresh** button.<br>

    > **ℹ️ NOTE**: The **Source System Scan** may take up to 5–10 minutes to complete. If you prefer not to wait, continue with **Step 14**.
    
    During the Source System Scan, a **Connectivity Check** is performed first, followed by an analysis of **customer-specific change documents**. If it detects change documents whose **object classes are not included in the SAP Business Transformation Center content**, corresponding **custom transformation objects** are generated and may require review.<br><br>
    These checks run sequentially in the background and ensure that all relevant elements are identified and considered before the actual data migration execution.<br><br>
    ![](/exercises/ex6/images/Screenshot-09.png)<br>

14. Choose the **Source System Scan** tab [1] and open **Review Custom Transformation Objects** [2].<br><br>
    ![](/exercises/ex6/images/Screenshot-10.png)<br>

15. In the **Review Custom Transformation Objects** dialog, deselect **Change Document – HOLIDAYCAL** from the list and choose **Save**.<br><br>
    This custom change document is not required for the scope of your transformation and can therefore be excluded.<br><br>
    ![](/exercises/ex6/images/Screenshot-11.png)<br>

16. The final step in this exercise is to create the immutable **Transformation Model Version**. Please note that a Model Version can only be created after the Transformation Model Readiness check completed successfully. <br><br>
    ![](/exercises/ex6/images/Screenshot-09.png)<br><br>
    If the status is still showing **In Progress**, continue with Step 20, otherwise you can continue with this step.<br><br><br>
    On the top of the screen, click the button **Create Version**<br><br>
    ![](/exercises/ex6/images/Screenshot-12.png)<br>
        
17. The **Transformation Model Version** application opens, with your transformation model already preselected.<br>
18. Enter **MDL_V1** as **Title** and choose **Create**.<br><br>
    ![](/exercises/ex6/images/Screenshot-13.png)<br>

19. After a few seconds, the **Transformation Model Version** is successfully created.<br><br>
    It represents a **snapshot** of your **transformation model** and serves as the **technical basis** for executing the **data transformation**.<br><br>
    It contains the same **objects**, **relations**, **filters**, and **rules** as defined in the model, ensuring that each transformation run is performed **consistently** and can be **traced back** to its exact configuration.<br><br>
    ![](/exercises/ex6/images/Screenshot-14.png)<br>

20. This is an alternative route to complete the exercise in case the model    creation took too long. From the menu at the top of the screen, click on the arrow to open the dropdown menu and select "Manage Transformation Models":<br><br>
   ![](/exercises/ex6/images/Screenshot-20.png)<br><br>
   Then, in the search field, enter **REFERENCE_TRAFO**, click on the magnifying lense, and select **REFERENCE_TRAFO-Model** from the list below: <br><br>
   ![](/exercises/ex6/images/Screenshot-21.png)<br><br>
   The Transformation Model application opens. Open the tab **Transformation Model Versions** and select the verion titled **REFERENCE_TRAFO-MODEL-VERSION**.<br><br>
   ![](/exercises/ex6/images/Screenshot-22.png)<br><br>
   You have now caught up with the process flow in this exercise and can contiune to the next exercise, creating the cycle from the model version.<br><br>

21. **Congratulations!** You have successfully completed this exercise.<br><br>



## Summary
<p align="justify">You have now built a transformation model and version that capture all scoped and related objects, preparing the setup for executing the transformation in the next exercise.</p>

Continue to - [Exercise 7 - Initialize Cycle: Create Cycle & Run Prevalidation](../ex7/README.md)