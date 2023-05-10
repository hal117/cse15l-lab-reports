# Lab Report 3 by: Harrison Le
---
# Reasearching Commands `find`
---
The `find` command is a useful command that allows the user to search for various files within a directory or folder. This command proves its versatility when being provided
with large repositories and want to find a specific file immediately. There are many different ways you can use this command and many different keywords to help you with that
being `-name`, `type`, `-path`, `-size`. 

# Using `-name`
---
When we use `-name` after the `find` command in the terminal, Bash will search for files based on that name or pattern. The command would look something like this.

`$ find <current directory> -name <what you want to find>`

First Example:
`$ find technical -name chapter-1.txt`

![Image](namecommand.png)

Second Example:
`$ find technical -name journal.pbio.0020001.txt`

![Image](namecommand2.png)

# Using `-size`
---
The `-size` command allows the user to look for every file that is larger than or less than a certain size. This is espescially useful when searching for multiple files of the same size. The command would look something like this. For reference you can measure the size value of files in bytes, kilobytes, megabytes, etc. 

`$ find <current directory> -path <part of path>`

First Example:
`$ find technical -size +200k` (This command finds files that are larger than 200 kilobytes where the k represents the kilobytes).

![Image](sizecommand.png)

Second Example:
`$ find technical -size  -1000c` (This command finds files that are smaller than 1000 kilobytes where the c represents the bytes).

![Image](sizecommand2.png)
