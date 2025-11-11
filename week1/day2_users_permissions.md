# Week 1 – Day 2: Users, Groups, and Permissions

### Key Concepts
- Linux separates file access into **User**, **Group**, and **Others**.
- Permissions are represented with `r` (read), `w` (write), and `x` (execute).
- Only the **owner** or **root** can change file permissions.
- Groups allow shared access between multiple users.
- Numeric permissions:  
  - 7 = rwx  
  - 6 = rw-  
  - 4 = r--  
  - Example: `chmod 640 file.txt` means owner can read/write, group can read, others have no access.
- Sticky bit (`chmod 1777`) prevents users from deleting each other’s files in shared directories.

### Commands Practiced

whoami
groups
sudo adduser dev1
sudo groupadd analysts
sudo usermod -aG analysts dev1
sudo chown dev1:analysts report.txt
sudo chmod 640 report.txt
sudo chmod 1777 /tmp/sharezone


### Learnings
- Got “Permission denied” until added to the correct group — real-world least privilege example.
- Understood ownership, permissions, and access hierarchy.
- Verified sticky bit protection (`drwxrwxrwt`) works.
- Learned how to cleanly shut down a VM.

