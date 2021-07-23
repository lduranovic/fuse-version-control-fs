## FUSE Version-Control File System

A virtual file system implementation using FUSE that provides basic functionalities for
version control. All the files and folders created by the user are actually stored in a
directory that is part of the inherent file system, but FUSE makes it seem like everything
is stored in the mounting point. Most of the basic Linux system calls (`mkdir`, `readdir`, etc.)
were overwritten to make everything work and to provide the necessary experience for the user.

### Proper usage for the version dump script

The user ought to make the following call:
```bash
bash version_dump.sh <path>
```
The `<path>` variable is supposed to be the relative path of the file. For example, let's say that the file you want to access is called `foo.txt`
and it's stored inside the directory `some_files`. (Naturally all of this is stored inside the `mnt` directory i.e. the `stg` directory)
The call
```bash
bash version_dump.sh some_files/foo.txt
```
will generate a directory called `foo.txt_versions` in the `sysproj-8` folder which will contain the copies of all the version files for the file `foo.txt`.
