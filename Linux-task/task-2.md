# What are files and directories?
* **File**:
A file is a container in your computer that stores data or information. This can be a text document, a photo, a video, a program, or any other kind of data. Files have names and usually extensions (like .txt, .jpg, .exe).
  
  * **Directory**:
A directory (also called a folder) is like a container that holds files and other directories. It helps organize files so they don’t get mixed up. You can think of it like a folder in a filing cabinet, where you keep papers (files) inside.

## Example:
* /home/user/Documents is a directory (folder).

* /home/user/Documents/todo.txt is a file inside that directory.

## 1. Create directory and file
```bash
mkdir /devops_workspace
touch /devops_workspace/project_notes.txt
```

## 2. Set permissions
* Owner can read & write (edit)

* Group can read only

* Others have no access
```bash
chmod 640 /devops_workspace/project_notes.txt
```
## Explanation:
6 for owner = read (4) + write (2)

4 for group = read (4)

0 for others = no permissions

## 3. Verify permissions using ls -l
```bash
ls -l /devops_workspace/project_notes.txt
```


