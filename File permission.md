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


