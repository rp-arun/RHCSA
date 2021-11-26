---
## User Types

1. **Normal Users**  - Team
2. **System Users**  - User created for services
3. **Root User**     - Super user 

Users are identified by UID

  | User | UID |
  |---|---|
  | Root | 0  |
  | System Users | 1-999  |
  | Normal Users | 1000+  |

***#useradd*** command is to add a user

***#passwd*** is to add/change the password that user
  
  >During user creation **/etc/passwd** file will be impacted
  >
  >A new line will be appended to this file with the following format

user : x : 0 : 0 : userfull name : /home/user : /bin/bash 

