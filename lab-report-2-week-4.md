**Code Change from Github:**
* The file I changed is in the MarkdownParse.java file
* [Actual Link to See Change(s) for MarkdownParse.java](https://github.com/evprado849/markdown-parser/commit/dbdf3aaa81cf4ccfe618bff384f212ad78f80604)
* [Actual Link to See Change(s) for MarkdownParseTest.java](https://github.com/evprado849/markdown-parser/commit/8f38fa8d1a7ff8a979b786b7e226816bedeac47f)
* (To see actual changes, commit to main and push to origin)
* Red is Original, Green is Recent Changes Made
![image](https://user-images.githubusercontent.com/103149284/164958755-e470fdde-907a-4db7-9aea-a72fee109dff.png)

**Test File Failures and Relationships:**
* [Information Came From Here](https://blog.regehr.org/archives/199)
* Bug: A flaw in computer system that could have some symptoms.
* Symptom: Faulty behavior that you can see 
* Failure-Inducing Input: Input from user that causes bugs and symptoms to show.

**Relationship with Bug, Symptom, and Failure Input in MarkdownParse.java & MarkdownParseTest.java:**
* Failure-inducing Input: If the user was to input this README.md file, it will cause a failure.
* Bug: When the program takes the user input on command line, it doesn't have any content for getLinks to be called upon:
![image](https://user-images.githubusercontent.com/103149284/166155310-117eaf5d-94a9-4ba3-96f6-6957b3921acb.png)

* Symptom: The bug causes the out of bound error message.


_Running with README.md file: (A crash/error shown)_
![image](https://user-images.githubusercontent.com/103149284/166155186-d1cfd068-41a1-4139-ad02-aad6cef6a647.png)


_Running other files: (No apprent crash)_
![image](https://user-images.githubusercontent.com/103149284/166155206-19c4c660-24ee-4963-b840-7ebcbf470e3b.png)

* Failure-inducing Input: In the JUnit Test, we see that the input we put in is 1 * 3, which is not equal to 4.
* Bug: A leading bug for this if we had program(s) like this is it can lead the program to have an unexpected or unwanted output.
* Symptom: Failing test, as expected and actual don't match, it can lead unexpected/unwanted outcomes for bigger programs.

Failing Test:
![image](https://user-images.githubusercontent.com/103149284/166163724-fc94c2cd-4980-4bd6-87f1-c5ff82e29364.png)



Fixed Test:

Fixed Test for JUnit to Pass:
![image](https://user-images.githubusercontent.com/103149284/166163750-ae0ce4b7-5d6b-4ea2-bf72-4732a60d13eb.png)

![image](https://user-images.githubusercontent.com/103149284/166163704-c2fcefc4-175d-46c6-b55a-2e9529929e65.png)




**Fixing the failures:**
* We could just simply fix the md file to have some content that would be used in getLinks:
![image](https://user-images.githubusercontent.com/103149284/166155413-dc353654-80e7-4a71-944e-6b915e05fecb.png)
![image](https://user-images.githubusercontent.com/103149284/166155425-442406b5-8c23-49a9-990b-7e84820bceeb.png)

* We could address a case where if there is no content, return null or 0 so there won't be an error.


