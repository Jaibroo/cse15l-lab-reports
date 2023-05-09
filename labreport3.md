# Lab Report 3
***

## Using the Command `find`
The first command-line operation for `find` will be the command `-name`:
It is usually structured as `find /path/to/directory -name "example.txt"`, where example.txt is replaced by the name of a file or directory.
* An example of using said command would be:
```
$ find stringsearch-data/technical -name "5_Legal_Groups.txt"
stringsearch-data/technical/government/Media/5_Legal_Groups.txt
```
* Second example of using `-name`:
```
$ find stringsearch-data/technical -name "Media"
stringsearch-data/technical/government/Media
```
**When used with the find command, the -name option allows you to search for files or directories that match a specific name or a pattern and gives you the path as the output. This ultimately allows you to time and effort when working with large sets of files or directories.**

