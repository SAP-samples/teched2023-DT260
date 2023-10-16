# Exercise 2 - Validate your business data using Data Transition Validation tool

## Before you start

The data transition validation is a tool that allows you to compare business data before and after a system conversion from SAP ECC to SAP S/4HANA. Additionally, you can perform validations during SAP S/4HANA system upgrade. Currently, the scope of the tool is to support validation of system conversion transition scenario or SAP S/4HANA upgrades. The tool uses business reports or transactions as instruments of comparison.
<br>![](/exercises/ex2/images/Introduction/image-0.png)

In the hands-on session <hands on ID>, you will get to experience the processes involved in the business data validation using DTV tool during the ECC to SAP S/4HANA conversion.  You will get experience of creating a DTV project, Maintaining Test specification, data extraction in source and target and finally performing data evaluation and obtain the comparison results.  
<br>![](/exercises/ex2/images/Introduction/image-1.png)

Login to your SAP TechEd system , and open the SAP Launchpad. Use the system named ECC Prior to conversion for the below activity of Project setup , Maintain systems , Import pre-delivered content, Maintain test specificaion and Souce Extraction.
<br>![](/exercises/ex2/images/Introduction/image-2.png)

## Exercise 2.1 User and Project setup

Create your first DTV project. 

### Exercise 2.1.1 User setup
You have already been assigned a user with needed authorization to execute DTV tool. Using the user provided, enter the system. 

### Exercise 2.1.2 Project setup

1. Enter transaction DTV and press enter.
<br>![](/exercises/ex2/images/User%20and%20project%20setup/dtv_001.png)

2. Enter project name as DT260_XXX_PRJ and click on change.
(Replace XXX with your user number).
<br>![Alt text](/exercises/ex2/images/User%20and%20project%20setup/dtv_002.png)

3. The project is opened with pre-defined steps to perform validation.
<br>![Alt text](/exercises/ex2/images/User%20and%20project%20setup/dtv_003.png)


## Exercise 2.2 Finalize and maintain test bed for validation

Maintain the tests for validation in your DTV project.

### Exercise 2.2.1 Maintain systems
In this exercise, systems are specified that shall participate in data validation. Usually, these systems are SAP ECC as source and SAP S/4HANA as target for conversion process.<br>
&#x1F4A1; Note : For SAP S/4HANA upgrade process, the source is the current release and the target is the release that you want to upgrade to.

1. Double click on step Maintain Sytems.
<br>![](/exercises/ex2/images/Maintain%20systems/image-0.png)

> <b> Maintain source system </b>

2. Click on Append Row icon.
<br>![](/exercises/ex2/images/Maintain%20systems/image-1.png)

3. Enter name field as “ECC”.
<br>![](/exercises/ex2/images/Maintain%20systems/image-2.png)

4. Select system role as “Source system” from the dropdown.
<br>![](/exercises/ex2/images/Maintain%20systems/image-3.png)

> <b> Maintain target system </b>
5. Click on Append row icon again
<br>![](/exercises/ex2/images/Maintain%20systems/image-4.png)

6. Enter name field as “S4HANA”
<br>![](/exercises/ex2/images/Maintain%20systems/image-5.png)

7. Select System Role as “Receiver System from the dropdown.
<br>![](/exercises/ex2/images/Maintain%20systems/image-6.png)

8. Click on save
<br>![](/exercises/ex2/images/Maintain%20systems/image-7.png)


### Exercise 2.2.2 Import test from predelivered content
In this exercise, you will learn to import the pre delivered set of reports from SAP to create the test specifications. You can use these test specifications later for analyzing and comparing the data during validation process.

1. Click on back button on maintain systems screen
<br>![](/exercises/ex2/images/Pre-delivered%20content/image-8.png)

2. Double click on Pre Delivered Content
<br>![](/exercises/ex2/images/Pre-delivered%20content/image-9.png)

3. Expand Financial Accounting in test specification column.
4. Go to Open Items/ Line Items->Reports and select RFDEPL00 report.
5. Go to General ->Reports and select RFBILA00 report.
<br>![](/exercises/ex2/images/Pre-delivered%20content/image-10.png)

6.	Click on Import Specification and confirm.
<br>![](/exercises/ex2/images/Pre-delivered%20content/image-11.png)


### Exercise 2.2.2 Maintain test specification
In this exercise, you will define the input parameters for each report. The input parameters are – Split, Conditions and Variant. These parameters will be considered for data extraction.

&#x1F4A1; Note: When a report is imported from pre-delivered content, the tool suggests certain split and conditions for each report. These parameters can be modified as per the scope.

1. Click on back button and double click on Define Test Specification
<br>![](/exercises/ex2/images/Define%20test%20specification/image-0.png)

> Input parameter: Split <br>
The split represents the granularity at which the data is extracted and compared. The granularity of each split is represented as Workitem and Workitem description specifies the value for it.
> <br> For Example: If the company is specified as split condition, then the results are extracted and compared at the granularity of company.
2. Double click on report name and go to split tab. 
<br>![](/exercises/ex2/images/Define%20test%20specification/image-1.png)

>Input parameter: Condition <br>
The conditions represent selection parameters which are to be passed for report execution to extract data. Multiple distinct conditions can be maintained for each system.
3. Go to Condition tab. Use the drop down to switch system and check the conditions for each system (ECC and S4).
<br>![](/exercises/ex2/images/Define%20test%20specification/image-2.png)

>Input parameter: Variant <br>
The variant represents the variant maintained for each report per system. For this project, no variant is maintained.
4. Go to variant tab.
<br>![](/exercises/ex2/images/Define%20test%20specification/image-3.png)

>Similarly, input parameters can be checked for RFDEPL00 report by double clicking on the report name

5. Click on save.
<br>![](/exercises/ex2/images/Define%20test%20specification/image-4.png)


### Exercise 2.2.3 Maintain project global data
In the previous step, we maintained split parameters for each report. In this step, we will maintain the values for each split. The Project Global Data screen allows you to capture the data, which is common across all the test specifications. By doing so, you can avoid maintaining the same data several times, for example, company, profit center, cost center, and so on. Setting up the project global data is necessary.  You can use it to define the split conditions in the test specifications.

1. Click on back button and double click on Project Global Data
<br>![](/exercises/ex2/images/Project%20global%20data/image-0.png)

2. Double Click on Company_Code to maintain company code values. 
<br>![](/exercises/ex2/images/Project%20global%20data/image-1.png)

3. Click on Append row in the item table
<br>![](/exercises/ex2/images/Project%20global%20data/image-2.png)

4. Select from drop down the following values: <br>
    •	Sign – “Range limit Included” <br>
    •	Option – “Equals” <br>
    •	From – “1000” <br>
<br>![](/exercises/ex2/images/Project%20global%20data/image-3.png)

4. Click on Append row button
<br>![](/exercises/ex2/images/Project%20global%20data/image-4.png)

5. Select from drop down the following values: <br>
    •	Sign – “Range limit Included” <br>
    •	Option – “Equals” <br>
    •	From – “2000” <br>
<br>![](/exercises/ex2/images/Project%20global%20data/image-5.png)

6. Click on save button.
<br>![](/exercises/ex2/images/Project%20global%20data/image-6.png)

## Exercise 2.3 Perform Simulation (OPTIONAL)
In the following exercise you will learn how simulate the execution of tests. Purpose of the simulation is to provide you the ability to check if the extraction of data is successful with the provided input. This is more relevant when one has to check for the memory and runtime requirements. Simulation results provide information about artifacts, such as:
<li>If the simulation was successful, then how many records were selected, and what is the memory size.
<li>If the simulation was unsuccessful, then the same is indicated by the status.
<li>In the Logs tab, the logs of the execution is shown. If the simulation is unsuccessful, the log provides appropriate message. 

<br>
&#x1F4A1; Note : In the interest of time, it is recommended to skip this Exercise and proceed with Exercise 2.4 . You may revisit this section , once the other sections are completed.

### Exercise 2.3.1 Execute simulation
1. Click on back button and double click on Define Test Specification step.
<br>![](/exercises/ex2/images/Simulation/image-0.png)

2. Select both reports and click on Simulate button. (To select both reports, click on select all button on the ALV List) 
<br>![](/exercises/ex2/images/Simulation/image-1.png)

>The execution runs in the background. The simulation status changes to in progress.
3. Click on refresh button to check the simulation status. Make sure you select both reports and click on refresh button to refresh simulation for reports at once.
<br>![](/exercises/ex2/images/Simulation/image-2.png)

4. Repeat step 4 until the Simulation status is completed (checked flag).
<br>![](/exercises/ex2/images/Simulation/image-3.png)

>The link is enabled in the Simulation Result column to check the results.

### Exercise 2.3.2 Check simulation results
1. Click on the Simulation result link corresponding to RFBILA00 report.
<br>![](/exercises/ex2/images/Simulation/image-4.png)

>The result tab shows status of simulation along with number of records and size each workitem has consumed. (Workitem: If split parameters are provided based on the inputs from the previous screen, the tool derives work items.)
2. Check the Result.
<br>![](/exercises/ex2/images/Simulation/image-5.png)

>The Logs tab shows the execution log. Also, if simulation fails, the reason can be checked in logs.
3. Check Logs
<br>![](/exercises/ex2/images/Simulation/image-6.png)

>Similarly, simulation data can be checked for RFDEPL00 report.


## Exercise 2.4 Extraction in Source system
In the following exercise you will learn how extract data in source system. The extraction screen provides a list of all the reports or transactions configured in the Project. The data for such reports can be extracted from this screen. 
The reports are shown in a tree structure with the hierarchy as Business Area >  Business Group  Type  > Report Name > System names. Extraction of reports is performed only on the leaf nodes, which are on the nodes where System IDs are present.

&#x1F4A1; Note : RFDEPLOO report has higher volumes of data and hence it might take slightly more time to finish extraction. This is exepected due to concurrent usage of systems in this hands-on kind of enviromnment. 

### Exercise 2.4.1 Execute extraction
1. Click on back button and double click on Execute Data Extraction step.
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-0.png)

2. Select Financial Accounting and click on Expand Button
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-1.png)

3. Double click on RFBILA00 > ECC node. Right side of the screen is loaded showing different tabs.
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-2.png)

4. Select RFBILA00>ECC and RFDEPL00>ECC.  And click on Run Selected button. (Press Ctrl and select both nodes)
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-3.png)

>The extraction is triggered in background. The status changes to in -progress.
5. Click on Refresh to fetch the latest status. Once the execution status is completed (green flag), check the details on the right side.
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-4.png)

### Exercise 2.4.2 Check source extraction results
>Overview Tab shows the execution details, i.e, status, runtime, number of records etc.
1. Check Overview tab
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-5.png)

>XML Test specification tab displays the test specification(split, conditions, variants) in XML format.
2. Click on XML Test Specification.
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-6.png)

>Workitems tab displays the number of records per workitem. If split parameters are provided based on the inputs from the test specification screen, the tool derives work items.
3. Click on Worklist Items tab.
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-7.png)

>Log tab shows the execution log
4. Cick on Log tab.
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-9.png)

>Result Data tab displays actual extracted data in tabular format.
4. Click on Result Data tab.
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-8.png)

## Exercise 2.5 System conversion

&#x1F4A1; The source system is now handed over for System Conversion. Once the Sytem conversion is complete the source ECC system is converted to a target SAP S/4HANA system. 
We have performed such a conversion and have provided you with a target SAP S/4HANA system. The next set of exercises are to be performed in the target system. 

1. Login to the SAP S/4HANA system
<br>![](/exercises/ex2/images/System%20Conversion/image-0.png)

## Exercise 2.6 Extraction in Target system
The extraction screen provides a list of all the reports or transactions configured in the project. The data for such reports can be extracted from this screen. The reports are shown in a tree structure with the hierarchy as Business Area >  Business Group  Type  > Report Name > System names. Extraction of reports is performed only on the leaf nodes, which are on the nodes where System IDs are present.
When extraction is performed , the reports are executed in the background and the output of the reports are saved in the tool. 
### Exercise 2.6.1 Execute extraction
1. Launch dtv.
<br>![](/exercises/ex2/images/Extraction%20-%20Target/image-0.png)

2. Enter same project name and click on display.
<br>![](/exercises/ex2/images/Extraction%20-%20Target/image-1.png)

3. Double click on Execute extraction step.
<br>![](/exercises/ex2/images/Extraction%20-%20Target/image-2.png)

4. Click on Financial accounting and expand it.
<br>![](/exercises/ex2/images/Extraction%20-%20Target/image-3.png)

5. Select S4HANA node of both reports and click on Run Selected.
<br>![](/exercises/ex2/images/Extraction%20-%20Target/image-4.png)

>The extraction runs in the background. The status changes to in-progress.

6. Click on refresh button until status changes to completed.
<br>![](/exercises/ex2/images/Extraction%20-%20Target/image-5.png)

### Exercise 2.6.2 Check source extraction results
1. Double click on RFBILA00>S4HANA. The right side of the screen is loaded.
<br>![](/exercises/ex2/images/Extraction%20-%20Target/image-6.png)

2. Check extraction details and results on different tabs.
<br>![](/exercises/ex2/images/Extraction%20-%20Target/image-7.png)

>Similarly, the extraction results for RFDEPL00 report can be checked.

## Exercise 2.7 Execute Evaluation
This screen provides the list of all the reports or transactions configured in the project. Data evaluation is performed from the result sets extracted from source and target release. Based on this result set, the tool compares the data and depicts the results in the Equals, Difference, Missing in Target, Unexpected in Target dimensions. 
The reports are shown in a tree structure with the hierarchy as Business Area > Business Group > Type > Report Name. Evaluation of the reports is performed only on the leaf nodes.

### Exercise 2.7.1 Execute evaluation
1. Go to steps screen and double click on Evaluate Data step.
<br>![](/exercises/ex2/images/Evaluation/image-0.png)

2. Click on Financial Accounting and click on expand button.
<br>![](/exercises/ex2/images/Evaluation/image-1.png)

3. Double click on RFBILA00 report. The right side of the screen is loaded with different tabs.
<br>![](/exercises/ex2/images/Evaluation/image-2.png)

4. Select both RFBILA00 and RFDEPL00 report and click on Run Selected.
<br>![](/exercises/ex2/images/Evaluation/image-3.png)

>The evaluation is triggered in the background. The status is changed to in-progress.

5. Click on refresh until the evaluation status changed to completed (green flag) 
<br>![](/exercises/ex2/images/Evaluation/image-4.png)

### Exercise 2.7.2 Check evaluation results

>The overview tab shows extraction status of both systems. Only when both systems extraction is completed, evaluation can be performed. It displays evaluation execution details.
1. Check Overview tab.
<br>![](/exercises/ex2/images/Evaluation/image-5.png)

>Worklist Items tab displays evaluation count for each workitem categorised in different dimensions.
2. Click on Worklist Items.

<br>![](/exercises/ex2/images/Evaluation/image-6.png)

>Result tab displays entire evaluated data categorised in different dimensions. Actual evaluated data can be checked by clicking on the data column.
3. Click on Result tab. Click on Equal>Data.
<br>![](/exercises/ex2/images/Evaluation/image-7.png)

4. Check the evaluation results
<br>![](/exercises/ex2/images/Evaluation/image-8.png)

>Similarly, you can check results for RFDEPL00 report by double click on the report.

## Exercise 2.8 Check Summary
In the following exercise you can check summary of the overall project and its status.

1. Double click on Summary step.
<br>![](/exercises/ex2/images/Summary/image-0.png)

2.	Check summary of entire project.
<br>![](/exercises/ex2/images/Summary/image-1.png)

You've now sucessfully performed data validation using DTV tool. 

Continue to - [Exercise 3 - Identify critical SAP Notes recommendation for your SAP S/4HANA systems](../ex3/README.md)
