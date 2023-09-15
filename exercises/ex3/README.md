# Exercise 3 - Identify critical SAP Notes recommendation for your SAP S/4HANA systems

In this exercise, you will identify critical SAP Notes recommendation for your SAP S/4HANA systems.

## Exercise 3.1 Login to Maintenance Planner

After completing these steps you will have logged into maintenance planner to view recommended SAP notes for your SAP S/4HANA systems.

1. Ctrl+Click <a href="https://maintenanceplanner.cfapps.eu10.hana.ondemand.com" target="_blank">here</a> to open maintenance planner in a new tab.

2. Enter the user details provided by speakers to login to the maintenance planner.

3. You should be able to see the following home page after logging in:

   > <i>![](/exercises/ex1/images/mp_027.png)</i>

## Exercise 3.2 Identify critical SAP Notes recommendation

After completing these steps you will have identifed with critical SAP Notes recommendation for your SAP S/4HANA systems.

Continue as described below.

1. <b> View Recommended Notes tile </b>

   Click on "View Recommended Notes" tile.

   > <i>![](/exercises/ex3/images/mp_301.png)</i>

2. <b> Select S/4HANA systems </b>

   In this step, you can filter and select S/4HANA systems for identifying critical SAP Notes recommendation.
   
   1. Click on "Filter" icon to filter the S/4HANA systems

      > <i>![](/exercises/ex3/images/mp_302.png)</i>

   2. Select filer as "Product".

      > <i>![](/exercises/ex3/images/mp_303.png)</i>

   3. Select the product "SAP S/4HANA". Click on "OK" to apply the filter.

      > <i>![](/exercises/ex3/images/mp_304.png)</i>
      
      You can explore other filter options to filter of list of systems.


3. <b> Calculate Notes </b>

   In this step, you can identify critical SAP Notes recommendation

   1. Select S/4HANA system: "S4Z" and click on "Calculate Notes".

      > <i>![](/exercises/ex3/images/mp_305.png)</i>

         On clicking "Calculate Notes", recommeded SAP Notes for the selected S/4HANA systems are calculated and displayed. It consists of the following:
         - Customized recommendations for individual systems based on your system landscape and SAP Notes metadata.
         - Recommended notes include Security Notes, Hot News, Performance Notes, Legal Changes, etc.

   2. Filter the recommended notes.
         
      you can see all the recommended SAP notes with their total count for the selected systems. To filter the recommended notes, use the following quick filters:
      - <i>SAP Security Notes</i>: Displays notes that are of the highest priority.

         > <i>![](/exercises/ex3/images/mp_306.png)</i>

      - <i>Hot News</i>: Displays notes that are of the highest priority.
      - <i>PerformanceNotes </i>: Displays notes that are critical for your systems performance.
      - <i>Legal Change Notes</i>: Displays notes relevant for any legal changes required for your systems.

   3. View SAP Note details.
         
      Select a note to view the note details in following tabs:
      - <i> About </i>: Displays the system and note details.
      - <i> Logs </i>: Displays all the actions performed on the note with the user ID, processing status, date, time, and comments.

      > <i>![](/exercises/ex3/images/mp_307.png)</i>

      For SAP Security Notes, details like CVSS Score and Vector, and CVE are also displayed.

   4. Use search and filter options   
      
      The toolbar consists of the following options:
      - Search - Search for a note from the list using its name or number.
      - Filter - Filter the notes list based on the displayed columns.
      - Reset Filter - Remove all the applied filters to view all the available notes in the list.
      - Sort - Sort the list in ascending or descending order.
      - Group - Group the notes together in ascending or descending order or based on the displayed columns.
      - Settings - Choose the columns that you want to see on the screen accordingly.
      - Export to Excel - Download and save the filtered list of notes in an excel file format.
      - Edit Processing Status - Change the processing status of the selected notes.

4. <b> Change processing status of notes </b>

      In this step, you can can change the processing status of the notes based on your requirement.
      
      1. Click the "Edit" icon displayed in the Processing Status column for which you want to change the status.
      2. Enter the following details:
         Select Status: Select the appropriate status for the note from the drop-down list.
         - <i>Transferring</i>: Note is transferred for implementation.
         - <i>In Progress</i>: Note implementation is in progress.
         - <i>On Hold</i>: Note is yet to be decided if it needs to be implemented or is irrelevant.
         - <i>Not Relevant</i>: Invalid or irrelevant note for your system.
      3. Comments: Enter comments 
      4. Click "Save" to update the processing status.

      > <i>![](/exercises/ex3/images/mp_308.png)</i>


5. <b> Download recommended SAP notes </b>

      In this step, you can can download the filtered list of SAP notes in an excel file format.
      
      1. Click the "Download" icon displayed toolbar.
      2. Click the "Excel" icon.
         This will download the file on the system's download folder.

         > <i>![](/exercises/ex3/images/mp_309.png)</i>

## Summary

You've now completed the exercise by identifing critical SAP Notes recommendation for your SAP S/4HANA systems.

<i> Note </i>: You need to have 'Security Contact' authorization to get security notes recommedation.

