# Linux

to run linux you have to start the virtual machine.

## File permissions

- Owner / User - **U** - The Owner permissions apply only the owner of the file or directory, they will not impact the actions of other users.
- Group - **G** - The Group permissions apply only to the group that has been assigned to the file or directory, they will not effect the actions of other users.
- Others - **O** - The All Users permissions apply to all other users on the system, this is the permission group that you want to watch the most.

| Number | Permission Type          | Symbol |
|--------|--------------------------|--------|
| 0      | No Permission            | —      |
| 1      | Execute                  | –x     |
| 2      | Write                    | -w-    |
| 3      | Execute + Write          | -wx    |
| 4      | Read                     | r–     |
| 5      | Read + Execute           | r-x    |
| 6      | Read + Write             | rw-    |
| 7      | Read + Write + Execute   | rwx    |

Example:

-rw-r--r-- 1 user wheel   0 Feb 16 14:22 file2

-(rw-) (r--) (r--) 1 user wheel   0 Feb 16 14:22 file2

(**u**ser)  (**g**roup)  (**o**thers)

- The owner has read and write permissions
- The group and others only have read permissions
- This code would be 644
  
  ### chmod command

  You can use chmod to change file permissions.

  chmod <what permissions / code> <file_name>

Examples:

- $ chmod u+x file_name
- $ chmod g+rw file_name
- $ chmod o-w file_name
- $ chmod u=rwx,g=rx,o= file_name
- $ chmod 774 file_name