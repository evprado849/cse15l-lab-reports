**Installing VS Code:**

![image](https://user-images.githubusercontent.com/103149284/162326911-96750d4a-fac7-4714-9f0a-29eb302e6ea0.png)

* VSCode is an IDE for various programming languages such
as Java, Python, and alike.
* To install VSCode, go to this link: https://code.visualstudio.com/
and make sure the environment is setup for Java (if you use Java) in
both your computer and on VSCode.
* As said by others: _Start Early, Start Often!_

**Remotely Connecting:**


* In this class, we learn techniques/basics about
connecting remotely to a server.
* To connect to a remote server (for this class) open
VSCode and the terminal and type the following: (Don't type the $)

`$ ssh cs15lsp22zzz@ieng6.ucsd.edu `
* zzz in cs15lsp22zzz@ieng6 is your own login to connect to the server.

![image](https://user-images.githubusercontent.com/103149284/162327999-fb8d2976-1190-4024-a071-de27a8d3f8ae.png)

**Trying Some Commands:**

`$ ls -lat`

* Lists all the files that is in that directory

`$ ls -a`

* Lists all the files that is in that directory (However, hidden files are not seen)

![image](https://user-images.githubusercontent.com/103149284/162606395-671060c9-c5d9-4d39-801e-163c0a2f146c.png)


`$ scp desiredFileName.filetype cs15lsp22zz@ieng6.ucsd.edu:~/`

* Transfers a secure copy of a file to the server (your login)

![image](https://user-images.githubusercontent.com/103149284/162606560-36e8c62d-7b7f-48f8-999c-a496685e7159.png)

![image](https://user-images.githubusercontent.com/103149284/162606569-244876a5-a456-4112-8727-5a68a6db7182.png)

**SSH Key:**

* Using an SSH Key can save us time to log into the server without needing a password.

* It can be setup via terminal on VSCode or on CMD Line with the code: `ssh-keygen`

![image](https://user-images.githubusercontent.com/103149284/162667604-71db0c0e-9020-42c6-aa26-c19c2e160eb6.png)


**Optimizing Remote Running:**

* When working in between our local machine and the server, we want to do some commands that can help
us know and use various files.

`$ ssh cs15lsp22zz@ieng6.ucsd.edu "ls"` - Lists the home directory on the remote server

![image](https://user-images.githubusercontent.com/103149284/162666123-fb5cb405-3285-4e09-9255-123c07e7ddfd.png)

* Using semicolons can allow us to run multiple commands (depending on some terminals)


