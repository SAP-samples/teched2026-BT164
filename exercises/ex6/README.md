# Exercise 6 - Chart of Accounts Mapping: Value Mapping Versions
<p align="justify">In this exercise, you will create and review mapping variant versions.

The Value Mapping Versions app allows you to create and review mapping variant versions based on a mapping variant.

The Manage Value Mappings app provides a structured, guided mapping experience that enables you to create a mapping variant, maintain value mappings and validate them to ensure correctness and completeness before the data transformation.</p>

> **ℹ️ NOTE**:  A mapping variant version is an immutable snapshot of a mapping variant. It contains all mapping objects, mapping entries, system information, and validation findings as they exist at the time of its creation. A mapping variant version serves as a reliable audit trail of the value mappings process. When there are many mapping variant versions created for a single mapping variant, the latest mapping variant version is always considered Active, and it is automatically picked up by a cycle when the mapping variant on which it is based on is associated with a transformation model.

## Steps:
Follow these steps to complete the exercise:<br>
1.  Enter the **Value Mapping Versions** app.<br><br>
    ![](/exercises/ex6/images/Screenshot-01.png)
    <br>

2.  Once the **Value Mapping Versions** application opens, start maintaining a Mapping Variant Version. Enter a **Title** and select the **Mapping Variant** you have just created. The **Systems** information is being fetched automatically. Once done you can hit the **Create** button. <br>
<br><br>
    ![](/exercises/ex6/images/Screenshot-02.png)
    <br>

3.  Once being processed, you see the confirmed and created **Mapping Variant Version**, its **Status** shows **Validated with Warnings** in accordance with the prior created **Mapping Variant**.<br><br>



4.  <i>Excursus</i>: Reviewing a Mapping Variant Version<br><br>
Below the name of the mapping variant version, you can see a link to the mapping variant that the version is based on, the selected solution pattern, and the validation status.Moreover, you can also view the main details grouped in the following tabs:<br><br>
**General Information**<br><br>
In this tab, you can view the descriptive context of the mapping variant version. In the Source System Details and Target System Details subtabs, you can review the connection details of the source and target systems this version applies to.<br><br>
**G/L Accounts**<br><br>
In this tab, you can review the G/L account mapping entries captured in this version, including the chart of accounts, the old and new values, whether they were modified, and their validation status, along with the edit metadata for each entry.<br><br>
**Secondary Cost Elements**<br><br>
In this tab, you can review the secondary cost element mapping entries captured in this version, including the chart of accounts, the old and new values, whether they were modified, and their validation status, along with the edit metadata for each entry.<br><br>

![](/exercises/ex6/images/Screenshot-03.png)
    <br>

## Summary
<p align="justify">You have now successfully created a version of the Chart of Accounts Value Mappings. In the next exercise you will use this value mapping version as an input for the transformation model. But before you can do that, you have to head back to the digital blueprint, activate the CoA solution pattern, do one final scoping step and then confirm the digital bluepring so it, too, gets fixed in its current version.</p>

Continue to - [Exercise 7 - Scope the Blueprint: Select & Reduce Data - Part 2/2](../ex7/README.md)
