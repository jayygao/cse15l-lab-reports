## Find Commands

1. ```find DIRECTORY -iname FILE```

     i. ```$ find 911report -iname "Chapter*.txt"```
     
     Output :
     ```
       911report/chapter-1.txt
       911report/chapter-10.txt
       911report/chapter-11.txt
       911report/chapter-12.txt
       911report/chapter-13.1.txt
       911report/chapter-13.2.txt
       911report/chapter-13.3.txt
       911report/chapter-13.4.txt
       911report/chapter-13.5.txt
       911report/chapter-2.txt
       911report/chapter-3.txt
       911report/chapter-5.txt
       911report/chapter-6.txt
       911report/chapter-7.txt
       911report/chapter-8.txt ```
       
    ii. ```$ find government/About_LSC -iname "legal*.txt"```
    
    Output : 
    ```
    government/About_LSC/LegalServCorp_v_VelazquezDissent.txt
    government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt
    government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt```
    
    Importance? The importance of the ```-iname``` option is that instead of the ```-name``` command
    
    which is case sensitive, ```-iname``` finds the files all with the same characters regardless of upper
    
    or lower case.
