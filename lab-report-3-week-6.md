**Streamling ssh Configuration**

_My .ssh/config File:_
* I needed to access the config file by typing this command on the terminal: ~:/.ssh/config .
* I typed in the Host, Hostname, account, and if needed, the Identity File to access the key.
![image](https://user-images.githubusercontent.com/103149284/167310603-dc075ffb-16d3-4f9e-b645-0d4a037d402b.png)

_ssh command to login:_
* In order to login with just `ssh ieng6`, I needed to put the ssh key in the proper id_rsa file.
* I needed to get the proper key starting with ssh-rsa and put it in id_rsa and in the remote authorized_keys file (ssh-rsa was from the id_rsa.pub file).
![image](https://user-images.githubusercontent.com/103149284/167344927-6a09fc21-a731-4a82-b7ed-de9452cb7245.png)

_scp command:_
* To scp, I needed to get the path on my local computer where my id_rsa is.
* I then needed the contents from my local computer and copy that into my remote account's authorized_keys.
* The following output of the code typed in terminal shows that the copying was successful and what file contents was copied.
![image](https://user-images.githubusercontent.com/103149284/167477247-c12b6761-e266-4662-a769-51b41d71a5be.png)
 

**Setup Github Access from ieng6:**

_Location of public key:_
* I made the public key from logging into my remote account and `ssh-keygen` (Just like below for private key).
* I got the public key by going into my remote server and finding the public key on id_rsa.pub, starting with ssh-rsa.
* To add the key on Github, I went to settings, SSH Keys, and add SSH key, I didn't show my ssh-rsa here for privacy.
![image](https://user-images.githubusercontent.com/103149284/167480453-1911af09-24f4-4c7f-9525-c667504bb131.png)

_Private key Stored:_
* To make a new private and public key, I logged into the remote account and `ssh-keygen`.
* Some content are blocked out just for extra privacy measures, however, the private key is stored in id_rsa.
* After making new keys, they are stored in id_rsa (the private keys) and the public keys would be stored in id_rsa.pub .
![image](https://user-images.githubusercontent.com/103149284/167479729-d811d538-e860-4882-a730-b936a439dc49.png)

_Running `git` commands to commit on remote server:_
* I wrote a simple method in MarkdownParse.java to show a simple change in the code.
* I use the following git commands in order to show on GitHub, the changes I made on my remote to the GitHub repo:
* `git status` `git commit -m ""` `git push` All those methods were done on the terminal from the remote sever to see the changes on Github.
* [Link to show that commit successful from remote server to GitHub.](https://github.com/evprado849/markdown-parser/commit/060ad3688221f275c54318f2aada0a9b34db65f2)
![image](https://user-images.githubusercontent.com/103149284/167491069-b6182fc0-b2ec-4962-8be6-b012d852789a.png)
![image](https://user-images.githubusercontent.com/103149284/167520793-78fc09d5-7cfe-493d-80af-c0d2dabe8db7.png)
![image](https://user-images.githubusercontent.com/103149284/167520787-923e96d7-ae1b-4f3d-afd8-c83f18935c5f.png)


**Copying whole directories with `scp -r`:**

_Copying your whole markdown-parse directory to your ieng6
account:_ 
* I just got the markdown-parser repository from GitHub and downloaded the repository onto my local computer.
* I used `scp` command in order to get the repository on my local laptop onto my remote account.
* Showing a successful copy command on the terminal:
![image](https://user-images.githubusercontent.com/103149284/167501832-c4208dff-ad12-47d6-8e5b-cb1b4a08246e.png)
![image](https://user-images.githubusercontent.com/103149284/167502742-0e97858a-381a-4e9d-9723-4ce9bee543cb.png)

* Showing that the new markdown-parse repository was also copied onto my remote account:
![image](https://user-images.githubusercontent.com/103149284/167502035-a4bc8bfc-b03a-4034-917f-4316cf2322ed.png)

_Copying a repository into ieng6 and running ieng6's:_
* I first copied and pasted a repository on my local laptop with scp.
* I used ssh to access the exact repository I just copied on my account and also did the javac and java commands equivalent to run the JUnit Tests without actually logging into my account.
![image](https://user-images.githubusercontent.com/103149284/167729718-ddba3ce4-7cac-436a-a3d4-33843d766e7f.png)
