# Exercise 4 - Chart of Accounts Mapping: Manage Value Mappings
<p align="justify">In this exercise, you will define and manage the value mappings relevant for the Selective Data Transition from SAP ERP to SAP S/4HANA.

The Manage Value Mappings app provides a structured, guided mapping experience that enables you to create a mapping variant, maintain value mappings and validate them to ensure correctness and completeness before the data transformation.</p>

> **ℹ️ NOTE**:  The app can be used independently before creating a transition cycle to maintain and validate your mappings or as part of the chart of accounts solution pattern, which enables you to reorganize your charts of accounts during the SDT. 

## Steps:
Follow these steps to complete the exercise:<br>
1.  Enter the **Manage Value Mapping** app.<br><br>
    ![](/exercises/ex4/images/Screenshot-01.png)
    <br>

2.  The **Manage Value Mapping** application opens, start maintaining a Mapping Variant using the **Create** button.<br>
<br><br>
    ![](/exercises/ex4/images/Screenshot-02.png)
    <br>

3.  Enter a **Title**, a brief **Description** and select **BDS_300** as a **Source System**. The Target System can be omitted. Once done hit the **Create** button.<br><br>

    ![](/exercises/ex4/images/Screenshot-03.png)<br>
    
    **ℹ️ NOTE**:  When no target system is selected, the validation will be done only on the GL acounts and cost elements of the source system (eg checking for completness of the mapping or comparing the attributes of GL accounts to be merged). This feature is especially designed in case mapping definition starts early and no target system is yet existing.<br><br>


4.  After the creating you automatically end up in the general view. Here you get an overview which systems you have maintained, the mapping objects overview and others.<br>


    The mapping object overview is still empty. Therefore enter the **Chart of Accounts Selection** tab and select Chart of Account **0010** (which refers to Company Code 2000). 
    
    Now you can see that the **GL Accounts** and **Secondary Cost Elements** tabs show the fetched source system information.<br><br>
    
    ![](/exercises/ex4/images/Screenshot-04.png)<br>


5.  Now switch to the **GL Accounts** tab. To actually maintain a mapping you can hit the **Edit** button. Enter **0000111000** as a **New GL Account** for the following **Old GL Account** values: <br><br>
**0000111000**<br>
**0000113010**<br>
**0000113014**<br><br>
The system will now mark the changed ones as **Modified** in the **Mapping Status** column. Note that the first account stays as **Original** as it acts as the leading account in this GL account merge example.<br><br>

    ![](/exercises/ex4/images/Screenshot-05.png)<br>

      **ℹ️ NOTE**:  The fetched data always provides the full list of all accounts maintained for the selected company codes. GL accounts or secondary cost elements which are not being mapped will keep the Mapping Status **Original**.<br><br> 

6. Once done hit the **Validation** button next to the mappings. The system will run a validation if the merge of the three source accounts can be implemented from a business point of view.<br><br> 

7. Now switch to the **Secondary Cost Elements** tab and again click the **Validation** button. Now all mappings are maintained!<br><br> **❗BE AWARE**: Now the overall status shows **Validated with Errors**. Reason is that one of the GL accounts shows an Error in the mapping validation, which is a showstopper. Warnings are acceptable. <br><br>

    ![](/exercises/ex4/images/Screenshot-06.png)<br><br>
    
    **ℹ️ NOTE**: To view the detailed results of the validation click on the details button and expand the page. Read through the detailed analysis<br><br>

    ![](/exercises/ex4/images/Screenshot-07.png)<br>

8.  Move back to the mapping tab of the **GL Accounts**, push the **Edit** button and remove the mapping value for GL account **0000113014** which showed **Error** and replace it with the original source GL account value: <br><br>**0000113014**<br><br>Rerun the validation by clicking again the **Validate** button while staying on the **GL Accounts** tab where you just did the mapping correction.<br><br>**✅ OK**: Now the overall status shows **Validated with Warnings**, which unblocks the next step.<br><br>
   
9.  <i>Excursus</i>: To see a list of all validations you can click on the **Validation Rules** tab in the overview screen, which provides information on which fields are being considered and what the severeness and impact will be.<br><br>

    ![](/exercises/ex4/images/Screenshot-08.png)
 

 ## Summary
<p align="justify">You have now successfully created the Chart of Accounts Value Mappings. In the next exercise you will create an immutable version of this definition to be used in the transformation model lateron.</p>

Continue to - [Exercise 5 - Chart of Accounts Mapping: Manage Value Mappings](../ex5/README.md)
