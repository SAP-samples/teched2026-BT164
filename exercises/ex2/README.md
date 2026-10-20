# Exercise 2 - Initialize Project: Create Digital Blueprint
<p align="justify">In this exercise, you will create the <b>Digital Blueprint</b>, a key artifact in the data-driven transformation process. The blueprint combines input from multiple sources, such as the <b>Usage and Data Profiling</b> (UDP) analysis file and the <b>System Scan</b>, and serves as the foundation for modeling and refining the transformation scope in the following exercises.</p><br>

## Steps:
Follow these steps to complete the exercise:<br>
1.  Still within the application **Manage Analysis File** of the previous exercise, click on the button **Create Digital Blueprint**.<br><br>
    ![](/exercises/ex2/images/Screenshot-01.png)<br>

2.  Enter **BLUEPRINT_BT164_XX** (replace *XX* with your seat number, for example **BLUEPRINT_BT164_01**) as the **Name**, and confirm that your UDP **Analysis** created in the first exercise is listed (otherwise select it via the dropdown selection). Afterwards, click on the button **Create** in the lower right hand side of your screen.<br><br>
    ![](/exercises/ex2/images/Screenshot-02.png)<br>
3.  The **Digital Blueprint** has now been successfully created.<br><br>
    ![](/exercises/ex2/images/Screenshot-03.png)<br>
4.  To get an overview of its current readiness, choose **Transition Readiness** [1].<br><br>
    In this view, you can review all activities required to prepare your blueprint for data migration. It serves as a checklist that highlights any missing or incomplete steps before you can confirm and activate the blueprint.<br><br>
    There can be messages of type **Warning**, **Information** and **Error**, the latter one indicating that a **System Scan** is required but missing [2]. Let’s resolve this next.<br><br>
    ![](/exercises/ex2/images/Screenshot-04.png)<br>
5.  Select **Edit**, set **REFERENCE_SYS-SCAN** as the **System Scan**, and then choose **Save**.<br>

    > **ℹ️ NOTE**: For time-saving purposes, the system scan has already been prepared and is simply consumed in this exercise. For a system of this size (~250 GB), the scan would normally take about 15–20 minutes to complete.

    ![](/exercises/ex2/images/Screenshot-05.png)<br>
6.  The **System Scan** error has now disappeared, but two new messages appear — one indicating that the scanned tables must still be scoped, and another referencing SAP S/4HANA Industry Solution–related data. These will be addressed in the next exercise.<br><br>
    ![](/exercises/ex2/images/Screenshot-06.png)<br>
7.  To review the **System Scan** in more detail, scroll to the top of the blueprint and choose **Related Apps** [1] > **Manage System Scans** [2].<br><br>
    ![](/exercises/ex2/images/Screenshot-07.png)<br>
8.  Select **REFERENCE_SYS-SCAN** from the list.<br><br>
    ![](/exercises/ex2/images/Screenshot-08.png)<br>
9.  The **System Scan** overview opens.<br><br>
    Here, you can review information such as the **Software Component Check** (including required versions and SAP Notes), the **Connectivity Status** of the source system, and the current **Scan Status**. If prerequisites are missing or the connection is inactive, the scan cannot be executed until these issues are resolved.<br><br>
    ![](/exercises/ex2/images/Screenshot-09.png)<br>
10. Choose **Client-Dependent Tables** to explore the scan results.<br><br>
    The **System Scan** identifies additional tables not covered in the SAP delivered Transformation Object content, including customer-specific tables (Z and Y), third-party tables (such as SAP Add-Ons), and dependent standard tables. It also detects **essential system tables** that are automatically added to the transformation scope to **ensure system consistency**.<br><br>
    For each table, you can review the **number of entries**, helping you make informed decisions during the upcoming scoping phase.<br><br>
    ![](/exercises/ex2/images/Screenshot-10.png)<br>
11. Use the Launchpad back button to return to your Digital Blueprint.<br>
12. **Congratulations!** You have successfully completed this exercise.<br><br><br>


## Summary
<p align="justify">You have now created the <b>Digital Blueprint</b> and linked it to the prepared <b>System Scan</b>, establishing a solid foundation for further scoping and data-reduction activities.</p>

Continue to - [Exercise 3 - Scope the Blueprint: Select & Reduce Data](../ex3/README.md)
