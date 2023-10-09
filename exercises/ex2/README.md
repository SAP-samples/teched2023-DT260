# Exercise 2 - Exercise 2 Description

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

2.	Double click on Pre Delivered Content
<br>![](/exercises/ex2/images/Pre-delivered%20content/image-9.png)

3.	Expand Financial Accounting in test specification column.
4.	Go to Open Items/ Line Items->Reports and select RFDEPL00 report.
5.	Go to General ->Reports and select RFBILA00 report.
<br>![](/exercises/ex2/images/Pre-delivered%20content/image-10.png)

6.	Click on Import Specification and confirm.
<br>![](/exercises/ex2/images/Pre-delivered%20content/image-11.png)


You've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
