### Proper usage for the version dump script

The user ought to make the following call:
```
bash version_dump.sh <path>
```
The `<path>` variable is supposed to be the relative path of the file. For example, let's say that the file you want to access is called `foo.txt`
and it's stored inside the directory `some_files`. (Naturally all of this is stored inside the `mnt` directory i.e. the `stg` directory)
The call
```
bash version_dump.sh some_files/foo.txt
```
will generate a directory called `foo.txt_versions` in the `sysproj-8` folder which will contain the copies of all the version files for the file `foo.txt`.