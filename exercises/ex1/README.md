# Exercise 1 - Build the Foundation: Upload UDP File
<p align="justify">In this exercise, you will utilize the key analysis file from the source SAP ERP 6.0 system – the <b>Usage and Data Profiling</b> (UDP) file – and upload it to SAP Cloud ALM. This file serves as the technical and functional input for the <b>Digital Blueprint</b> application.</p><br>

Normally, in a real project-like setup, you would now log on to the SAP ERP 6.0 source system, run an APAB report to generate this analysis file and then first download this file to you local PC and in the next step upload it to Cloud ALM. However, due to resource and time constraints, we will skip these steps in this hands-on session. Instead, the file is provided for you to download directly from within this repository.<br>

If you wish to follow the full procedure at your own pace on your own system landscape you can find the detailed instructions at the end of this exercise.<br>


## Steps:
Follow these steps to complete the exercise:<br>
1.  Download the provided analysis file from the following link and save the ZIP file to your local disk.<br>

📦 [**Download RC_UDP_DMR2_BDS_300.zip**](https://github.com/SAP-samples/teched2026-BT164/raw/main/resources/files/RC_UDP_DMR2_BDS_300.zip)

2.  Switch to [SAP Cloud ALM](https://calm-deep-dive-workshop.us10.alm.cloud.sap) and log in with the user **btc-0XX** (replace *XX* with your seat number, for example **btc-001**).<br>

    > **💡 TIP**: To open this link in a new tab, **right-click** and choose **Open Link in New Tab**.

3.  Navigate to **Transformation** [1] &gt; **Manage Analysis File** [2].<br><br>
    ![](/exercises/ex1/images/Screenshot-05.png)<br>

4.  In the **Manage Analysis File** application, choose **Create**.<br><br>
    ![](/exercises/ex1/images/Screenshot-06.png)<br>

5.  Enter **UDP_BT164_XX** (replace *XX* with your seat number, for example **UDP_BT164_01**) as the **Name**, and keep the default **Analysis Type** (SAP Readiness Check for SAP ERP usage and data profiling).<br><br>
    ![](/exercises/ex1/images/Screenshot-07.png)<br>

6. Upload the ZIP file you downloaded in Step 3 (or from this repo) and choose **Create**.<br><br>
    ![](/exercises/ex1/images/Screenshot-08.png)<br>

7. Verify that the analysis file has been successfully uploaded.<br><br>
    ![](/exercises/ex1/images/Screenshot-09.png)<br>


8. **Congratulations!** You have successfully completed this exercise.<br><br><br>


## Summary
<p align="justify">You have now downloaded the <b>Usage and Data Profiling</b> (UDP) analysis file and uploaded it to the <b>Manage Analysis File</b> app in <b>SAP Cloud ALM</b>. This builds the foundation for analyzing your current system.</p>

Continue to - [Exercise 2 - Initialize Project: Create Digital Blueprint](../ex2/README.md)

<br><br><br>

## Add-On Exercise: Create the UDP file yourself

In case you want to perform the activity on the SAP ERP 6.0 source system, please find here the steps that would have to be performed to obtain the UDP analysis file directly yourself from the ABAP system.

## Steps:
A.  Log on to the source system in SAP GUI and open transaction **SE38** (ABAP Editor).<br>

B.  In the **Program** field, enter **RC_UDP_START_DMR2** [1] and choose **Execute** (F8) [2].<br><br>
    ![](/exercises/ex1/images/Screenshot-01.png)<br>

C.  Choose **Download DRM2 Analysis Data** and save the ZIP file to your local disk.<br><br>
    ![](/exercises/ex1/images/Screenshot-02.png)<br>

Now you have retrieved the UDP analysis file directly from the ABAP Source system and you can continue with **Step 2** of the instructions presented above.<br>

