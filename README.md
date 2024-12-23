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

- Find a process running on a specific port (you need to install the tools like netstat)


- Decode a base64 encoded message

## 1. Find a hidden file

Use the `ls -a` command. This command lists all files in a directory, including hidden ones. Hidden files typically start with a period (`.`), such as `.git`.

![finding hidden files](https://github.com/user-attachments/assets/1b03dc83-6781-4daf-ad3f-f2ad435116d6)

## 2. Locate a file with "secret" in its name

 Use the `find ./ -name "*secret*"` command. The `*` is a wildcard, meaning it will search for any file with "secret" in its name, anywhere in the directory.

![Screenshot 2024-12-23 122637](https://github.com/user-attachments/assets/a838091c-a99c-4be4-83f3-f9f81d35bceb)


## 3. Find the largest file in a specific directory


