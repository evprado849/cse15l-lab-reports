**Lab Report 4**


* [My implemention (repository) of MarkdownParse](https://github.com/evprado849/markdown-parser)
* [Implemention of MarkdownParse from Group (Group repository)](https://github.com/UDXS/markdown-parser)

_Snippet1.md:_
Expected From CommonMark.js for Snippet1.md:
![image](https://user-images.githubusercontent.com/103149284/170853034-54d2876a-4b57-4ce4-b121-abe6988b0018.png)

* My Implementation (Repository) of MarkdownParseTest.java: 
How I could fix my implementation:
In my implementation, I got a Heap error, and it occured on line 25. I could fix this by changing a line of code, that could state after `int openBracket = markdown.indexOf("[", currentIndex);`, to skip over it. For instance, after that line of code, we could state something like `if [`
![image](https://user-images.githubusercontent.com/103149284/169954390-9e7edb1e-32f6-472f-9a18-1dae841ab09a.png)
* Group's (Repository) of MarkdownParseTest.java:
![image](https://user-images.githubusercontent.com/103149284/169955958-46314323-e855-4dae-9790-18beac03a3bf.png)
How our group could fix the implementation:
In my group's implementation, the expected JUnit failed because it expected url.com but rather went to ucsd.edu. From what I see, it completely skipped over url.com and went straight to the end, ucsd.edu because of some of the brackets which was included between the tick marks. The way I think our group can fix this, is include a code that finds an instance of a open and closed tickmark. For example, maybe our group can put something like: `int tickMark = markdown.indexOf("`", tickMarkIndex);`. Although its not perfect, I think if our group found a way to use something like that approach, it can help get the link.




_Snippet2.md:_
Expected From CommonMark.js for Snippet2.md:
![image](https://user-images.githubusercontent.com/103149284/170853077-1ef60e4f-a61c-45f2-a483-7ffa27ab6945.png)

* My Implementation (Repository) of MarkdownParseTest.java:
![image](https://user-images.githubusercontent.com/103149284/170422191-abefa2b0-4b16-4470-a8b3-020bc6e57412.png)
How I could fix my implementation:
Similarly to snippet1.md for my implementation, I got a Heap error in my MarkdownParse.java while iterating through snippet2.md contents.
* Group's (Repository) of MarkdownParseTest.java:
![image](https://user-images.githubusercontent.com/103149284/170422460-ff23cf91-0ca5-4cd8-9977-af6612944331.png)
How our group could fix the implementation:
For snippet2.md at least, I see that it expected b.com, but instead was a.com. From what I see, our group could fix this (for this specific snippet file at least), that if there is a second `[`, to write some code like `int duplicateBracketOpen = markdown.indexOf("["); int duplicateBracketClosed = markdown.indexOf("]");` then after that code runs, to get whatever code we got in between the duplicates and have it included when we get the actual closing bracket (`int closeBracket = markdown.indexOf("]", openBracket);`). This way, we could get the expected b.com for this specific test.


_Snippet3.md:_
Expected From CommonMark.js for Snippet3.md:
![image](https://user-images.githubusercontent.com/103149284/170853097-754372dd-8fa6-4b6f-864f-66b0790d10ba.png)

* My Implementation (Repository) of MarkdownParseTest.java: 
![image](https://user-images.githubusercontent.com/103149284/170423077-66308729-4eff-4f95-b2ad-c928a5cf200e.png)

How I could fix my implementation:
For testing the snippet files, including snippet3.md file

* Group's (Repository) of MarkdownParseTest.java:
![image](https://user-images.githubusercontent.com/103149284/170423177-64a09730-69a8-42c1-b164-d525c928f16f.png)
How our group could fix the implementation:
The group's implementation failed snippet3 because it expected `https://www.twitter.com` link, however it got end of array instead. From what I see, I got this because the first link had a line break. The way I believe our group could fix this is writing a code like if there is a line break, continue onto the next line. This way, we don't get to end of array for the actual link. From there, if we reach the end of the array without finding the closed bracket with `int closeBracket = markdown.indexOf("]", openBracket);`, then continue to look for it in the next line.

