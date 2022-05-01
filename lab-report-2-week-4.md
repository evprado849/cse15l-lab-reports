**Code Change from Github:**
* The file I changed is in the MarkdownParse.java file
* [Actual Link to See Change(s)](https://github.com/evprado849/markdown-parser/commit/dbdf3aaa81cf4ccfe618bff384f212ad78f80604)
* (To see actual changes, commit to main and push to origin)
* Red is Original, Green is Recent Changes Made
![image](https://user-images.githubusercontent.com/103149284/164958755-e470fdde-907a-4db7-9aea-a72fee109dff.png)

**Test File Failures and Relationships:**
* [Information Came From Here](https://blog.regehr.org/archives/199)
* Bug: A flaw in computer system that could have some symptoms.
* Symptom: Faulty behavior that you can see 
* Failure-Inducing Input: Input from user that causes bugs and symptoms to show.

**Relationship with Bug, Symptom, and Failure Input in MarkdownParse.java:**
* Failure-inducing Input: If the user was to input this README.md file, it will cause a failure.
* Bug: When the program takes the user input on command line, it doesn't have any content for getLinks to be called upon:
![image](https://user-images.githubusercontent.com/103149284/166155310-117eaf5d-94a9-4ba3-96f6-6957b3921acb.png)

* Symptom: The bug causes the out of bound error message.


_Running with README.md file: (A crash/error shown)_
![image](https://user-images.githubusercontent.com/103149284/166155186-d1cfd068-41a1-4139-ad02-aad6cef6a647.png)


_Running other files: (No apprent crash)_
![image](https://user-images.githubusercontent.com/103149284/166155206-19c4c660-24ee-4963-b840-7ebcbf470e3b.png)



**Fixing the failures:**
* e
