25/11/2025

# chmod
Tool used to update the permissions of an object.

```bash
ls -l
```
Running this will display the file permissions.

The first charactor is type.
- for a file, d for a directory

The remaining 9 characters are split into 3 groups of 3.
For all three groups the characters represet
1. read     (r)
2. write    (w)
3. execute  (x)

A dash (-) means that permission is not permitted.

- The first 3 characters are user permissions (for the owner of the file)
- The next 3 characters are group permissions.
- The final 3 characters are for anyone not in the first two groups.

The permissons can be updated in a few ways.
- who - Who's permissions are we updating (a is the default, if it's left blank)
    - u user/owner of the file
    - g group
    - o other (not user or group)
    - a all of the above
- what what action are we taking (adding or removing permissoin)
    - + add the permission
    - - remove the permission
    - = set the specified permission and remove all others
- which - Which permission do we want to act on
    - r read
    - w write
    - x execute

```bash
chmod u+x
```

Would mean add execture permission to the user group.


```bash
chmod u=rw, og+r new_file.txt
```
In this example,

The user would have read and write access permissions. If they had
executable permissions it would be removed.

The group and other would have the read permission added.

These permissoin would be applied to new_file.txt

## Numerical shorthand
Permissions can also be set like this;


```bash
chmod 777 new_file.text
```
This would permit all actions for all.

0. No permissions                       (000)
1. Execute permisson                    (001)
2. write permission                     (010)
3. Write and exectute permissons        (011)
4. Read permisson                       (100)
5. Read and execute permissions         (101)
6. Read and write permissions           (110)
7. Read, write and execute permissions  (111)

