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
* In order to get the contents of the public key, I did `cat ~/.ssh/id_rsa.pub` in the terminal on VSCode.
* I also updated the key in my id_rsa folder with the key above (key starting with ssh-rsa).
* To add the key on Github, I went to settings, SSH Keys, and add SSH key, I didn't show my ssh-rsa here for privacy.
![image](https://user-images.githubusercontent.com/103149284/167338503-a1434304-2ede-42bb-b584-c64d783bf9ed.png)

_Private key Stored:_
* To make a new private and public key, I logged into the remote account and `ssh-keygen`.
* Some content are blocked out just for extra privacy measures, however, the private key is stored in id_rsa.
* After making new keys, they are stored in id_rsa (the private keys) and the public keys would be stored in id_rsa.pub .
![image](https://user-images.githubusercontent.com/103149284/167479729-d811d538-e860-4882-a730-b936a439dc49.png)

_Running `git` commands to commit:_

_Link to show commit:_


**Copying whole directories with `scp -r`:**
