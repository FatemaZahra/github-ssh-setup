
# SSH Documentation

**Step 1:** Open terminal

**Step 2:** Type in the following code to check if ssh folder exists
```
$ cd ~/.ssh
```

Note: If the folder doesn't exist make folder by typing in:
```
$ mkdir .ssh
```

**Step 3:** Paste the text substituting in your Github email address:
```
$ ssh-keygen -t ed25519 -C "your_email@example.com"
```

**Step 4:** Enter file name to save the key in

**Step 5:** Enter password or leave empty if no password is needed, do the same to confirm password

Note: The key's randomart image is generated. To check if files exists use 
```
ls
```
You should see the file name and a **.pub file**


