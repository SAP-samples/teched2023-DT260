# Exercise 2 - Validate your business data using Data Transition Validation tool

In this exercise, we will create...

## Exercise 2.1 User and project setup

After completing these steps you will have logged in to the ABAP system with authorized user.

### Exercise 2.1.1 User setup
You have been assigned a user with needed authorization to execute DTV tool. Using the user provided, enter the system. 

### Exercise 2.1.2 Project setup

1. Enter transaction DTV and press enter.
<br>![](/exercises/ex2/images/User%20and%20project%20setup/dtv_001.png)

2. Enter project name as DT260_XXX_PRJ and click on change.
(Replace XXX with your user number).
<br>![Alt text](/exercises/ex2/images/User%20and%20project%20setup/dtv_002.png)

3. The project is opened with pre-defined steps to perform validation.
<br>![Alt text](/exercises/ex2/images/User%20and%20project%20setup/dtv_003.png)


## Exercise 2.2 Finalize and maintain test bed for validation

After completing these steps you will have...

### Exercise 2.2.1 Maintain systems
1. Double click on step Maintain Sytems.
<br>![](/exercises/ex2/images/Maintain%20systems/image-0.png)

2. Click on Append Row icon.
<br>![](/exercises/ex2/images/Maintain%20systems/image-1.png)

3. Enter name field as “ECC”.
<br>![](/exercises/ex2/images/Maintain%20systems/image-2.png)

4. Select system role as “Source system” from the dropdown.
<br>![](/exercises/ex2/images/Maintain%20systems/image-3.png)

5. Click on Append row icon again
<br>![](/exercises/ex2/images/Maintain%20systems/image-4.png)

6. Enter name field as “S4HANA”
<br>![](/exercises/ex2/images/Maintain%20systems/image-5.png)

7. Select System Role as “Receiver System from the dropdown.
<br>![](/exercises/ex2/images/Maintain%20systems/image-6.png)

8. Click on save
<br>![](/exercises/ex2/images/Maintain%20systems/image-7.png)


### Exercise 2.2.2 Import test from predelivered content
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
1. Click on back button and double click on Define Test Specification
<br>![](/exercises/ex2/images/Define%20test%20specification/image-0.png)

2. Double click on report name and go to split tab. 
<br>![](/exercises/ex2/images/Define%20test%20specification/image-1.png)

3. Go to Condition tab. Use the drop down to switch system and check the conditions for each system (ECC and S4).
<br>![](/exercises/ex2/images/Define%20test%20specification/image-2.png)

4. Go to variant tab.
<br>![](/exercises/ex2/images/Define%20test%20specification/image-3.png)

5. Click on save.
<br>![](/exercises/ex2/images/Define%20test%20specification/image-4.png)


### Exercise 2.2.3 Maintain project global data
1. Click on back button and double click on Project Global Data
<br>![](/exercises/ex2/images/Project%20global%20data/image-0.png)

2. Double Click on Company_Code to maintain company code values. 
<br>![](/exercises/ex2/images/Project%20global%20data/image-1.png)

3. Click on Append row in the item table
<br>![](/exercises/ex2/images/Project%20global%20data/image-2.png)

4. Select from drop down the following values:
    •	Sign – “Range limit Included”
    •	Option – “Equals”
    •	From – “1000”
<br>![](/exercises/ex2/images/Project%20global%20data/image-3.png)

4. Click on Append row button
<br>![](/exercises/ex2/images/Project%20global%20data/image-4.png)

5. Select from drop down the following values:
    •	Sign – “Range limit Included”
    •	Option – “Equals”
    •	From – “2000”
<br>![](/exercises/ex2/images/Project%20global%20data/image-5.png)

6. Click on save button.
<br>![](/exercises/ex2/images/Project%20global%20data/image-6.png)

## Exercise 2.3 Perform simulation (OPTIONAL)
...
### Exercise 2.3.1 Execute simulation
1. Click on back button and double click on Define Test Specification step.
<br>![](/exercises/ex2/images/Simulation/image-0.png)

2. Select both reports and click on Simulate button. (To select both reports, click on select all button on the alv) 
<br>![](/exercises/ex2/images/Simulation/image-1.png)

3. Click on refresh button to check the simulation status. Make sure you select both reports and click on refresh button to refresh simulation for reports at once.
<br>![](/exercises/ex2/images/Simulation/image-2.png)

4. Repeat step 4 until the Simulation status is completed (checked flag).
<br>![](/exercises/ex2/images/Simulation/image-3.png)

### Exercise 2.3.2 Check simulation results
1. Click on the Simulation result link corresponding to RFBILA00 report.
<br>![](/exercises/ex2/images/Simulation/image-4.png)

2. Check the Result.
<br>![](/exercises/ex2/images/Simulation/image-5.png)

3. Check Logs
<br>![](/exercises/ex2/images/Simulation/image-6.png)

## Exercise 2.4 Extraction in source system
...
### Exercise 2.4.1 Execute extraction
1. Click on back button and double click on Execute Data Extraction step.
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-0.png)

2. Select Financial Accounting and click on Expand Button
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-1.png)

3. Double click on RFBILA00 > ECC node. Right side of the screen is loaded showing different tabs.
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-2.png)

4. Select RFBILA00>ECC and RFDEPL00>ECC.  And click on Run Selected button. (Press Ctrl and select both nodes)
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-3.png)

5. Click on Refresh to fetch the latest status. Once the execution status is completed (green flag), check the details on the right side.
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-4.png)

### Exercise 2.4.2 Check source extraction results
1. Check Overview tab
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-5.png)

2. Click on XML Test Specification.
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-6.png)

3. Click on Worklist Items tab.
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-7.png)

4. Click on Result Data tab. It shows the actual extracted data
<br>![](/exercises/ex2/images/Extraction%20-%20Source/image-8.png)

## Exercise 2.5 Extraction in target system
...
### Exercise 2.5.1 Execute extraction
1. Login to S4 system and launch dtv.
![Alt text](image.png)

2. Enter same project name and click on display.
![Alt text](image-1.png)

3. Double click on Execute extraction step.
![Alt text](image-2.png)

4. Click on Financial accounting and expand it.
![Alt text](image-3.png)

5. Select S4HANA node of both reports and click on Run Selected.
![Alt text](image-4.png)

6. Click on refresh button until status changes to completed.
![Alt text](image-5.png)

### Exercise 2.4.2 Check source extraction results
1. Double click on RFBILA00>S4HANA. The right side of the screen is loaded.
![Alt text](image-6.png)

2. Check extraction details and results on different tabs.
![Alt text](image-7.png)


You've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
