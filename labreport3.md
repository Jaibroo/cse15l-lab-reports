# Lab Report 3
***

## Using the Command `find` and `-name`
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

Source: Used Chat-GPT to ask about the functionality of `-name` for the command-line operation `find` as well as how it can be used.

***

## Using the Command `-size` for `find`
A second different command-line operation used along with `find` is `-size`:
It's usually formatted as `find /path/to/directory -size +/-#` where the + would represent more and - represent less than, as well as where the # would be replaced by a number and then a letter variable such as k-kilobytes, M-megabytes, c-bytes and even G-gigabytes.
* First Example using -size for more than 12 kilobytes:
```
$ stringsearch:214$ find stringsearch-data/technical/government/Media -size +12k
stringsearch-data/technical/government/Media/Coup_Reshapes_Legal_Aid.txt
stringsearch-data/technical/government/Media/Terrorist_Attack.txt
```
* Second Example: 
```
$ find stringsearch-data/technical/government/Media -size -10k
stringsearch-data/technical/government/Media/5_Legal_Groups.txt
stringsearch-data/technical/government/Media/AP_LawSchoolDebts.txt
stringsearch-data/technical/government/Media/A_Perk_of_Age.txt
stringsearch-data/technical/government/Media/A_helping_hand.txt
stringsearch-data/technical/government/Media/Abuse_penalties.txt
stringsearch-data/technical/government/Media/Advocate_for_Poor.txt
stringsearch-data/technical/government/Media/Aid_Gets_7_Million.txt
stringsearch-data/technical/government/Media/All_May_Have_Justice.txt
stringsearch-data/technical/government/Media/Annual_Fee.txt
stringsearch-data/technical/government/Media/Anthem_Payout.txt
```
-The list continued on until the output was all files less than 10 kilobytes.

**The -size command is essential in looking for files of specific sizes (k/M/G/c) and it gives you an output of a list of files that meet that size requirement. This is helpful when working with large files or when trying to free up disk space as you could find and get rid of unecessary files.**

Source: https://www.geeksforgeeks.org/find-command-in-linux-with-examples/

***

## Using the command `-type` for `find`
This third command `-type` is used along with `find`:
