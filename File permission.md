# Topic:- File Permission
There are 3 types of permission

**Read (r):-** The read permission allows you to open and read the contents of a file but you can't do any editing and modification in the file.

**Write (w):-** The write permission gives you the authority to modify the contents of file.

**execute (x):-** you can't run or execute a program unless execute permission is set.
```sh
read = r
write = w
execute = x
```

## Changing file/directory permission with chmod command

Syntax
```sh
chmod permissions file/directory name
```

There are two ways to use the command

1. Symbolic method
2. Absolute method

## Symbolic method
| operator| Description |
| --- | --- |
| **+** | Adds a permission to a file or directory |
| **-** | remove a permission to a file or directory |
| **=** | Sets the permission and overrides the permissions set earlier. |
| **u** | user/owner |
| **g** | group |
| **o** | other |
| **a** | all |

Example

[prarvesh@main directory]$ ls -l
```sh
-rw-rw-r-- 1 prarvesh prarvesh 0 Aug 21 11:23 file
fist - => It represent a file
rw- => permission for user
rw- => permission for group
r-- => permission for other
```
Some examples using chmod in **symbolic mode**

add read write permission for user and group
```sh
chmod ug+rw file name
```
remove execute permission for all
```sh
chmod a-x filename
```
set the permission read ,write,execute for user and read write for group and read for others
```sh
chmod u=rwx,g=rx,o=r
```
## Absolute method

The table below gives numbers for all for permissions types.
| Number| Permission type | symbol |
| --- | --- | --- |
| **0** | No permission | --- |
| **1** | execute | --x |
| **2** | write | -w- |
| **3** | write,execute | -wx |
| **4** | read | r-- |
| **5** | read,execute | r-x |
| **6** | read,write | rw- |
| **7** | read,write,execute | rwx |

Some examples using chmod in **Absolute mode**

give permission to a file read,write,execute for user and read write for group and read for others
```sh
chmod 764 file name
```
Use of **-R** option with chmod

-R (--recursive) = change files and directories recursively

Example
```sh
chmod -R permissions (directory name)
it set the permission of directory as well as files in the directory
```
## Changing ownership of file/directory
``sh
command : chown
chown command is used to change the file Owner or group.
```


User: A user is the one who created the file. By default, whosoever, creates the file becomes the owner of the file. A user can create, delete, or modify the file.

Group: A group can contain multiple users. All the users belonging to a group have same access permission for a file.

Other: Any one who has access to the file other than user and group comes in the category of other. Other has neither created the file nor is a group member.
