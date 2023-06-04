# Lab Report 5

## Part 1

Student Post:

![Image](https://i.gyazo.com/768466e77fef155be37d832e93ad5eb8.png)
![Image](https://i.gyazo.com/a4de293e91b264a6e836ef0d8fd432ad.png)

TA Response:

![Image](https://i.gyazo.com/0c102603d81e000407824060fa5236a5.png)

Student Reponse:

![Image](https://i.gyazo.com/f74845d68172e2ae41d7e4611dab4eac.png)
![Image](https://i.gyazo.com/86f8d908ccfaaa6b35e3c2dbed616838.png)
![Image](https://i.gyazo.com/feee518e2ef9162161591ffc5f20fed1.png)

TA Reponse:

![Image](https://i.gyazo.com/59a1f3894c16007fe6de1952980342cb.png)

Student Reponse:

![Image](https://i.gyazo.com/bdd045676832e0fe0daa45f811f1ddc9.png)

## End of Part 1
- The file and directory needed was from week 7 of lab, which had ListExamples.java, ListExamplesTests.java, test.sh, and the jUnit files.

- The contents of each file

Test.sh
![Image](https://i.gyazo.com/cbdf5cc39a9519a9ccb3b483613d6e9e.png)

ListExamplesTests.java
![Image](https://i.gyazo.com/c39434f7c385b5f73e0fd58290fad987.png)

ListExamples.java
![Image](https://i.gyazo.com/feee518e2ef9162161591ffc5f20fed1.png)

- Command line I used to trigger bug
`bash test.sh`

- Description of what I used to fix the bug.

I changed the command in test.sh from a Mac user command to a Window users command.

```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```

Then in ListExamples.java, I changed the variable that was being incremented from index1 to index2. 

![Image](https://i.gyazo.com/8660729b67020cae3cb16561389bed16.png)

## Part 2

In my lab experience I found it cool how I can edit files through vim on a server, through <h><j><k><l> to move around in a file and edit it. However I also learned how specific we need to be in our lab reports, to the smallest detail or we would get points docked off. It was also irritating how some times I get points marked off on my lab reports for something the TA said I didn't do, even though I did. It's as if sometimes the things I write on the Lab Report don't exist and they just read over it, causing me to lose points and resubmit the lab report all ovet again.
