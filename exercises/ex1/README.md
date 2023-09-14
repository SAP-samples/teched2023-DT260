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

1. <b> Plan for SAP S/4HANA tile </b>

   Click on Plan for SAP S/4HANA tile.

   > <i>![](/exercises/ex1/images/mp_001.png)</i>

2. <b> Overview </b>

   Click on the option "Manual Conversion" under "Convert Existing SAP ERP System to SAP S/4HANA System". Read the contents briefly to understand the pre-requisites, tools and steps involved in the system conversion process. Click on "Next" once done.

   > <i>![](/exercises/ex1/images/mp_002.png)</i>

3. <b> Backend System </b>

   Enter the system ID "S2Y[ABAP]" in the value help. From the filtered set of values, select "S2Y[ABAP]".

   > <i>![](/exercises/ex1/images/mp_003.png)</i>

   On selecting the same, thecurrent SAP ERP product version present on the system shows up in the "Current Version" field. Make the selections as shown in the screenshot below for "Target Version", "Target Stack". The "Target Product Instances" will be pre-selected.

   > <i>![Target selections](/exercises/ex1/images/mp_004.png)</i>

   Below is a small description of the fields:

   1. <i>Target Version</i>: The target SAP S/4HANA version
   2. <i>Target Stack</i>: The Feature Package Stack or Support Package Stack of the target version.
   3. <i>Target Product Instances</i>: Core and additional business functionality of the target stack you want to include in the SAP S/4HANA system.

   Keep the selections as is, and click on "Next".

4. <b> Additional Systems </b>

   In this step, one can select the Frontend server for deploying the SAP Fiori for SAP S/4HANA software, and the Java adapters for SAP S/4HANA.

   SAP Fiori can be deployed in your system landscape on an existing frontend server, new frontend server, or together with SAP S/4HANA backend. These options are provided by maintenance planner as shown in the screenshot below.

   > <i>![SAP Fiori](/exercises/ex1/images/mp_005.png)</i>

   In this hands-on exercise, focus is on planning an embedded deployment of SAP Fiori software. Do the below selections in the maintenance planner and click on Next button.

   > <i>![SAP Fiori selections](/exercises/ex1/images/mp_006.png)</i>

5. <b> Summary </b>

   In this step, you can see the results of the Add-ons and business functions for SAP S/4HANA system conversion planning. The results summarize the following in general:

   - SAP add-ons in the system which are incompatible with the target SAP S/4HANA version (including the ones which can be uninstalled during conversion).
   - Third party add-ons which need to be checked up with the vendor about their compatibility with target SAP S/4HANA version.
   - Activated Business Functions compatibility against the target SAP S/4HANA version
   - Software-component-versions which are not assigned to any SAP product-versions as per the SAP product model.
   - Links to related documentation.

   Once you have gone through the details in this step, click on "Continue Planning" to move to the next guided procedure used for generating the stack XML.

   > <i>![SAP S/4HANA add-ons and business function check summary](/exercises/ex1/images/mp_007.png)</i>

   In case there are any warnings, then you will get an additional confirmation step as follows. Click on Continue:

   > <i>![Warning](/exercises/ex1/images/mp_008.png)</i>

## Exercise 1.3 Generate stack XML using the planning guided procedure

1. <b> Define Change </b>

   On clicking "Continue Planning" in the previous guided procedure of Exercise 1.2, you will land into the "Define Change" step. Notice that the plan-id is the same as the previous guided procedure.

   The target will have been applied based on the SAP product model, and the selections done in the previous steps. Review the selections and click on "Next" to continue.

   > <i>![Define Change](/exercises/ex1/images/mp_009.png)</i>

2.

## Summary

You've now been able to generate a stack XML which can be used by Software Update Manager for converting the system. In this hands-on workshop, execution of Software Update Manager is not in scope.

Continue to - [Exercise 2 - Exercise 2 Description](../ex2/README.md)
