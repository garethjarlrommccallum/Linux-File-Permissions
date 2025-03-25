![image](https://github.com/user-attachments/assets/246b8806-e167-4536-b8ce-27ac798979de)



<h1>Linux File Permissions</h1>


<h2>Objective</h2>

Update the file permissions for designated files and directories within the 'projects' directory so that they accurately reflect the required authorization levels, thereby enhancing overall system security.
<p>
  
</p>

<h2>Check file and directory details</h2>
The following code demonstrates how I used Linux commands to determine the existing permissions set for a specific directory in the file system. 
<p>
  
</p>

![list of all](https://github.com/user-attachments/assets/fe42665a-59b6-40d7-85ca-5da6b7602aef)


Using [ls -la]  provided a detailed view, including hidden files. The output reveals one directory named drafts, one hidden file called .project_x.txt, and five additional project files. The first 10 characters in each line designate the permissions for the file or directory, divided among the user, group, and others.

<h2>Permission String Explained</h2>

  - File Type (1st Character):
    - [ d ] indicates the item is a directory.
    - [ - ] indicates a regular file.

  - User (Owner) Permissions (Characters 2-4):
    - [ r ] means the user has read permission.
    - [ w ] means the user has write permission.
    - [ x ] means the user has execute permission.
    - [ - ] indicates that the permission is not granted to the user.

  - Group Permissions (Characters 5-7):
    - [ r ] means the group has read permission.
    - [ w ] means the group has write permission.
    - [ x ] means the group has execute permission.
    - [ - ] indicates that the permission is not granted to the group.

  - Other Users' Permissions (Characters 8-10):
    - [ r ] means other users have read permission.
    - [ w ] means other users have write permission.
    - [ x ] means other users have execute permission.
    - [ - ] indeicates that the permission is not granted to users outside the owner and group.
