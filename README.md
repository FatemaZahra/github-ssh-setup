## Link to Markdown file
[Markdown Documentation techniques](https://github.com/FatemaZahra/markdown_documentation_techniques)


# What is Git and Github
## Git
Git is a free, high-quality distributed version control system suitable for tracking modifications in source code in software development. It was originally created as an open-source system for coordinating tasks among programmers, but today it is widely used to track changes in any set of files. 

## GitHub
- It is a web-based Git repository. This hosting service has cloud-based storage. 
- GitHub offers all distributed version control and source code management functionality of Git while adding its own features. 
- It makes it easier to collaborate using Git. 
- GitHub lets the users work together on projects.

## Git Set-up with SSH and HTTPS

### HTTPS setup
**Step 1:** Go to github.com and login.
Note: If you do not have an account, create a new account using a valid email address.

**Step 2:** Click on the profile icon --> Go to "Your repositories" --> Create a new repository by clicking on "New" --> Add a repository name --> Set it to "Public" --> Click on. "Create repository"

When you reach the quick setup page, select HTTPS as shown in the image.

![Screenshot 2022-07-29 at 16 28 46](https://user-images.githubusercontent.com/102330725/181793201-39e80194-a3a5-4042-85a4-d3d234529064.png)

Follow the commands to create new repository on command line
```
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin "your https link here"
git push -u origin main
``` 
_Note: To clone repository using HTTPS, Go to "Code" on the repo page --> select HTTPS and copy the link. Paste the following command with the link on terminal_

`git clone "your link"`

![Screenshot 2022-07-29 at 16 41 34](https://user-images.githubusercontent.com/102330725/181795892-6679836a-6379-473e-af07-b6c55a97cccb.png)

### SSH Setup

**Step 1:** Open terminal

**Step 2:** Type in the following code to check if ssh folder exists
```
$ cd ~/.ssh
```

_Note: If the folder doesn't exist make folder by typing in:_
```
$ mkdir .ssh
```

**Step 3:** Paste the text substituting in your Github email address:
```
$ ssh-keygen -t ed25519 -C "your_email@example.com"
```

**Step 4:** Enter file name to save the key in

**Step 5:** Enter password or leave empty if no password is needed, do the same to confirm password

_Note: The key's randomart image is generated. To check if files exists use_
```
ls
```
You should see the file name and a **.pub file**

**Step 6:** Paste the command on the terminal, replace the filename with your file where the key is saved and then copy the SSH key received.
```
cat filename.pub
```

**Step 7:** Go to GitHub --> Settings --> SHS and GPG keys --> New SSH Key --> Paste the SSH Key copied from the terminal --> add a title --> click 'Add SSH key'

**Step 8:** Add your SSH private key to the ssh-agent and store your passphrase in the keychain. Paste the command in terminal and replace filename with the name of the file where key is avavilable.
```
ssh-add -K ~/.ssh/filename
```
_Note: We do not need to use .pub_

**Step 9:** Create a new repository on github and follow the steps to init, add, commit and push after selecting **SSH** on the quick setup page.
![Screenshot 2022-07-29 at 16 37 10](https://user-images.githubusercontent.com/102330725/181794575-17aef9b4-943b-43da-a2b7-3596bacb7a89.png)

```
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin "your ssh link here"
git push -u origin main
``` 

