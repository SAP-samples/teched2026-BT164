# Exercise 1 - Build the Foundation: Upload UDP File
<p align="justify">In this exercise, you will extract the key analysis file from the source SAP ERP 6.0 system – the <b>Usage and Data Profiling</b> (UDP) file – and upload it to SAP Cloud ALM. This file serves as the technical and functional input for the <b>Digital Blueprint</b> application.</p><br>

**ℹ️ NOTE**

In this hands-on session, you will actually **not** follow the steps outlined below to log on to the ABAP system, execute the Readiness Check Report, etc... Instead, the analysis file is already provided for you to download from within this repository. You can find it at the link below. Please download this file and continue directly with **step 6** in this guide. <br>

📦 [**Download RC_UDP_DMR2_BDS_300.zip**](https://github.com/SAP-samples/teched2026-BT164/raw/main/resources/files/RC_UDP_DMR2_BDS_300.zip)

You may of course take a look at the next steps 1 - 5, which describe what needs to be done in case you have access to an ECC ABAP Source System. <br>



## Steps:
Follow these steps to complete the exercise:<br>
1.  Log on to the **BDS** system in SAP GUI, client **300**, using the user **btc-0XX** (replace *XX* with your seat number, for example **btc-001**), and open transaction **SE38** (ABAP Editor).<br>

2.  In the **Program** field, enter **RC_UDP_START_DMR2** [1] and choose **Execute** (F8) [2].<br><br>
    ![](/exercises/ex1/images/Screenshot-01.png)<br>

3.  Choose **Download DRM2 Analysis Data** and save the ZIP file to your local disk.<br><br>
    ![](/exercises/ex1/images/Screenshot-02.png)<br>

4.  Switch to [SAP Cloud ALM](https://calm-deep-dive-workshop.us10.alm.cloud.sap) and log in with the user **btc-0XX** (replace *XX* with your seat number, for example **btc-001**).<br>

    > **💡 TIP**: To open this link in a new tab, **right-click** and choose **Open Link in New Tab**.

5.  Navigate to **Transformation** [1] &gt; **Manage Analysis File** [2].<br><br>
    ![](/exercises/ex1/images/Screenshot-05.png)<br>

6.  In the **Manage Analysis File** application, choose **Create**.<br><br>
    ![](/exercises/ex1/images/Screenshot-06.png)<br>

7.  Enter **UDP_BT164_XX** (replace *XX* with your seat number, for example **UDP_BT164_01**) as the **Name**, and keep the default **Analysis Type** (SAP Readiness Check for SAP ERP usage and data profiling).<br><br>
    ![](/exercises/ex1/images/Screenshot-07.png)<br>

8. Upload the ZIP file you downloaded in Step 3 (or from this repo) and choose **Create**.<br><br>
    ![](/exercises/ex1/images/Screenshot-08.png)<br>

9. Verify that the analysis file has been successfully uploaded.<br><br>
    ![](/exercises/ex1/images/Screenshot-09.png)<br>


10. **Congratulations!** You have successfully completed this exercise.<br><br><br>



## Summary
<p align="justify">You have now extracted the <b>Usage and Data Profiling</b> (UDP) analysis file from the source SAP ERP 6.0 system and uploaded it to the <b>Manage Analysis File</b> app in <b>SAP Cloud ALM</b>. This builds the foundation for analyzing your current system.</p>

<p align="justify">For this hands-on session we will skip the Exercise 2 - Finding the Transition Approach - and will jump right to the next exercise - Exercise 3 - <b>Creating the digitial blueprint</b>.</p>

Continue to - [Exercise 2 - Initialize Project: Create Digital Blueprint](../ex2/README.md)