# Exercise 1 - Generating a stack XML using Maintenance Planner

In this exercise, we will create a maintenance plan for planning a conversion of an SAP ERP system to SAP S/4HANA 2022 - Feature Package Stack 2.

## Exercise 1.1 Login to Maintenance Planner

After completing these steps you will have logged into maintenance planner for generation of stack XML.

1. Ctrl+Click <a href="https://maintenanceplanner.cfapps.eu10.hana.ondemand.com/" target="_blank">here</a> to open maintenance planner in a new tab.

2. Enter the user details provided by speakers to login to the maintenance planner.

3. You should be able to see the following home page after logging in:
   > <i>![](/exercises/ex1/images/mp_027.png)</i>

## Exercise 1.2 Plan for SAP S/4HANA conversion

After completing these steps you will have generated the stack XML for the system conversion.

Continue as described below.

1. Click on the "Plan for SAP S/4HANA" tile.

   > <i>![](/exercises/ex1/images/mp_001.png)</i>

2. Click on the option "Manual Conversion" under "Convert Existing SAP ERP System to SAP S/4HANA System". Read the contents briefly to understand the pre-requisites, tools and steps involved in the system conversion process. Click on "Next" once done.

   > <i>![](/exercises/ex1/images/mp_002.png)</i>

3. Enter the system ID "S2Y[ABAP]" in the value help. From the filtered set of values, select "S2Y[ABAP]".

   > <i>![](/exercises/ex1/images/mp_003.png)</i>

4. On selecting the same, thecurrent SAP ERP product version present on the system shows up in the "Current Version" field. Make the selections as shown in the screenshot below for "Target Version", "Target Stack". The "Target Product Instances" will be pre-selected. Keep the selections as is, and click on "Next".

   > <i>![Target selections](/exercises/ex1/images/mp_004.png)</i>

   Below is a small description of the fields:

   1. <i>Target Version</i>: The target SAP S/4HANA version
   2. <i>Target Stack</i>: The Feature Package Stack or Support Package Stack of the target version.
   3. <i>Target Product Instances</i>: Core and additional business functionality of the target stack you want to include in the SAP S/4HANA system.

## Summary

You've now ...

Continue to - [Exercise 2 - Exercise 2 Description](../ex2/README.md)
