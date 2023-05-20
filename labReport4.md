# Lab Report 4

## Forking

I forked the repository 

[Lab 7 Repository](https://github.com/ucsd-cse15l-s23/lab7)

and got my ssh clone command

`git@github.com:jayygao/lab7.git`

now I can proceed with logging onto ieng6.

## ieng6
First I logged in with copying 

`ssh cs15lsp23ea@ieng6.ucsd.edu <enter>`

and pasting with 

`<Ctrl> <Shift> <V> <enter>`

because '<Ctrl> <V>' wouldn't work in ssh command line.

Logged in with ieng6, then I git cloned my fork onto ieng6 with the command

`git clone git@github.com:jayygao/lab7.git <enter>'

after the clone was finished, I went into the directory of my repository with the command 

`cd lab7 <enter> `

Here, to run the tests I used the test.sh bash file to make things quicker, the command was

`bash test.sh <enter>`

within test.sh was the commands 

`
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests  
`

I was then returned with the error 

`
JUnit version 4.13.2
..E
Time: 0.543
There was 1 failure:
1) testMerge2(ListExamplesTests)
org.junit.runners.model.TestTimedOutException: test timed out after 500 milliseconds
        at ListExamples.merge(ListExamples.java:44)
        at ListExamplesTests.testMerge2(ListExamplesTests.java:19)

FAILURES!!!
Tests run: 2,  Failures: 1
`

Knowing what the error was, I went into ListExamples.java to fix the error, the command was...

`vim ListExamples.java <enter>`

In here, I used the keys `<h> <j> <k> <l>` to navigate around.

Which was `<left> <left> <left> <left> <left> <left>` and `dw <enter>` to delete the "index1"

I then clicked i to insert "index2" and `<esc>` to return to normal mode, then `:wq <enter>` to save 

![Image](https://i.ibb.co/bg7VQSv/Screenshot-2023-05-18-095232.png)

my changes and return back to the lab7 directory.

Here, I ran the test.sh bashg file again to run the tests to ensure there were no errors.

`bash test.sh <enter>`

and I was returned with the test results

`
JUnit version 4.13.2
..
Time: 0.016

OK (2 tests)
`

![Image](https://i.ibb.co/hCVNXbY/Screenshot-2023-05-18-095158.png)
        
Indicating my tests had passed, here I then added the files I changed to commit with git.

`git add ListExamples.java <enter>`

Now I can commit the changes.

`git commit -m "Fixed Index" <enter>`

Finally I pushed the changes onto GitHub

`git push <enter>`

I was returned with...

`
Warning: Permanently added the ECDSA host key for IP address '140.82.114.3' to the list of known hosts.    
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (1/1), done.
Writing objects: 100% (3/3), 304 bytes | 304.00 KiB/s, done.
Total 3 (delta 2), reused 2 (delta 2), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:jayygao/lab7.git
   c258751..7f996d4  main -> main
`
![Image](https://i.ibb.co/kqznrrK/Screenshot-2023-05-18-095137.png)
        
Now I'm finally done! That's the end of this lab report.

### Final Time from Timer: 01:53:07.
