![image](https://github.com/user-attachments/assets/246b8806-e167-4536-b8ce-27ac798979de)



<h1>Linux File Permissions</h1>

Examine the permissions on every file in the directory—including hidden ones—to ensure they meet the required authorization levels, and adjust any permissions that do not comply. Permissions are assigned to three categories: user, group, and others. In the `chmod` command, `u` specifies settings for the file owner, `g` for the group, and `o` for all other users. None of the files should allow the other users to write to files.


<h2>Objective</h2>

Update the file permissions for designated files and directories within the `projects` directory so that they accurately reflect the required authorization levels:
  - <b>Verify</b> user and group permissions for all files in the `projects` directory.
  - <b>Identify</b> and correct any files with improper permissions.
  - <b>Inspect</b> the permissions for the `/home/researcher2/projects/drafts` directory and remove any unauthorized access.

<h3>Check file and directory details. (Verify)</h3>

Navigate to the `projects` directory and list the contents and permissions of the directory. 
  
</p>

![image](https://github.com/user-attachments/assets/4831cc2b-4b0c-435f-9f59-eb4ed6905bb8)



Using command `ls -l` the output reveals one directory named `drafts`, one hidden file called `.project_x.txt`, and five additional project files. The first 10 characters in each line designate the permissions for the file or directory, divided among the user, group, and others.

<h3>Permission String Explained</h3>

  - <b>File Type (1st Character):</b>
    - `d` indicates the item is a directory.
    - `-` indicates a regular file.

  - <b>User (Owner) Permissions (Characters 2-4):</b>
    - `r` means the user has read permission.
    - `w` means the user has write permission.
    - `x` means the user has execute permission.
    - `-` indicates that the permission is not granted to the user.

  - <b>Group Permissions (Characters 5-7):</b>
    - `r` means the group has read permission.
    - `w` means the group has write permission.
    - `x` means the group has execute permission.
    - `-` indicates that the permission is not granted to the group.

  - <b>'Other' Users Permissions (Characters 8-10):</b>
    - `r` means other users have read permission.
    - `w` means other users have write permission.
    - `x` means other users have execute permission.
    - `-` indicates that the permission is not granted to users outside the owner and group.

<h3>Change File Permissions. (Identify)</h3>

  - None of the files should allow the 'other' users to write to files. The project_k.txt file has write permissions for other users. 
</li>
    <p>
    </p>
    
![image](https://github.com/user-attachments/assets/ee74fc1d-b4e4-47cf-b800-0e6a0d04ce17)
  <p>
  </p>
  
Using the `chmod` command, I removed the write permission from other. I then input command `ls -l` to verify the modification.</li>

![image](https://github.com/user-attachments/assets/5758babd-1010-44bb-bc21-fffe9434c19b)
<p>
  

</p>


  - The file `project_m.txt` is restricted and should allow only the user to read and write it, with no read or write permissions for the group or others.

![image](https://github.com/user-attachments/assets/ff4027d4-cc90-4f60-bbd5-ac3086a98c9b)

Using command `ls -l` I list the current directory’s contents and permissions to see if the group has read and write permissions. The group has read only permission for `project_m.txt`.

![image](https://github.com/user-attachments/assets/d4858f1d-c156-4606-87fd-91ae7098ae79)

Using the `chmod` command, I removed the read permission for the group on `project_m.txt`.

<h3>Change File Permissions on a Hidden File. (Inspect)</h3>

  - Examine the hidden file `.project_x.txt` to verify if its permissions are set correctly, and adjust them if necessary. This archived file must be read-only for both the user and group, ensuring it cannot be written to by anyone.


![Screenshot 2025-03-25 123855](https://github.com/user-attachments/assets/ba4237e5-6bc4-4335-8490-4fcb5bd3066b)

The user and group owner types have incorrect write permissions. I'll change the permissions of the file `.project_x.txt` so that both the user and the group can read, but not write to the file.

![Screenshot 2025-03-25 124834](https://github.com/user-attachments/assets/028db062-c13b-4837-ac63-fd40f9fb9a46)

I use the `chmod` command to execute this change.

<h3>Change Directory Permissions</h3>

  - I will check the group permissions for the `/home/researcher2/projects/drafts` directory while I'm in the projects directory, then make any necessary changes. Only the researcher2 user should have access and execute privileges for the drafts directory and its contents.

![Screenshot 2025-03-25 125718](https://github.com/user-attachments/assets/0f3254e0-84ef-4e94-b249-ed157f3d4d92)

The group has execute permissions and therefore has access to the drafts directory. I'll remove the execute permission for the group from the drafts directory.


![Screenshot 2025-03-25 125950](https://github.com/user-attachments/assets/3e44cbe0-4d1a-44ff-9aa6-ff6a33d3ea1c)


I again used the `chmod` to remove group permission for the draft directory.

<h1>Conclusion</h1>

Using Linux commands I configured authorizations and examined the permissions then adjust the ownership of a files and directory to limit access appropriately.






