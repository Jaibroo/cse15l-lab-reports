# Lab Report 3
***

## #1: Using the Command `find` and `-name`
The first command-line operation for `find` will be the command `-name`:
It is usually structured as `find /path/to/directory -name "example.txt"`, where `example.txt` is replaced by the name of a file or directory.
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
**When used with the `find` command, the -name option allows you to search for files or directories that match a specific name or a pattern and gives you the path as the output. This ultimately allows you to time and effort when working with large sets of files or directories.**

Source: Used Chat-GPT to ask about the functionality of `-name` for the command-line operation `find` as well as how it can be used.

***

## #2: Using the Command `-size` for `find`
A second different command-line operation used along with `find` is `-size`:
It's usually formatted as `find /path/to/directory -size +/-#` where the `+` would represent more and `-` represent less than, as well as where the `#` would be replaced by a number and then a letter variable such as `k`-kilobytes, `M`-megabytes, `c`-bytes and even `G`-gigabytes.
* First Example using `-size` for more than 12 kilobytes:
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

**The `-size` command is essential in looking for files of specific sizes `(k/M/G/c)` and it gives you an output of a list of files that meet that size requirement. This is helpful when working with large files or when trying to free up disk space as you could find and get rid of unecessary files.**

Source: https://www.geeksforgeeks.org/find-command-in-linux-with-examples/

***

## #3: Using the command `-type` for `find`
This third command `-type` is used along with `find`:
The format for entering the input would look something like `find /path/to/search -type f` where the `f` (regular files) would be replaced by either `d` (for directories), `l` for symbolic links, `s` for sockets, `p` for pipes, `c` for special characters, and `b` for block special files.
* First example using `-type d`:
```
$ stringsearch:217$ find stringsearch-data/technical -type d
stringsearch-data/technical
stringsearch-data/technical/911report
stringsearch-data/technical/biomed
stringsearch-data/technical/government
stringsearch-data/technical/government/About_LSC
stringsearch-data/technical/government/Alcohol_Problems
stringsearch-data/technical/government/Env_Prot_Agen
stringsearch-data/technical/government/Gen_Account_Office
stringsearch-data/technical/government/Media
stringsearch-data/technical/government/Post_Rate_Comm
stringsearch-data/technical/plos
```
-Lists all directories within technical path.

* Second Example using `-type f`:
```
$ find stringsearch-data/technical/government/Post_Rate_Comm -type f
stringsearch-data/technical/government/Post_Rate_Comm/Cohenetal_Cost_Function.txt
stringsearch-data/technical/government/Post_Rate_Comm/Cohenetal_CreamSkimming.txt
stringsearch-data/technical/government/Post_Rate_Comm/Cohenetal_DeliveryCost.txt
stringsearch-data/technical/government/Post_Rate_Comm/Cohenetal_RuralDelivery.txt
stringsearch-data/technical/government/Post_Rate_Comm/Cohenetal_Scale.txt
stringsearch-data/technical/government/Post_Rate_Comm/Cohenetal_comparison.txt
stringsearch-data/technical/government/Post_Rate_Comm/Gleiman_EMASpeech.txt
stringsearch-data/technical/government/Post_Rate_Comm/Gleiman_gca2000.txt
stringsearch-data/technical/government/Post_Rate_Comm/Mitchell_6-17-Mit.txt
stringsearch-data/technical/government/Post_Rate_Comm/Mitchell_RMVancouver.txt
stringsearch-data/technical/government/Post_Rate_Comm/Mitchell_spyros-first-class.txt
stringsearch-data/technical/government/Post_Rate_Comm/Redacted_Study.txt
stringsearch-data/technical/government/Post_Rate_Comm/ReportToCongress2002WEB.txt
stringsearch-data/technical/government/Post_Rate_Comm/WolakSpeech_usps.txt
```
-Lists all files within the desired pathway.

**`-type` is used to filter search results by the type of file being searched for. It allows you to narrow down your search results based on the type of file you're interested in, such as regular files, directories, symbolic links, etc. The `-type` option can also be useful when used in conjunction with other options such as `-name` and `-size` to search for files with specifics.**

Source: https://www.howtogeek.com/771399/how-to-use-the-find-command-in-linux/ 

***

## #4: Using Command `-mindepth` for `find`
This fourth command is also used with `find`:
The formatting for using this code looks something to `find /path/to/search -mindepth 2 -type d`, where the number `2` would be replaced with the specific number of depth of the files/directories to be found, while the `d`(directories) could be replaced with an `f` for files limitations.
* First Example using `-mindepth 2 -type d`:
```
$ find stringsearch-data/technical/ -mindepth 2 -type d
stringsearch-data/technical/government/About_LSC
stringsearch-data/technical/government/Alcohol_Problems
stringsearch-data/technical/government/Env_Prot_Agen
stringsearch-data/technical/government/Gen_Account_Office
stringsearch-data/technical/government/Media
stringsearch-data/technical/government/Post_Rate_Comm
```

* Second Example using `mindepth 1 -type f`:
```
$ find stringsearch-data/technical/plos -mindepth 1 -type f
stringsearch-data/technical/plos/journal.pbio.0020001.txt
stringsearch-data/technical/plos/journal.pbio.0020010.txt
stringsearch-data/technical/plos/journal.pbio.0020012.txt
stringsearch-data/technical/plos/journal.pbio.0020013.txt
stringsearch-data/technical/plos/journal.pbio.0020019.txt
stringsearch-data/technical/plos/journal.pbio.0020028.txt
stringsearch-data/technical/plos/journal.pbio.0020035.txt
stringsearch-data/technical/plos/journal.pbio.0020040.txt
stringsearch-data/technical/plos/journal.pbio.0020042.txt
stringsearch-data/technical/plos/journal.pbio.0020043.txt
stringsearch-data/technical/plos/journal.pbio.0020046.txt
stringsearch-data/technical/plos/journal.pbio.0020047.txt
```
-It went on to list the rest of the files in the directory plos.

**The `-mindepth` command is used for specifying the minimum depth of the directory depth that `find` should start searching from. It tells `find` to only consider files and directories that are at least the specified number of levels deep in the directory tree and is useful because it allows you to limit the range of your search to a specific level in the directory tree/path.**

Source: https://www.geeksforgeeks.org/mindepth-maxdepth-linux-find-command-limiting-search-specific-directory/ 
