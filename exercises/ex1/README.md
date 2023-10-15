# Exercise 1 - Generating a stack XML using Maintenance Planner

In this exercise, we will create a maintenance plan for planning a conversion of an SAP ERP system to SAP S/4HANA 2022 - Feature Package Stack 2.

## Exercise 1.1 Login to Maintenance Planner

After completing these steps you will have logged into maintenance planner for generation of stack XML.

1. Ctrl+Click <a href="https://maintenanceplanner.cfapps.eu10.hana.ondemand.com/" target="_blank">here</a> to open maintenance planner in a new tab.

2. Enter the user details provided by speakers to login to the maintenance planner.

3. You should be able to see the following home page after logging in:
   <br>![](/exercises/ex1/images/mp_027.png)

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

2. <b> Select Files: Select OS/DB dependent files </b>

   In this step, you can select additional software required for the conversion. This includes:

   - SAP Kernel and related components like SAP IGS.
   - Software Logistic tools like Software Update Manager
   - SAP Host Agent
   - SAP HANA Database and Client revision

   Click on the expand arrow to see the list of selectable software.

   > <i>![Select OS/DB files](/exercises/ex1/images/mp_010.png)</i>

   Select the required checkbox to select the child entities, as shown below.

   > <i>![Select OS/DB files](/exercises/ex1/images/mp_011.png)</i>

   Click on "Confirm Selection".

   A warning pop-up comes up to outline the dependencies between SAP Kernel and SAP IGS. In the case of this hands-on session, this can be ignored and you may click on "Continue" to calculate the delta packages.

   > <i>![Select OS/DB files](/exercises/ex1/images/mp_012.png)</i>

3. <b> Select Files: Select Stack Dependent and Independent files </b>

   This step is meant to present the list of all the calculated delta packages which are required by Software Logistic tools to implement. This delta includes:

   - Add-on installation packages, if there are any for the planned target.
   - Support-Packages of the selected target.
   - Add-on exchange upgrade packages, if there are any relevant for the target.
   - Attribute Change Packages (ACPs), if there are any required for this plan.
   - Files for non-ABAP components like SAP Kernel, SAP IGS, Software Logistic tools, SAP Kernel hotfix patches like R3Trans.
   - Installation or Upgrade archives (including languages) for SAP S/4HANA product versions.

   You may explore these in this step by collapsing/expanding the relevant tree nodes.

   > <i>![Select Stack files](/exercises/ex1/images/mp_013.png)</i>

   > <i>![Select Stack files](/exercises/ex1/images/mp_014.png)</i>

   You may want to include additional HR packages into the plan, for which you can use the "Add HR Packages" button.

   > <i>![Select Stack files](/exercises/ex1/images/mp_015.png)</i>

   This opens a pop-up with the list of additional HR packages which get included in the plan as per your selections.

   > <i>![Select Stack files](/exercises/ex1/images/mp_016.png)</i>

   Click on Next to continue to Download Files step.

   > <i>![Select Stack files](/exercises/ex1/images/mp_017.png)</i>

4. <b> Download Files </b>

   In this step, you see the list of all the files which have been collected by maintenance planner for the plan to be implemented. In addition, you can download stack XML, push the archives to download basket and also download additional files for traceability.

   > <i>![Download Stack XML](/exercises/ex1/images/mp_018.png)</i>

   Stack XML file contents:

   > <i>![Stack XML](/exercises/ex1/images/mp_019.png)</i>

   > <i>![Push to Download Basket](/exercises/ex1/images/mp_020.png)</i>

   Download plan PDF:

   > <i>![Download plan PDF](/exercises/ex1/images/mp_021.png)</i>

   > <i>![View plan PDF](/exercises/ex1/images/mp_022.png)</i>

   Export planned files metadata into an excel:

   > <i>![Export to Microsoft Excel](/exercises/ex1/images/mp_023.png)</i>

   View contents:

   > <i>![View contents](/exercises/ex1/images/mp_024.png)</i>

   Click on Next to go to Complete step.

   > <i>![Next](/exercises/ex1/images/mp_025.png)</i>

5. <b> Complete </b>

   In this step, you can save the plan and see the contents of the plan PDF. Click on the home icon to go to the home page of maintenance planner.

   > <i>![Save plan](/exercises/ex1/images/mp_026.png)</i>

   > <i>![Home page](/exercises/ex1/images/mp_027.png)</i>

## Summary

You've now been able to generate a stack XML which can be used by Software Update Manager for converting the system. In this hands-on workshop, execution of Software Update Manager is not in scope.

Continue to - [Exercise 2 - Exercise 2 Description](../ex2/README.md)
