## Find Commands

1. ```find DIRECTORY -iname FILE```

     Option ```-delete```. Usage explained under examples.
     
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
       911report/chapter-8.txt 
   ```
       
    ii. ```$ find government/About_LSC -iname "legal*.txt"```
    
    Output : 
    ```
    government/About_LSC/LegalServCorp_v_VelazquezDissent.txt
    government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt
    government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt
    ```
    
    **Importance?** The importance of the ```-iname``` option is that instead of the ```-name``` command
    
    which is case sensitive, ```-iname``` finds the files all with the same characters regardless of upper
    
    or lower case.

2. ```$ find DIRECTORY -size +SIZE```

     Option ```-size```. Usage explained under examples.

     i. ```$ find 911report -size +100k```
     
     Output : 
     ```
     911report/chapter-1.txt
     911report/chapter-12.txt
     911report/chapter-13.2.txt
     911report/chapter-13.3.txt
     911report/chapter-13.4.txt
     911report/chapter-13.5.txt
     911report/chapter-3.txt
     911report/chapter-6.txt
     911report/chapter-7.txt
     911report/chapter-9.txt
     ```
     
     ii. ```$ find government/About_LSC -size +200k```
     
     Output :
     ```
     government/About_LSC/commission_report.txt
     ```
     
     **Importance?** The importance of the ```-size``` option is that it helps the user filter and find files based on 
     
     on the files size, for megabytes it's +(Value)M, kilobytes it's +(Value)k.
     
3. ```$ find DIRECTORY -name "FILE" -delete```
     
     Option ```-delete```. Usage explained under examples.

      i. ```$ find 911report -name "preface.txt" -delete``` & ```$ ls 911report```
     
     Output :
     ```
        chapter-1.txt   chapter-13.1.txt  chapter-13.5.txt  chapter-6.txt
        chapter-10.txt  chapter-13.2.txt  chapter-2.txt     chapter-7.txt
        chapter-11.txt  chapter-13.3.txt  chapter-3.txt     chapter-8.txt
        chapter-12.txt  chapter-13.4.txt  chapter-5.txt     chapter-9.txt
     ```
     
     ii. ```$ find government/Env_Prot_Agen -name "final.txt" -delete``` & ```$ ls government/Env_Prot_Agen```
     
     Output : 
     ```
        1-3_meth_901.txt  ctm4-10.txt              section-by-section_summary.txt
        atx1-6.txt        jeffordslieberm.txt      tech_adden.txt
        bill.txt          multi102902.txt          tech_sectiong.txt
        ctf1-6.txt        nov1.txt
        ctf7-10.txt       ro_clear_skies_book.txt
     ```
     
     
     
     **Importance?** ```-delete``` finds the files that fit your critera, and deletes them from the directory. It has 
     
     no output however it makes it easier to filter and delete things from the command line rather than opening the folder 
     
     going through the directories.
     
4. ```find DIRECTORY  -mtime -VALUE```
     i. ```$ find 911report -mtime -1```
     
     Output : 
     ```
     911report
     911report/preface.txt
     ```
     
     ii. ```$ find government -mtime -1
     
     Output : 
     ```
     government
     government/Env_Prot_Agen
     government/Env_Prot_Agen/final.txt
     ```
     
     **Importance?** The importance of the ```-mtime``` command option is that it finds the files that has been most 
     
     recently edited in a certain amount of days by the user, such as ```-mtime -7``` shows the files that has been 
     
     edited within a 7 day time period. 
     
## Works Cited

All these command options were given to me by [ChatGPT](https://chat.openai.com/), I provided the AI with the prompt 

" find 4 interesting command-line options or alternate ways to use the command 'find' "

And I was provided with these 4 command options for ```-find```.

```
Here are four interesting command-line options or alternate ways to use the find command:
     
    1. -iname: This option performs a case-insensitive search for a file or directory by name. For example, find /home/user        -iname "file.txt" will find all files named file.txt, regardless of capitalization, in the /home/user directory and         its subdirectories.
    2. -mtime: This option searches for files that were modified a certain number of days ago. For example, find /home/user
       -mtime -7 will find all files in the /home/user directory and its subdirectories that were modified within the last         7 days.
    3. -size: This option searches for files based on their size. You can use it to find files that are larger or smaller          than a certain size. For example, find /home/user -size +10M will find all files in the /home/user directory and its        subdirectories that are larger than 10 megabytes.
    4. -delete: This option allows you to delete files that match the search criteria directly from the find command. For           example, find /home/user -name "*.bak" -delete will find all files in the /home/user directory and its          
        subdirectories that end in .bak and delete them. Note that this option can be dangerous, as it will delete files
        without prompting for confirmation.
```

The only thing I changed was the size option which ChatGPT searched by megabytes, while I searched by kilobytes. As well as 

mtime option where I searched within 1 day instead of 7 days.
     
 
   
