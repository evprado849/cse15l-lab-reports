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
* Failure-inducing Input: The input that will cause the failure is the user input (on line 30)
is args[0]
* Bug: The calling of args[0] in the main method is the bug that will cause the symptom (out of bounds)
There could also be apprent bugs with the file we choose for args[0] or getLinks.
* Symptom: The bug causes the out of bound error message because there is nothing to be indexed
(Message: Index 0 out of bounds for length 0)

_Running with args[0]: (A crash/error shown)__
![image](https://user-images.githubusercontent.com/103149284/166152590-60e82a33-d90d-45c0-80bc-21f5d53693aa.png)

_Running without args[0]: (No apprent crash)_
![image](https://user-images.githubusercontent.com/103149284/166154132-fe6ccd09-a151-4c3a-8654-1b301fa8fada.png)



