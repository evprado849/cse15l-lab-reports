**Lab Report 5**

[My Repository](https://github.com/evprado849/markdown-parser)

[Given Repository](https://github.com/nidhidhamnani/markdown-parser)


_Using vimdiff for differences:_
* I see how different my implmentations for my MarkdownParse vs the given Repository. It's very different from the given Repository because I remember how in the last Report, my implementation was buggy.
* After running the scripts for both my own repository and on the given repository, I recall that on the given repository, I got successful [] (brackets] for those that don't have a link/contents, however, for those that did have cotnents within them, it contained links (i.e: [https://something.com], just an example).
* However, my implementation was buggy because I kept getting an out of bounds exception for several of them, so after seeing how after running the scripts and seeing the differences are of my repo and the given one, I'll try to debug it so that some (or most tests) can pass.
![image](https://user-images.githubusercontent.com/103149284/171511747-b327c214-e6df-4ef9-b900-8567301b755f.png)

File Differences (Files used) from given Repository:
* [test-Files/500.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/500.md)
* [test-Files/516.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/516.md)

CommonMark for 500:

![image](https://user-images.githubusercontent.com/103149284/172223047-eb30ccc0-986b-4ca3-ae8b-413acc9adbc0.png)

CommonMark for 516:

![image](https://user-images.githubusercontent.com/103149284/172223150-56d0e01b-8638-473f-97fb-65f3c1306f3f.png)


Correct Implementations:
* The given repository is the correct implementation for both of these test files, 500 and 516.
* The reason why my repository is wrong is because I got several out of bound errors with my implementation. My implementation was only able to handle the very first test file we worked on with something.com or example.com because of the way it was implemented. However, the group's repo was able to take into account the different styles/links for the test files.
