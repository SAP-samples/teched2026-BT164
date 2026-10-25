# Exercise 4 - Chart of Accounts Mapping: Manage Value Mappings

<p align="justify">In this exercise, you will define and manage the value mappings relevant for the Selective Data Transition from SAP ERP to SAP S/4HANA.

The Manage Value Mappings app provides a structured, guided mapping experience that enables you to create a mapping variant, maintain value mappings and validate them to ensure correctness and completeness before the data transformation.</p>

> **ℹ️ NOTE**:  The app can be used independently before creating a transition cycle to maintain and validate your mappings or as part of the chart of accounts solution pattern, which enables you to reorganize your charts of accounts during the SDT.

## Steps:

Follow these steps to complete the exercise:

1. Enter the **Manage Value Mapping** app.

   ![](/exercises/ex4/images/Screenshot-01.png)

2. The **Manage Value Mapping** application opens, start maintaining a Mapping Variant using the **Create** button.

   ![](/exercises/ex4/images/Screenshot-02.png)

3. Enter CoA_MV_BT164_XX (replace XX with your seat number, for example BLUEPRINT_BT164_01) as the **Title**, if you like, also enter a brief **Description** and select **BDS** as a **Source System**. The Target System can be omitted. Once done click on the **Create** button.

   ![](/exercises/ex4/images/Screenshot-03.png)

   > **ℹ️ NOTE**:  When no target system is selected, the validation will be done only on the GL acounts and cost elements of the source system (eg checking for completness of the mapping or comparing the attributes of GL accounts to be merged). This feature is especially designed in case mapping definition starts early and no target system is yet existing.

4. After the creating you automatically end up in the general view. Here you get an overview which systems you have maintained, the mapping objects overview and others.

   The **Mapping Object Overview** is still empty.

   ![](/exercises/ex4/images/Screenshot-04a.png)

   Therefore enter the **Chart of Accounts Selection** tab and select Chart of Account **0010** (which refers to Company Code 2000).

   ![](/exercises/ex4/images/Screenshot-04b.png)

   Turn the toggle button to **ON**, then read and confirm the dialog box tha pops up by selecting the option **Select Scope**.

   Now you can see that the **GL Accounts** and **Secondary Cost Elements** tabs show the fetched source system information.

   ![](/exercises/ex4/images/Screenshot-04c.png)

5. Now switch to the **GL Accounts** tab.

   ![](/exercises/ex4/images/Screenshot-04.png)

   To actually maintain a mapping, click on the **Edit** button, enter **0000111000** as a **New GL Account** for the following **Old GL Account** values:

   - **0000111000**
   - **0000113010**
   - **0000113014**

   and save your work by clicking the **Save** button at the bottom right hand side of the screen.

   The system will now mark the changed ones as **Modified** in the **Mapping Status** column. Note that the first account stays as **Original** as it acts as the leading account in this GL account merge example.

   ![](/exercises/ex4/images/Screenshot-05.png)

   > **ℹ️ NOTE**:  The fetched data always provides the full list of all accounts maintained for the selected company codes. GL accounts or secondary cost elements which are not being mapped will keep the Mapping Status **Original**.

6. Once this is done the mappings have to be validated. This needs to be done for both mapping objects, the **G/L Accounts** and the **Secondary Cost Elements**. Let's first do it for the G/L accounts, the tab you are already on. Select the **Validate** button. The system will run a validation if the merge of the three source accounts can be implemented from a business point of view.

   ![](/exercises/ex4/images/Screenshot-20.png)

   After validation, the UI may show warnings and perhaps also errors. But note, the the overal mapping status is still showing **Maintaining Mapping Values**.

   ![](/exercises/ex4/images/Screenshot-21.png)

   This is because the 2nd mapping object, the Secondary Cost Elements, has not yet been validated. This is done in the next step.

7. Switch to the **Secondary Cost Elements** tab and again click the **Validate** button. 

   ![](/exercises/ex4/images/Screenshot-22.png)

   After a while the overall status of the mapping changed from **Maintaining...** to **Validated...** and all mappings are maintained.

   > **❗BE AWARE**: Now the overall status shows **Validated with Errors**. The reason is that one of the GL accounts has an error in the mapping validation (we saw that already during the first validation), which is a showstopper and needs to be corrected. Warnings are acceptable.

   ![](/exercises/ex4/images/Screenshot-22b.png)

   We will fix that in the next step.

 8. Move back to the mapping tab of the **GL Accounts**. To view the detailed results of the validation click on the details button and expand the page. Read through the detailed analysis.
   
   ![](/exercises/ex4/images/Screenshot-23.png)

   Close the details view. If you're not yet in edit mode, click the **Edit** button and remove the mapping value for GL account **0000113014** which showed **Error** and replace it with the original source GL account value:

   **0000113014**

   Save the changes and then rerun the validation by clicking again the **Validate** button while staying on the **GL Accounts** tab where you just did the mapping correction.

   > **✅ OK**: Now the overall status shows **Validated with Warnings**, which unblocks the next step.

   ![](/exercises/ex4/images/Screenshot-25.png)

9. Congratulations! This concludes this exercise. In the next exercise we will create a variant out of this value mapping.

10. *Excursus*: To see a list of all validations you can click on the **Validation Rules** tab in the overview screen, which provides information on which fields are being considered and what the severeness and impact will be.

   ![](/exercises/ex4/images/Screenshot-08.png)

## Summary

<p align="justify">You have now successfully created the Chart of Accounts Value Mappings. In the next exercise you will create an immutable version of this definition to be used in the transformation model lateron.</p>

Continue to - [Exercise 5 - Chart of Accounts Mapping: Value Mapping Versions](../ex5/README.md)
