---
### User Types

1. **Normal Users**  - Team
2. **System Users**  - User created for services
3. **Root User**     - Super user 
![143580481-406d844a-06ba-4621-acb6-7d2ae5d19f33](https://user-images.githubusercontent.com/73754563/145420946-c31b522e-f4d6-4f82-a168-888090dd9780.png)

***

Users are identified by UID

  | User | UID |
  |---|---|
  | Root | 0  |
  | System Users | 1-999  |
  | Normal Users | 1000+  |
  
 ***

***#useradd*** command is to add a user
>useradd options
>
>![Screenshot from 2021-11-26 13-00-41](https://user-images.githubusercontent.com/73754563/143580632-99c6a66a-1fe3-4e20-b24a-2e18971febe8.png)


***#passwd*** is to add/change the password that user
***
  
  >During user creation **/etc/passwd** file will be impacted
  >
  >A new line will be appended to this file with the following format

user : x : 0 : 0 : userfull name : /home/user : /bin/bash 


| user | username |
|---|---|
| ***x*** | **Password in encrypted format** |
| ***0*** | **UID / UserID** |
| ***0*** | **GID / Primary Group Id** |
| ***username*** | **User fullname / comment** |
| ***/home/user*** | **Home directory** |
| ***/bin/bash*** | **Default shell** |
***

- User Details - **/etc/passwd**
- Passwords - **/etc/shadow**
- Group details - **/etc/group**
***


>Password will be saved in **/etc/shadow** in the following format

user : $6$16digit$encpassword : password aging policies

| user | username |
|---|---|
| ***$*** | **Feild seperator** |
| ***6*** | **Algorithm code SHA512** |
| ***16digit*** | **Salt value** |
| ***next $-$*** | **Encrypted password** |
| ***next*** | **Password aging policies** |

>**#chage -l user** command will display the password aging policy
![Screenshot from 2021-11-26 17-53-00](https://user-images.githubusercontent.com/73754563/143580481-406d844a-06ba-4621-acb6-7d2ae5d19f33.png)

>The following options can be given with chage command to change password aging policy
![Screenshot from 2021-11-26 17-56-09](https://user-images.githubusercontent.com/73754563/143581036-4aa4a7a1-6218-4f13-beda-b61aa7ebd929.png)

> We can provide default values in **/etc/login.defs** as well
***

Users home director is defaultly copied with some files that comes from **/etc/skell** dir

> ![Screenshot from 2021-12-09 20-09-37](https://user-images.githubusercontent.com/73754563/145418824-342e7e19-132c-4b61-acf1-8d4423b1c84b.png)

- **.bashrc** and **.bash_logout** executes during login time.
- **.bash_logout** executes during logout.

***

> #usermod - this command changes the properties of users
> ![Screenshot from 2021-12-09 20-34-13](https://user-images.githubusercontent.com/73754563/145421140-b6157eb3-853e-4562-81a3-72354549d1e4.png)


