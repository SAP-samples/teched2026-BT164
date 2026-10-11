# Exercise 7 - Scope the Blueprint: Select & Reduce Data - Part 2/2
<p align="justify">In this exercise, you will define the data scope of your digital blueprint by excluding irrelevant company codes, limiting historical data, and filtering transformation objects. These scoping activities help to reduce system size and complexity before the transformation model is created.</p>

This exercise consists of the following sub-exercises:
- [Exercise 7.1 - Activate CoA Solution Pattern](#exercise-71---activate-coa-solution-pattern)
- [Exercise 7.2 - Select Transformation Objects](#exercise-72---select-transformation-objects)
- [Exercise 7.3 - Confirm Digital Blueprint](#exercise-73---confirm-digital-blueprint)

<br>

## Exercise 7.1 - Activate CoA Solution Pattern
<p align="justify">In this sub-exercise, you will activate the CoA solution pattern for your digital blueprint.</p>

### Steps:
Follow these steps to complete the exercise:<br>
1. Bla
2. Bla
3. Bla

10. **Congratulations!** You have successfully completed this sub-exercise.<br><br><br>


## Exercise 7.2 - Select Transformation Objects
<p align="justify">After successfully applying both the organizational and time-based reductions, you will now refine your blueprint further by narrowing the scope of <b>transformation objects</b>. This step focuses on excluding objects without relevant data, ensuring that only necessary business data is considered for migration.</p>

### Steps:
Follow these steps to complete the exercise:<br>
1.  Within your blueprint, click on the **Solution Patterns** tab and click on **Chart of Accounts**.<br><br>
2.  Click on the **Edit** button in the top right hand corner to make your digital blueprint editable. This will allow you to activate the CoA solution pattern.<br><br>
3.  In the status drop-down, change the value fom **Inactive** to **Active**.<br><br>
4.  On the bottom right hand side of your screen, click on the button **Apply**. The solution pattern is now active. <br><br>
5.  Confirm your decision bu clicking on the button **Save**.<br><br>
6. **Congratulations!** You have successfully completed this sub-exercise.<br><br><br>  


## Exercise 7.3 - Confirm Digital Blueprint
<p align="justify">After completing the organizational, time, and object scoping, you will now finalize and confirm your digital blueprint. Before confirming, you will review the remaining information and warning messages.</p>

### Steps:
Follow these steps to complete the exercise:<br>
1.  Within your blueprint, select **SAP HCM data identified** from the **Transition Readiness** list.<br><br>
    ![](/exercises/ex7/images/Screenshot-5-01.png)<br><br>
2.  The system indicates that **SAP Human Capital Management** (HCM) data has been identified and must be migrated outside of **SAP Business Transformation Center**.<br><br>
    This is expected and can be safely ignored for this exercise.<br><br>
    ![](/exercises/ex7/images/Screenshot-5-02.png)<br><br>
3.  Use the **Back** button in the Launchpad to return to the blueprint.<br><br>
4.  Next, select the **SAP S/4HANA Industry Solution-related data detected** warning from the list.<br><br>
    ![](/exercises/ex7/images/Screenshot-5-03.png)<br><br>
5.  The warning informs you that data related to **SAP Industry Solutions** (except IS-H* if applicable) will be technically transferred from SAP ECC to SAP S/4HANA as-is, without transformation.<br><br>
    Since these objects are handled outside **SAP Business Transformation Center**, you can also ignore this message.<br><br>
    ![](/exercises/ex7/images/Screenshot-5-04.png)<br><br>
6.  Use the **Back** button in the Launchpad to return to the blueprint.<br><br>
7.  Choose **Confirm Digital Blueprint**.<br><br>
    ![](/exercises/ex7/images/Screenshot-5-05.png)<br><br>
8.  In the confirmation dialog, review the settings and choose **Confirm** to finalize your blueprint.<br><br>
    ![](/exercises/ex7/images/Screenshot-5-06.png)<br><br>
9.  The **Status** of the **Digital Blueprint** has changed from **Open** to **Confirmed**, indicating that your blueprint is now locked for scoping and ready for modeling.<br><br>
    ![](/exercises/ex7/images/Screenshot-5-07.png)<br><br>
10. **Congratulations!** You have successfully completed this sub-exercise.<br><br><br>  


## Summary
<p align="justify">You have now successfully completed the end-to-end scoping of your <b>Digital Blueprint</b>. By defining the organizational scope through company code selection, applying a time-based reduction with the Time Slice pattern, and refining both transformation objects and scanned tables, you have reduced the overall data footprint while keeping all relevant business information intact. By activating the Chart of Accounts Solution Pattern you have additionally enabled the harmonization of the Charts of Accounts as specified by the Mapping Model from the previous exercise. After reviewing system messages and confirming the blueprint, you now have a fully scoped and validated data foundation, optimized in size, complexity, and relevance, ready for transformation modeling in the next exercise.</p>

Continue to - [Exercise 8 - Build the Model: Create Transformation Model & Version](../ex8/README.md)
