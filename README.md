# Linux-command-with-LTC

Getting started with cloud environments or switching to the field means learning Linux commands to manage files and systems effectively. I’ll test my Linux skills for this challenge, but first, I need to set up the learning environment.

Instead of manually creating an instance on AWS through the console, I’ll use **Terraform**. It’s a tool that lets me automate the setup process, making things faster and easier.

To get started, I need:

1. **Terraform** (version 1.9.0 or later).
   
2. **AWS CLI** (optional since I’m using my Ubuntu terminal for this).

Once everything is set up, I’ll start the challenges!

![Getting started](https://github.com/user-attachments/assets/24a9e217-dd93-4489-80e5-f9f3a39e09bd)

## Challenges

- Find a hidden file
  
- Locate a file with "secret" in its name

- Find the largest file in a specific directory

- Identify a user with a specific UID

- Locate a file with specific permissions



### 1. Find a hidden file

Use the `ls -a` command. This command lists all files in a directory, including hidden ones. Hidden files typically start with a period (`.`), such as `.git`.

![finding hidden files](https://github.com/user-attachments/assets/1b03dc83-6781-4daf-ad3f-f2ad435116d6)

### 2. Locate a file with "secret" in its name

 Use the `find ./ -name "*secret*"` command. The `*` is a wildcard, meaning it will search for any file with "secret" in its name, anywhere in the directory.

![Screenshot 2024-12-23 122637](https://github.com/user-attachments/assets/a838091c-a99c-4be4-83f3-f9f81d35bceb)


## 3. Find the largest file in a specific directory

Use the `du -ah ./ | sort -rh | head -n 1` command.

![Screenshot 2024-12-23 194457](https://github.com/user-attachments/assets/cf311cf0-a7e1-48ca-a46a-964143317086)

### 4. Identify a user with a specific UID
For this challenge, I need to find the user ID (UID) first. To do this, I use the command:  

```bash
cat /etc/passwd
```  

This command displays a list of all users on the system. Scroll through the output to find the user and their UID.  

Once you have the UID, use the following command to find the user details:  

```bash
grep ":<UID>:" /etc/passwd
```  

Replace `<UID>` with the actual user ID you found.

### 5. Locate a file with specific permissions
Use the `find` command 
But first: use the command `ls -l` to find the file permission

![Screenshot 2024-12-23 202658](https://github.com/user-attachments/assets/8be7a218-7e2f-46a8-9080-606b455d1481)

To find a file with specific permissions, type:  
```bash
find ./ -type f -name "very_secret_file.txt" -perm 644
```  
Change `"very_secret_file.txt"` to your file's name and `644` to the permissions you want. If the file is not in the current folder, add the correct path to where the file is.

Output

![Screenshot 2024-12-23 203256](https://github.com/user-attachments/assets/59518b62-2f5d-4d70-a613-82accbeff5d9)

## Purpose

I know these are just basic Linux commands, but for me this knowledge check, reading theory doesn’t work like that. I learn better by doing. 


Thank You 4 reading 



