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

_Running `git` commands to commit:_
* I wrote a simple method in MarkdownParse.java to show a simple change in the code.
![image](https://user-images.githubusercontent.com/103149284/167491069-b6182fc0-b2ec-4962-8be6-b012d852789a.png)
* Originally, I had trouble pushing the changes I made from my remote, however I needed to make sure I properly setup the repository I want to change with the command: `git remote set-url origin <ssh link>`
* I needed to do git pull (before I made changes on the remote account) to get other changes and then do `git push origin main` (The success that the java file changed is the message below after `git push origin main`).
* ![image](https://user-images.githubusercontent.com/103149284/167491222-39faf8e9-6497-451a-85ed-90a63bf40907.png)


_Link to show commit:_


**Copying whole directories with `scp -r`:**
